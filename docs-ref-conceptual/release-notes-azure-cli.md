---
title: Azure CLI 2.0 发行说明
description: 了解 Azure CLI 2.0 的最新更新
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 04/10/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 254c7b306440d921cef6b611268839150fdf3196
ms.sourcegitcommit: 15d6dfaee2075d0abceb2aa2423f0b6ef7b2ac9b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2018
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="61198-103">Azure CLI 2.0 发行说明</span><span class="sxs-lookup"><span data-stu-id="61198-103">Azure CLI 2.0 release notes</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="61198-104">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="61198-104">May 7, 2018</span></span>

<span data-ttu-id="61198-105">版本 2.0.32</span><span class="sxs-lookup"><span data-stu-id="61198-105">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="61198-106">核心</span><span class="sxs-lookup"><span data-stu-id="61198-106">Core</span></span>

* <span data-ttu-id="61198-107">修复了使用证书从服务主体帐户检索机密时引发未处理异常的问题</span><span class="sxs-lookup"><span data-stu-id="61198-107">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="61198-108">增加了对位置参数的有限支持</span><span class="sxs-lookup"><span data-stu-id="61198-108">Added limited support for positional arguments</span></span>
* <span data-ttu-id="61198-109">修复了 `--query` 无法与 `--ids` 一起使用的问题。</span><span class="sxs-lookup"><span data-stu-id="61198-109">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="61198-110">#5591</span><span class="sxs-lookup"><span data-stu-id="61198-110">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="61198-111">改进了使用 `--ids` 时通过命令执行的管道方案。</span><span class="sxs-lookup"><span data-stu-id="61198-111">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="61198-112">支持在指定查询的情况下使用 `-o tsv`，或者在不指定查询的情况下使用 `-o json`</span><span class="sxs-lookup"><span data-stu-id="61198-112">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="61198-113">增加了在用户的命令中存在拼写错误的情况下，针对错误提供命令建议的功能</span><span class="sxs-lookup"><span data-stu-id="61198-113">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="61198-114">改进了用户键入 `az ''` 时出现的错误</span><span class="sxs-lookup"><span data-stu-id="61198-114">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="61198-115">增加了针对命令模块和扩展自定义资源类型的功能</span><span class="sxs-lookup"><span data-stu-id="61198-115">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="61198-116">ACR</span><span class="sxs-lookup"><span data-stu-id="61198-116">ACR</span></span>

* <span data-ttu-id="61198-117">增加了 ACR 生成命令</span><span class="sxs-lookup"><span data-stu-id="61198-117">Added ACR Build commands</span></span>
* <span data-ttu-id="61198-118">改进了“找不到资源”类型的错误消息</span><span class="sxs-lookup"><span data-stu-id="61198-118">Improved resource not found error messages</span></span>
* <span data-ttu-id="61198-119">改进了资源创建性能和错误处理</span><span class="sxs-lookup"><span data-stu-id="61198-119">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="61198-120">改进了 acr 登录非标准控制台和 WSL</span><span class="sxs-lookup"><span data-stu-id="61198-120">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="61198-121">改进了存储库命令错误消息</span><span class="sxs-lookup"><span data-stu-id="61198-121">Improved repository commands error messages</span></span>
* <span data-ttu-id="61198-122">更新了表列和排序</span><span class="sxs-lookup"><span data-stu-id="61198-122">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="61198-123">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-123">ACS</span></span>

* <span data-ttu-id="61198-124">增加了“`az aks` 是预览版服务”警告</span><span class="sxs-lookup"><span data-stu-id="61198-124">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="61198-125">修复了未指定 `--aci-resource-group` 时 `aks install-connector` 中的权限问题</span><span class="sxs-lookup"><span data-stu-id="61198-125">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="61198-126">AMS</span><span class="sxs-lookup"><span data-stu-id="61198-126">AMS</span></span>

* <span data-ttu-id="61198-127">初始版本 - 管理 Azure 媒体服务资源</span><span class="sxs-lookup"><span data-stu-id="61198-127">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-128">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-128">Appservice</span></span>

* <span data-ttu-id="61198-129">修复了提供 `--slot` 时 `webapp delete` 中的 Bug</span><span class="sxs-lookup"><span data-stu-id="61198-129">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="61198-130">从 `webapp auth update` 删除了 `--runtime-version`</span><span class="sxs-lookup"><span data-stu-id="61198-130">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="61198-131">增加了对 min\_tls\_version & https2.0 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-131">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="61198-132">增加了对多容器的支持</span><span class="sxs-lookup"><span data-stu-id="61198-132">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="61198-133">Batch AI</span><span class="sxs-lookup"><span data-stu-id="61198-133">Batch AI</span></span>

* <span data-ttu-id="61198-134">更改了 `batchai create cluster`，以便遵循在群集的配置文件中配置的 VM 优先级</span><span class="sxs-lookup"><span data-stu-id="61198-134">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="61198-135">认知服务</span><span class="sxs-lookup"><span data-stu-id="61198-135">Cognitive Services</span></span>

* <span data-ttu-id="61198-136">修复了在 `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603) 的示例中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="61198-136">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="61198-137">消耗</span><span class="sxs-lookup"><span data-stu-id="61198-137">Consumption</span></span>

* <span data-ttu-id="61198-138">增加了预算 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="61198-138">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="61198-139">容器</span><span class="sxs-lookup"><span data-stu-id="61198-139">Container</span></span>

* <span data-ttu-id="61198-140">删除了在映像名称中包括注册表服务器时对 `container create` 命令的 `--registry-server` 参数的要求</span><span class="sxs-lookup"><span data-stu-id="61198-140">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="61198-141">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61198-141">Cosmos DB</span></span>

* <span data-ttu-id="61198-142">引入针对 Azure CLI 的 VNET 支持 - Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61198-142">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="61198-143">DMS</span><span class="sxs-lookup"><span data-stu-id="61198-143">DMS</span></span>

* <span data-ttu-id="61198-144">初始版本 - 为 Azure SQL 迁移方案增加了对 SQL 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-144">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="61198-145">分机</span><span class="sxs-lookup"><span data-stu-id="61198-145">Extension</span></span>

* <span data-ttu-id="61198-146">修复了停止显示扩展元数据的 Bug</span><span class="sxs-lookup"><span data-stu-id="61198-146">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="61198-147">交互</span><span class="sxs-lookup"><span data-stu-id="61198-147">Interactive</span></span>

* <span data-ttu-id="61198-148">允许交互式补全选项使用位置参数</span><span class="sxs-lookup"><span data-stu-id="61198-148">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="61198-149">增强用户键入 '\' 时的输出的用户友好性</span><span class="sxs-lookup"><span data-stu-id="61198-149">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="61198-150">修复了在没有帮助的情况下参数的补全问题</span><span class="sxs-lookup"><span data-stu-id="61198-150">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="61198-151">修复了命令组的说明问题</span><span class="sxs-lookup"><span data-stu-id="61198-151">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="61198-152">实验室</span><span class="sxs-lookup"><span data-stu-id="61198-152">Lab</span></span>

* <span data-ttu-id="61198-153">修复了 Knack 转换的回归问题</span><span class="sxs-lookup"><span data-stu-id="61198-153">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="61198-154">网络</span><span class="sxs-lookup"><span data-stu-id="61198-154">Network</span></span>

* <span data-ttu-id="61198-155">[重大更改] 删除了以下项的 `--ids` 参数：</span><span class="sxs-lookup"><span data-stu-id="61198-155">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span> 
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="61198-156">配置文件</span><span class="sxs-lookup"><span data-stu-id="61198-156">Profile</span></span>

* <span data-ttu-id="61198-157">修复了 `disk create` 源检测问题</span><span class="sxs-lookup"><span data-stu-id="61198-157">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="61198-158">[重大更改] 删除了不再使用的 `--msi-port` 和 `--identity-port`</span><span class="sxs-lookup"><span data-stu-id="61198-158">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="61198-159">修复了 `account get-access-token` 短摘要中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="61198-159">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="61198-160">Redis</span><span class="sxs-lookup"><span data-stu-id="61198-160">Redis</span></span>

* <span data-ttu-id="61198-161">弃用 `redis patch-schedule patch-schedule show` 而改用 `redis patch-schedule show`</span><span class="sxs-lookup"><span data-stu-id="61198-161">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="61198-162">弃用 `redis list-all`。</span><span class="sxs-lookup"><span data-stu-id="61198-162">Deprecated `redis list-all`.</span></span> <span data-ttu-id="61198-163">此功能已加入 `redis list` 中</span><span class="sxs-lookup"><span data-stu-id="61198-163">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="61198-164">弃用 `redis import-method` 而改用 `redis import`</span><span class="sxs-lookup"><span data-stu-id="61198-164">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="61198-165">为各种命令增加了对 `--ids` 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-165">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="61198-166">角色</span><span class="sxs-lookup"><span data-stu-id="61198-166">Role</span></span>

* <span data-ttu-id="61198-167">[重大更改] 删除了已弃用的 `ad sp reset-credentials`</span><span class="sxs-lookup"><span data-stu-id="61198-167">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="61198-168">存储</span><span class="sxs-lookup"><span data-stu-id="61198-168">Storage</span></span>

* <span data-ttu-id="61198-169">在源 SAS 和帐户密钥未指定的情况下，允许将目标 SAS 令牌应用到源，以便进行 Blob 复制</span><span class="sxs-lookup"><span data-stu-id="61198-169">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="61198-170">公开了用于 Blob 上传和下载的 --socket-timeout 参数</span><span class="sxs-lookup"><span data-stu-id="61198-170">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="61198-171">将以路径分隔符开头的 Blob 名称视为相对路径</span><span class="sxs-lookup"><span data-stu-id="61198-171">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="61198-172">允许 `storage blob copy --source-sas` 以查询字符“?”开头</span><span class="sxs-lookup"><span data-stu-id="61198-172">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="61198-173">修复了 `storage entity query --marker` 问题，接受“键=值”列表</span><span class="sxs-lookup"><span data-stu-id="61198-173">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="61198-174">VM</span><span class="sxs-lookup"><span data-stu-id="61198-174">VM</span></span>

* <span data-ttu-id="61198-175">修复了非托管 Blob URI 上的检测逻辑无效的问题</span><span class="sxs-lookup"><span data-stu-id="61198-175">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="61198-176">增加了在没有用户提供的服务主体的情况下进行磁盘加密的功能</span><span class="sxs-lookup"><span data-stu-id="61198-176">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="61198-177">[重大更改] 请勿使用 VM“ManagedIdentityExtension”来寻求 MSI 支持</span><span class="sxs-lookup"><span data-stu-id="61198-177">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="61198-178">增加了对 `vmss` 使用逐出策略的支持</span><span class="sxs-lookup"><span data-stu-id="61198-178">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="61198-179">[重大更改] 从以下项删除了 `--ids`：</span><span class="sxs-lookup"><span data-stu-id="61198-179">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="61198-180">增加了写入加速器支持</span><span class="sxs-lookup"><span data-stu-id="61198-180">Added write accelerator support</span></span> 
* <span data-ttu-id="61198-181">添加了 `vmss perform-maintenance`</span><span class="sxs-lookup"><span data-stu-id="61198-181">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="61198-182">修复了 `vm diagnostics set` 问题，可以可靠地检测 VM 的 OS 类型</span><span class="sxs-lookup"><span data-stu-id="61198-182">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="61198-183">更改了 `vm resize`，系统会检查请求的大小是否不同于当前设置的大小，只在二者有变化时进行更新</span><span class="sxs-lookup"><span data-stu-id="61198-183">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="61198-184">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="61198-184">April 10, 2018</span></span>

<span data-ttu-id="61198-185">版本 2.0.31</span><span class="sxs-lookup"><span data-stu-id="61198-185">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="61198-186">ACR</span><span class="sxs-lookup"><span data-stu-id="61198-186">ACR</span></span>

* <span data-ttu-id="61198-187">改进了 wincred 回退错误处理</span><span class="sxs-lookup"><span data-stu-id="61198-187">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="61198-188">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-188">ACS</span></span>

* <span data-ttu-id="61198-189">更改了 aks 创建的 SPN，使其有效期达到 5 年</span><span class="sxs-lookup"><span data-stu-id="61198-189">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-190">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-190">Appservice</span></span>

* [重大更改]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="61198-192">修复了 Web 应用计划不存在导致的未捕获异常</span><span class="sxs-lookup"><span data-stu-id="61198-192">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="61198-193">BatchAI</span><span class="sxs-lookup"><span data-stu-id="61198-193">BatchAI</span></span>

* <span data-ttu-id="61198-194">添加了对 2018-03-01 API 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-194">Added support for 2018-03-01 API</span></span>

 - <span data-ttu-id="61198-195">作业级装载</span><span class="sxs-lookup"><span data-stu-id="61198-195">Job level mounting</span></span>
 - <span data-ttu-id="61198-196">使用机密值的环境变量</span><span class="sxs-lookup"><span data-stu-id="61198-196">Environment variables with secret values</span></span>
 - <span data-ttu-id="61198-197">性能计数器设置</span><span class="sxs-lookup"><span data-stu-id="61198-197">Performance counters settings</span></span>
 - <span data-ttu-id="61198-198">报告作业特定的路径段</span><span class="sxs-lookup"><span data-stu-id="61198-198">Reporting of job specific path segment</span></span>
 - <span data-ttu-id="61198-199">支持“列出文件”API 中的子文件夹</span><span class="sxs-lookup"><span data-stu-id="61198-199">Support for subfolders in list files api</span></span>
 - <span data-ttu-id="61198-200">使用情况和限制报告</span><span class="sxs-lookup"><span data-stu-id="61198-200">Usage and limits reporting</span></span>
 - <span data-ttu-id="61198-201">允许为 NFS 服务器指定缓存类型</span><span class="sxs-lookup"><span data-stu-id="61198-201">Allow to specify caching type for NFS servers</span></span>
 - <span data-ttu-id="61198-202">支持自定义映像</span><span class="sxs-lookup"><span data-stu-id="61198-202">Support for custom images</span></span>
 - <span data-ttu-id="61198-203">添加了 pyTorch 工具包支持</span><span class="sxs-lookup"><span data-stu-id="61198-203">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="61198-204">添加了 `job wait` 命令，以允许等待作业完成和报告作业退出代码</span><span class="sxs-lookup"><span data-stu-id="61198-204">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="61198-205">添加了 `usage show` 命令，用于列出不同区域的当前 Batch AI 资源使用情况和限制</span><span class="sxs-lookup"><span data-stu-id="61198-205">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="61198-206">支持国家云</span><span class="sxs-lookup"><span data-stu-id="61198-206">National clouds are supported</span></span>
* <span data-ttu-id="61198-207">添加了作业命令行参数，以便除了装载配置文件以外，还能装载作业级别的文件系统</span><span class="sxs-lookup"><span data-stu-id="61198-207">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="61198-208">添加了更多选项用于自定义群集 - VM 优先级、子网、自动缩放群集的初始节点计数，以及指定自定义映像</span><span class="sxs-lookup"><span data-stu-id="61198-208">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="61198-209">添加了命令行选项用于指定 Batch AI 托管 NFS 的缓存类型</span><span class="sxs-lookup"><span data-stu-id="61198-209">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="61198-210">简化了在配置文件中指定装载文件系统的方法。</span><span class="sxs-lookup"><span data-stu-id="61198-210">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="61198-211">现在，可以省略 Azure 文件共享和 Azure Blob 容器的凭据 - CLI 将会使用通过命令行参数提供的或通过环境变量指定的存储帐户密钥来填充缺少的凭据，或者从 Azure 存储查询密钥（如果存储帐户属于当前订阅）</span><span class="sxs-lookup"><span data-stu-id="61198-211">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="61198-212">作业完成后（成功、失败、已终止或已删除），作业文件流命令现在会自动完成</span><span class="sxs-lookup"><span data-stu-id="61198-212">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="61198-213">改进了 `show` 操作的 `table` 输出</span><span class="sxs-lookup"><span data-stu-id="61198-213">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="61198-214">添加了 `--use-auto-storage` 选项用于创建群集。</span><span class="sxs-lookup"><span data-stu-id="61198-214">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="61198-215">使用此选项可以更方便地管理存储帐户，以及将 Azure 文件共享和 Azure Blob 容器装载到群集</span><span class="sxs-lookup"><span data-stu-id="61198-215">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="61198-216">为 `cluster create` 和 `file-server create` 添加了 `--generate-ssh-keys` 选项</span><span class="sxs-lookup"><span data-stu-id="61198-216">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="61198-217">添加了通过命令行提供节点设置任务的功能</span><span class="sxs-lookup"><span data-stu-id="61198-217">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="61198-218">[重大更改]移动了 `job file` 组下面的 `job stream-file` 和 `job list-files` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-218">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="61198-219">[重大更改]已将 `file-server create` 命令中的 `--admin-user-name` 重命名为 `--user-name`，使其与 `cluster create` 命令一致</span><span class="sxs-lookup"><span data-stu-id="61198-219">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="61198-220">计费</span><span class="sxs-lookup"><span data-stu-id="61198-220">Billing</span></span>

* <span data-ttu-id="61198-221">添加了登记帐户命令</span><span class="sxs-lookup"><span data-stu-id="61198-221">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="61198-222">消耗</span><span class="sxs-lookup"><span data-stu-id="61198-222">Consumption</span></span>

* <span data-ttu-id="61198-223">添加了 `marketplace` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-223">Added `marketplace` commands</span></span>
* <span data-ttu-id="61198-224">[重大更改] 已将 `reservations summaries` 重命名为 `reservation summary`</span><span class="sxs-lookup"><span data-stu-id="61198-224">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="61198-225">[重大更改] 已将 `reservations details` 重命名为 `reservation detail`</span><span class="sxs-lookup"><span data-stu-id="61198-225">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="61198-226">[重大更改]删除了 `reservation` 命令的 `--reservation-order-id` 和 `--reservation-id` 短选项</span><span class="sxs-lookup"><span data-stu-id="61198-226">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="61198-227">[重大更改]删除了 `reservation summary` 命令的 `--grain` 短选项</span><span class="sxs-lookup"><span data-stu-id="61198-227">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="61198-228">[重大更改]删除了 `pricesheet` 命令的 `--include-meter-details` 短选项</span><span class="sxs-lookup"><span data-stu-id="61198-228">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="61198-229">容器</span><span class="sxs-lookup"><span data-stu-id="61198-229">Container</span></span>

* <span data-ttu-id="61198-230">添加了 git 存储库卷装载参数 `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` 和 `--gitrepo-mount-path`</span><span class="sxs-lookup"><span data-stu-id="61198-230">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="61198-231">修复了 [#5926](https://github.com/Azure/azure-cli/issues/5926)：指定 --container-name 时 `az container exec` 失败</span><span class="sxs-lookup"><span data-stu-id="61198-231">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="61198-232">分机</span><span class="sxs-lookup"><span data-stu-id="61198-232">Extension</span></span>

* <span data-ttu-id="61198-233">已将分配检查消息更改为调试级别</span><span class="sxs-lookup"><span data-stu-id="61198-233">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="61198-234">交互</span><span class="sxs-lookup"><span data-stu-id="61198-234">Interactive</span></span>

* <span data-ttu-id="61198-235">更改为在命令不可识别时停止完成</span><span class="sxs-lookup"><span data-stu-id="61198-235">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="61198-236">添加了创建命令子树之前和之后所用的事件挂钩</span><span class="sxs-lookup"><span data-stu-id="61198-236">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="61198-237">添加了 `--ids` 参数补全</span><span class="sxs-lookup"><span data-stu-id="61198-237">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="61198-238">网络</span><span class="sxs-lookup"><span data-stu-id="61198-238">Network</span></span>

* <span data-ttu-id="61198-239">修复了 [#5936](https://github.com/Azure/azure-cli/issues/5936)：无法设置 `application-gateway create` 标记</span><span class="sxs-lookup"><span data-stu-id="61198-239">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="61198-240">添加了参数 `--auth-certs`，以附加 `application-gateway http-settings [create|update]` 的身份验证证书。</span><span class="sxs-lookup"><span data-stu-id="61198-240">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="61198-241">#4910</span><span class="sxs-lookup"><span data-stu-id="61198-241">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="61198-242">添加了 `ddos-protection` 命令用于创建 DDoS 保护计划</span><span class="sxs-lookup"><span data-stu-id="61198-242">Added `ddos-protection` commands to create DDoS protection plans</span></span> 
* <span data-ttu-id="61198-243">为 `vnet [create|update]` 添加了 `--ddos-protection-plan` 支持，以便将 VNet 关联到 DDoS 保护计划</span><span class="sxs-lookup"><span data-stu-id="61198-243">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="61198-244">修复了 `network route-table [create|update]` 中 `--disable-bgp-route-propagation` 标志的问题</span><span class="sxs-lookup"><span data-stu-id="61198-244">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="61198-245">删除了 `network lb [create|update]` 的虚拟参数 `--public-ip-address-type` 和 `--subnet-type`</span><span class="sxs-lookup"><span data-stu-id="61198-245">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="61198-246">为 `network dns zone [import|export]` 和 `network dns record-set txt add-record` 添加了采用 RFC 1035 转义序列的 TXT 记录支持</span><span class="sxs-lookup"><span data-stu-id="61198-246">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="61198-247">配置文件</span><span class="sxs-lookup"><span data-stu-id="61198-247">Profile</span></span>

* <span data-ttu-id="61198-248">在 `account list` 中添加了 Azure 经典帐户支持</span><span class="sxs-lookup"><span data-stu-id="61198-248">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="61198-249">[重大更改]删除了 `--msi` & `--msi-port` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-249">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="61198-250">RDBMS</span><span class="sxs-lookup"><span data-stu-id="61198-250">RDBMS</span></span>

* <span data-ttu-id="61198-251">添加了 `georestore` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-251">Added `georestore` command</span></span>
* <span data-ttu-id="61198-252">删除了 `create` 命令的存储大小限制</span><span class="sxs-lookup"><span data-stu-id="61198-252">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="61198-253">资源</span><span class="sxs-lookup"><span data-stu-id="61198-253">Resource</span></span>

* <span data-ttu-id="61198-254">在 `policy definition create` 中添加了对 `--metadata` 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-254">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="61198-255">为 `policy definition update` 添加了对 `--metadata`、`--set`、`--add` 和 `--remove` 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-255">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="61198-256">SQL</span><span class="sxs-lookup"><span data-stu-id="61198-256">SQL</span></span>

* <span data-ttu-id="61198-257">添加了 `sql elastic-pool op list` 和 `sql elastic-pool op cancel`</span><span class="sxs-lookup"><span data-stu-id="61198-257">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="61198-258">存储</span><span class="sxs-lookup"><span data-stu-id="61198-258">Storage</span></span>

* <span data-ttu-id="61198-259">改进了有关连接字符串格式不当的错误消息</span><span class="sxs-lookup"><span data-stu-id="61198-259">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="61198-260">VM</span><span class="sxs-lookup"><span data-stu-id="61198-260">VM</span></span>

* <span data-ttu-id="61198-261">为 `vmss create` 添加了配置平台容错域计数的支持</span><span class="sxs-lookup"><span data-stu-id="61198-261">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="61198-262">已将 `vmss create` 的默认值更改为区域性、大型或禁用单一位置组的规模集的标准负载均衡器</span><span class="sxs-lookup"><span data-stu-id="61198-262">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [重大更改]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="61198-264">为 `vm create` 添加了对公共 IP SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-264">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="61198-265">为 `vm secret format` 添加了 `--keyvault` 和 `--resource-group` 参数，以便在命令无法解析保管库 ID 的情况下提供支持。</span><span class="sxs-lookup"><span data-stu-id="61198-265">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="61198-266">#5718</span><span class="sxs-lookup"><span data-stu-id="61198-266">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="61198-267">改进了当资源组的位置不支持区域时，`[vm|vmss create]` 发生的错误</span><span class="sxs-lookup"><span data-stu-id="61198-267">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="61198-268">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="61198-268">March 27, 2018</span></span>

<span data-ttu-id="61198-269">版本 2.0.30</span><span class="sxs-lookup"><span data-stu-id="61198-269">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="61198-270">核心</span><span class="sxs-lookup"><span data-stu-id="61198-270">Core</span></span>

* <span data-ttu-id="61198-271">为帮助中标记为预览版的扩展显示消息</span><span class="sxs-lookup"><span data-stu-id="61198-271">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="61198-272">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-272">ACS</span></span>

* <span data-ttu-id="61198-273">为 Cloud Shell 中的 `aks install-cli` 修复 SSL 证书验证错误</span><span class="sxs-lookup"><span data-stu-id="61198-273">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-274">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-274">Appservice</span></span>

* <span data-ttu-id="61198-275">为 `webapp update` 添加了仅限 HTTPS 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-275">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="61198-276">为 `az webapp identity [assign|show]` 和 `az functionapp identity [assign|show]` 添加了对插槽的支持</span><span class="sxs-lookup"><span data-stu-id="61198-276">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="61198-277">备份</span><span class="sxs-lookup"><span data-stu-id="61198-277">Backup</span></span>

* <span data-ttu-id="61198-278">添加了新命令 `az backup protection isenabled-for-vm`。</span><span class="sxs-lookup"><span data-stu-id="61198-278">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="61198-279">此命令可用于检查 VM 是否已由订阅中的任何保管库备份</span><span class="sxs-lookup"><span data-stu-id="61198-279">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="61198-280">为下列命令的 `--resource-group` 和 `--vault-name` 参数启用了 Azure 对象 ID：</span><span class="sxs-lookup"><span data-stu-id="61198-280">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="61198-281">更改了 `--name` 参数以接受 `backup ... show` 命令的输出格式</span><span class="sxs-lookup"><span data-stu-id="61198-281">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="61198-282">容器</span><span class="sxs-lookup"><span data-stu-id="61198-282">Container</span></span>

* <span data-ttu-id="61198-283">添加了 `container exec` 命令。</span><span class="sxs-lookup"><span data-stu-id="61198-283">Added `container exec` command.</span></span> <span data-ttu-id="61198-284">在正在运行的容器组的容器中执行命令</span><span class="sxs-lookup"><span data-stu-id="61198-284">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="61198-285">允许将表输出用于创建和更新容器组</span><span class="sxs-lookup"><span data-stu-id="61198-285">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="61198-286">分机</span><span class="sxs-lookup"><span data-stu-id="61198-286">Extension</span></span>

* <span data-ttu-id="61198-287">为 `extension add` 添加了消息（如果扩展处于预览状态）</span><span class="sxs-lookup"><span data-stu-id="61198-287">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="61198-288">更改了 `extension list-available` 以通过 `--show-details` 显示完整扩展数据</span><span class="sxs-lookup"><span data-stu-id="61198-288">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="61198-289">[重大更改] 更改了 `extension list-available` 以在默认情况下显示简化的扩展数据</span><span class="sxs-lookup"><span data-stu-id="61198-289">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="61198-290">交互</span><span class="sxs-lookup"><span data-stu-id="61198-290">Interactive</span></span>

* <span data-ttu-id="61198-291">已将“完成”更改为在执行命令表加载后立即激活</span><span class="sxs-lookup"><span data-stu-id="61198-291">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="61198-292">修复了使用 `--style` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-292">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="61198-293">交互式词法分析器在命令表转储后实例化（如果缺失）</span><span class="sxs-lookup"><span data-stu-id="61198-293">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="61198-294">改进了完成符支持</span><span class="sxs-lookup"><span data-stu-id="61198-294">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="61198-295">实验室</span><span class="sxs-lookup"><span data-stu-id="61198-295">Lab</span></span>

* <span data-ttu-id="61198-296">修复了 `create environment` 命令的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-296">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="61198-297">监视</span><span class="sxs-lookup"><span data-stu-id="61198-297">Monitor</span></span>

* <span data-ttu-id="61198-298">为 `metrics list` 添加了对 `--top`、`--orderby` 和 `--namespace` 的支持 [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="61198-298">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="61198-299">修复了 [#4529](https://github.com/Azure/azure-cli/issues/5785)：`metrics list`接受要检索的指标的空格分隔列表</span><span class="sxs-lookup"><span data-stu-id="61198-299">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="61198-300">为 `metrics list-definitions` 添加了对 `--namespace` 的支持 [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="61198-300">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="61198-301">网络</span><span class="sxs-lookup"><span data-stu-id="61198-301">Network</span></span>

* <span data-ttu-id="61198-302">添加了对专用 DNS 区域的支持</span><span class="sxs-lookup"><span data-stu-id="61198-302">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="61198-303">配置文件</span><span class="sxs-lookup"><span data-stu-id="61198-303">Profile</span></span>

* <span data-ttu-id="61198-304">为 `login` 添加了针对 `--identity-port` 和 `--msi-port` 的警告</span><span class="sxs-lookup"><span data-stu-id="61198-304">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="61198-305">RDBMS</span><span class="sxs-lookup"><span data-stu-id="61198-305">RDBMS</span></span>

* <span data-ttu-id="61198-306">添加了业务模型 GA API 版本 2017-12-01</span><span class="sxs-lookup"><span data-stu-id="61198-306">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="61198-307">资源</span><span class="sxs-lookup"><span data-stu-id="61198-307">Resource</span></span>

* [重大更改]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="61198-309">角色</span><span class="sxs-lookup"><span data-stu-id="61198-309">Role</span></span>

* <span data-ttu-id="61198-310">为 `az ad app create` 添加了对所需访问权限配置和本机客户端的支持</span><span class="sxs-lookup"><span data-stu-id="61198-310">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="61198-311">更改了 `rbac` 命令以在对象解析时返回少于 1000 个的 ID</span><span class="sxs-lookup"><span data-stu-id="61198-311">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="61198-312">添加了凭据管理命令 `ad sp credential [reset|list|delete]`</span><span class="sxs-lookup"><span data-stu-id="61198-312">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="61198-313">[重大更改] 从 `az role assignment [list|show]` 输出中删除了“properties”</span><span class="sxs-lookup"><span data-stu-id="61198-313">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="61198-314">为 `role definition` 添加了对 `dataActions` 和 `notDataActions` 权限的支持</span><span class="sxs-lookup"><span data-stu-id="61198-314">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="61198-315">存储</span><span class="sxs-lookup"><span data-stu-id="61198-315">Storage</span></span>

* <span data-ttu-id="61198-316">修复了在上传大小介于 195GB 和 200GB 之间的文件时存在的问题</span><span class="sxs-lookup"><span data-stu-id="61198-316">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="61198-317">修复了 [#4049](https://github.com/Azure/azure-cli/issues/4049)：上传 append 类型的 Blob 时忽略条件参数的问题</span><span class="sxs-lookup"><span data-stu-id="61198-317">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="61198-318">VM</span><span class="sxs-lookup"><span data-stu-id="61198-318">VM</span></span>

* <span data-ttu-id="61198-319">针对即将到来的、适用于包含 100 个以上实例的集合的重大更改，为 `vmss create` 添加了警告</span><span class="sxs-lookup"><span data-stu-id="61198-319">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="61198-320">为 `vm [snapshot|image]` 添加了区域弹性支持</span><span class="sxs-lookup"><span data-stu-id="61198-320">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="61198-321">更改了磁盘实例视图以更好地报告加密状态</span><span class="sxs-lookup"><span data-stu-id="61198-321">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="61198-322">[重大更改] 更改了 `vm extension delete` 以不再返回输出</span><span class="sxs-lookup"><span data-stu-id="61198-322">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="61198-323">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="61198-323">March 13, 2018</span></span>

<span data-ttu-id="61198-324">版本 2.0.29</span><span class="sxs-lookup"><span data-stu-id="61198-324">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="61198-325">ACR</span><span class="sxs-lookup"><span data-stu-id="61198-325">ACR</span></span>

* <span data-ttu-id="61198-326">为 `repository delete` 添加了对 `--image` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="61198-326">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="61198-327">弃用了 `repository delete` 命令的 `--manifest` 和 `--tag` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-327">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="61198-328">添加了 `repository untag` 命令以在不删除数据的情况下删除标记</span><span class="sxs-lookup"><span data-stu-id="61198-328">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="61198-329">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-329">ACS</span></span>

* <span data-ttu-id="61198-330">添加了 `aks upgrade-connector` 命令以升级现有连接器</span><span class="sxs-lookup"><span data-stu-id="61198-330">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="61198-331">更改了 `kubectl` 配置文件以使用更具可读性的块样式 YAML</span><span class="sxs-lookup"><span data-stu-id="61198-331">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="61198-332">顾问</span><span class="sxs-lookup"><span data-stu-id="61198-332">Advisor</span></span>

* <span data-ttu-id="61198-333">[重大更改] 已将 `advisor configuration get` 重命名为 `advisor configuration list`</span><span class="sxs-lookup"><span data-stu-id="61198-333">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="61198-334">[重大更改] 已将 `advisor configuration set` 重命名为 `advisor configuration update`</span><span class="sxs-lookup"><span data-stu-id="61198-334">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="61198-335">[重大更改] 删除了 `advisor recommendation generate`</span><span class="sxs-lookup"><span data-stu-id="61198-335">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span> 
* <span data-ttu-id="61198-336">为 `advisor recommendation list` 添加了 `--refresh` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-336">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="61198-337">添加了 `advisor recommendation show` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-337">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-338">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-338">Appservice</span></span>

* <span data-ttu-id="61198-339">弃用了 `[webapp|functionapp] assign-identity`</span><span class="sxs-lookup"><span data-stu-id="61198-339">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="61198-340">添加了托管标识命令 `webapp identity [assign|show]` 和 `functionapp identity [assign|show]`</span><span class="sxs-lookup"><span data-stu-id="61198-340">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="61198-341">Eventhubs</span><span class="sxs-lookup"><span data-stu-id="61198-341">Eventhubs</span></span>

* <span data-ttu-id="61198-342">初始版本</span><span class="sxs-lookup"><span data-stu-id="61198-342">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="61198-343">分机</span><span class="sxs-lookup"><span data-stu-id="61198-343">Extension</span></span>

* <span data-ttu-id="61198-344">添加了检查，以在使用的发行版不是程序包源文件中存储的发行版时提醒用户，因为这可能导致错误</span><span class="sxs-lookup"><span data-stu-id="61198-344">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="61198-345">交互</span><span class="sxs-lookup"><span data-stu-id="61198-345">Interactive</span></span>

* <span data-ttu-id="61198-346">修复了 [#5625](https://github.com/Azure/azure-cli/issues/5625)：在不同会话之间永久保留历史记录</span><span class="sxs-lookup"><span data-stu-id="61198-346">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="61198-347">修复了 [#3016](https://github.com/Azure/azure-cli/issues/3016)：在作用域中时不记录历史记录</span><span class="sxs-lookup"><span data-stu-id="61198-347">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="61198-348">修复了 [#5688](https://github.com/Azure/azure-cli/issues/5688)：如果命令表加载遇到了异常，不显示“完成”</span><span class="sxs-lookup"><span data-stu-id="61198-348">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="61198-349">修复了用于长时间运行的操作的进度指示器</span><span class="sxs-lookup"><span data-stu-id="61198-349">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="61198-350">监视</span><span class="sxs-lookup"><span data-stu-id="61198-350">Monitor</span></span>

* <span data-ttu-id="61198-351">弃用了 `monitor autoscale-settings` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-351">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="61198-352">添加了 `monitor autoscale` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-352">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="61198-353">添加了 `monitor autoscale profile` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-353">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="61198-354">添加了 `monitor autoscale rule` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-354">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="61198-355">网络</span><span class="sxs-lookup"><span data-stu-id="61198-355">Network</span></span>

* <span data-ttu-id="61198-356">[重大更改] 从 `route-filter rule create` 中删除了 `--tags` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-356">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="61198-357">删除了以下命令的某些错误默认值：</span><span class="sxs-lookup"><span data-stu-id="61198-357">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="61198-358">添加了 `network watcher connection-monitor` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-358">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="61198-359">为 `network watcher show-topology` 添加了 `--vnet` 和 `--subnet`</span><span class="sxs-lookup"><span data-stu-id="61198-359">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="61198-360">配置文件</span><span class="sxs-lookup"><span data-stu-id="61198-360">Profile</span></span>

* <span data-ttu-id="61198-361">弃用了 `az login` 的 `--msi` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-361">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="61198-362">为 `az login` 添加了 `--identity` 参数以替换 `--msi`</span><span class="sxs-lookup"><span data-stu-id="61198-362">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="61198-363">RDBMS</span><span class="sxs-lookup"><span data-stu-id="61198-363">RDBMS</span></span>

* <span data-ttu-id="61198-364">[预览] 已更改为使用 API 2017-12-01-preview</span><span class="sxs-lookup"><span data-stu-id="61198-364">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="61198-365">服务总线</span><span class="sxs-lookup"><span data-stu-id="61198-365">Service Bus</span></span>

* <span data-ttu-id="61198-366">初始版本</span><span class="sxs-lookup"><span data-stu-id="61198-366">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="61198-367">存储</span><span class="sxs-lookup"><span data-stu-id="61198-367">Storage</span></span>

* <span data-ttu-id="61198-368">修复了 [#4971](https://github.com/Azure/azure-cli/issues/4971)：`storage blob copy` 现在支持其他 Azure 云</span><span class="sxs-lookup"><span data-stu-id="61198-368">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="61198-369">修复了 [#5286](https://github.com/Azure/azure-cli/issues/5286)：Batch 命令 `storage blob [delete-batch|download-batch|upload-batch]` 不再在前置条件失败时引发错误</span><span class="sxs-lookup"><span data-stu-id="61198-369">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="61198-370">VM</span><span class="sxs-lookup"><span data-stu-id="61198-370">VM</span></span>

* <span data-ttu-id="61198-371">为 `[vm|vmss] create` 添加了支持，以附加非托管数据磁盘和配置缓存</span><span class="sxs-lookup"><span data-stu-id="61198-371">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="61198-372">弃用了 `[vm|vmss] assign-identity` 和 `[vm|vmss] remove-identity`</span><span class="sxs-lookup"><span data-stu-id="61198-372">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="61198-373">添加了 `vm identity [assign|remove|show]` 和 `vmss identity [assign|remove|show]` 以替换弃用的命令</span><span class="sxs-lookup"><span data-stu-id="61198-373">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="61198-374">已将 `vmss create` 中的默认优先级更改为 None</span><span class="sxs-lookup"><span data-stu-id="61198-374">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="61198-375">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="61198-375">February 27, 2018</span></span>

<span data-ttu-id="61198-376">版本 2.0.28</span><span class="sxs-lookup"><span data-stu-id="61198-376">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="61198-377">核心</span><span class="sxs-lookup"><span data-stu-id="61198-377">Core</span></span>

* <span data-ttu-id="61198-378">已修复 [#5184](https://github.com/Azure/azure-cli/issues/5184)：Homebrew 安装问题</span><span class="sxs-lookup"><span data-stu-id="61198-378">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="61198-379">添加了对具有自定义密钥的扩展遥测的支持</span><span class="sxs-lookup"><span data-stu-id="61198-379">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="61198-380">为 `--debug` 添加了 HTTP 日志记录</span><span class="sxs-lookup"><span data-stu-id="61198-380">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="61198-381">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-381">ACS</span></span>

* <span data-ttu-id="61198-382">已更改为默认情况下对 `aks install-connector` 使用 `virtual-kubelet-for-aks` Helm 图</span><span class="sxs-lookup"><span data-stu-id="61198-382">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="61198-383">已修复问题：服务主体没有足够的权限来创建 ACI 容器组的问题</span><span class="sxs-lookup"><span data-stu-id="61198-383">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="61198-384">已为 `aks install-connector` 添加了 `--aci-container-group`、`--location` 和 `--image-tag`</span><span class="sxs-lookup"><span data-stu-id="61198-384">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="61198-385">从 `aks get-versions` 中删除了弃用通知</span><span class="sxs-lookup"><span data-stu-id="61198-385">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-386">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-386">Appservice</span></span>

* <span data-ttu-id="61198-387">针对新 SDK 版本 (azure-mgmt-web 0.35.0) 的更新</span><span class="sxs-lookup"><span data-stu-id="61198-387">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="61198-388">已修复 [#5538](https://github.com/Azure/azure-cli/issues/5538)：`Free` 被报告为无效 SKU</span><span class="sxs-lookup"><span data-stu-id="61198-388">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="61198-389">认知服务</span><span class="sxs-lookup"><span data-stu-id="61198-389">Cognitive Services</span></span>

* <span data-ttu-id="61198-390">更新了创建新的认知服务帐户时的“通知”</span><span class="sxs-lookup"><span data-stu-id="61198-390">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="61198-391">消耗</span><span class="sxs-lookup"><span data-stu-id="61198-391">Consumption</span></span>

* <span data-ttu-id="61198-392">为 pricesheet API 添加了新命令</span><span class="sxs-lookup"><span data-stu-id="61198-392">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="61198-393">更新了现有“使用情况详细信息”和“预订详细信息”格式</span><span class="sxs-lookup"><span data-stu-id="61198-393">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="61198-394">容器</span><span class="sxs-lookup"><span data-stu-id="61198-394">Container</span></span>

* <span data-ttu-id="61198-395">为 `container create` 添加了 `--secrets` 和 `--secrets-mount-path` 参数以在 ACI 中使用机密</span><span class="sxs-lookup"><span data-stu-id="61198-395">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="61198-396">网络</span><span class="sxs-lookup"><span data-stu-id="61198-396">Network</span></span>

* <span data-ttu-id="61198-397">修复了 [#5559](https://github.com/Azure/azure-cli/issues/5559)：`network vnet-gateway vpn-client generate` 中缺少客户端</span><span class="sxs-lookup"><span data-stu-id="61198-397">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="61198-398">资源</span><span class="sxs-lookup"><span data-stu-id="61198-398">Resource</span></span>

* <span data-ttu-id="61198-399">更改了 `group deployment export` 以在失败时显示部分模板和错误</span><span class="sxs-lookup"><span data-stu-id="61198-399">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="61198-400">角色</span><span class="sxs-lookup"><span data-stu-id="61198-400">Role</span></span>

* <span data-ttu-id="61198-401">添加了 `role assignment list-changelogs` 以允许审核服务主体角色</span><span class="sxs-lookup"><span data-stu-id="61198-401">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="61198-402">SQL</span><span class="sxs-lookup"><span data-stu-id="61198-402">SQL</span></span>

* <span data-ttu-id="61198-403">添加了在创建和更新时对数据库和弹性池的区域冗余支持</span><span class="sxs-lookup"><span data-stu-id="61198-403">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="61198-404">存储</span><span class="sxs-lookup"><span data-stu-id="61198-404">Storage</span></span>

* <span data-ttu-id="61198-405">已允许为 `storage blob [upload-batch|download-batch]` 指定 destination-path/prefix</span><span class="sxs-lookup"><span data-stu-id="61198-405">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="61198-406">VM</span><span class="sxs-lookup"><span data-stu-id="61198-406">VM</span></span>

* <span data-ttu-id="61198-407">添加了对在单个 VMSS 实例上附加/分离磁盘的支持</span><span class="sxs-lookup"><span data-stu-id="61198-407">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="61198-408">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="61198-408">February 13, 2018</span></span>

<span data-ttu-id="61198-409">版本 2.0.27</span><span class="sxs-lookup"><span data-stu-id="61198-409">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="61198-410">核心</span><span class="sxs-lookup"><span data-stu-id="61198-410">Core</span></span>

* <span data-ttu-id="61198-411">更改了同时根据订阅 ID 和在 MSI 登录名对密钥进行身份验证</span><span class="sxs-lookup"><span data-stu-id="61198-411">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="61198-412">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-412">ACS</span></span>

* <span data-ttu-id="61198-413">[重大更改] 为了提高准确性，已将 `aks get-versions` 重命名为 `aks get-upgrades`</span><span class="sxs-lookup"><span data-stu-id="61198-413">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="61198-414">更改了 `aks get-versions` 以显示可用于 `aks create` 的 Kubernetes 版本</span><span class="sxs-lookup"><span data-stu-id="61198-414">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="61198-415">更改了 `aks create` 默认值以允许服务器选择 Kubernetes 版本</span><span class="sxs-lookup"><span data-stu-id="61198-415">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="61198-416">更新了引用由 AKS 生成的服务主体的帮助消息</span><span class="sxs-lookup"><span data-stu-id="61198-416">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="61198-417">更改了 `aks create` 的默认节点大小，从“Standard\_D1\_v2”更改为“Standard\_DS1\_v2”</span><span class="sxs-lookup"><span data-stu-id="61198-417">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="61198-418">改进了定位 `az aks browse` 的仪表板 pod 时的可靠性</span><span class="sxs-lookup"><span data-stu-id="61198-418">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="61198-419">修复了 `aks get-credentials` 以便在加载 Kubernetes 配置文件时处理 Unicode 错误</span><span class="sxs-lookup"><span data-stu-id="61198-419">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="61198-420">向 `az aks install-cli` 添加了一条消息，以便帮助在 `$PATH` 中获取 `kubectl`</span><span class="sxs-lookup"><span data-stu-id="61198-420">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-421">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-421">Appservice</span></span>

* <span data-ttu-id="61198-422">修复了由于空引用 `webapp [backup|restore]` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="61198-422">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="61198-423">通过 `az configure --defaults appserviceplan=my-asp` 添加了对默认应用服务计划的支持</span><span class="sxs-lookup"><span data-stu-id="61198-423">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="61198-424">CDN</span><span class="sxs-lookup"><span data-stu-id="61198-424">CDN</span></span>

* <span data-ttu-id="61198-425">添加了 `cdn custom-domain [enable-https|disable-https]` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-425">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="61198-426">容器</span><span class="sxs-lookup"><span data-stu-id="61198-426">Container</span></span>

* <span data-ttu-id="61198-427">向 `az container logs` 添加了 `--follow` 选项，用于流式传输日志</span><span class="sxs-lookup"><span data-stu-id="61198-427">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="61198-428">添加了 `container attach` 命令，用于将本地标准输出和错误流附加到容器组中的容器</span><span class="sxs-lookup"><span data-stu-id="61198-428">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="61198-429">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="61198-429">CosmosDB</span></span>

* <span data-ttu-id="61198-430">添加了对设置功能的支持</span><span class="sxs-lookup"><span data-stu-id="61198-430">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="61198-431">分机</span><span class="sxs-lookup"><span data-stu-id="61198-431">Extension</span></span>

* <span data-ttu-id="61198-432">向 `az extension [add|update]` 命令添加了对 `--pip-proxy` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="61198-432">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="61198-433">向 `az extension [add|update]` 命令添加了对 `--pip-extra-index-urls` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="61198-433">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="61198-434">反馈</span><span class="sxs-lookup"><span data-stu-id="61198-434">Feedback</span></span>

* <span data-ttu-id="61198-435">将扩展信息添加到了遥测数据</span><span class="sxs-lookup"><span data-stu-id="61198-435">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="61198-436">交互</span><span class="sxs-lookup"><span data-stu-id="61198-436">Interactive</span></span>

* <span data-ttu-id="61198-437">修复了在 Cloud Shell 中使用交互模式时提示用户登录的问题</span><span class="sxs-lookup"><span data-stu-id="61198-437">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="61198-438">修复了缺少参数补全时的回归问题</span><span class="sxs-lookup"><span data-stu-id="61198-438">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="61198-439">IoT</span><span class="sxs-lookup"><span data-stu-id="61198-439">IoT</span></span>

* <span data-ttu-id="61198-440">修复了 `iot dps access policy [create|update]` 在成功时返回“not found”错误的问题</span><span class="sxs-lookup"><span data-stu-id="61198-440">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="61198-441">修复了 `iot dps linked-hub [create|update]` 在成功时返回“not found”错误的问题</span><span class="sxs-lookup"><span data-stu-id="61198-441">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="61198-442">向 `iot dps access policy [create|update]` 和 `iot dps linked-hub [create|update]` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="61198-442">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="61198-443">更改了 `iot hub create` 以允许指定分区数</span><span class="sxs-lookup"><span data-stu-id="61198-443">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="61198-444">监视</span><span class="sxs-lookup"><span data-stu-id="61198-444">Monitor</span></span>

* <span data-ttu-id="61198-445">修复了 `az monitor log-profiles create` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-445">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="61198-446">网络</span><span class="sxs-lookup"><span data-stu-id="61198-446">Network</span></span>

* <span data-ttu-id="61198-447">修复了以下命令的 `--tags` 选项：</span><span class="sxs-lookup"><span data-stu-id="61198-447">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="61198-448">配置文件</span><span class="sxs-lookup"><span data-stu-id="61198-448">Profile</span></span>

* <span data-ttu-id="61198-449">在交互模式中启用了 `az login`</span><span class="sxs-lookup"><span data-stu-id="61198-449">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="61198-450">资源</span><span class="sxs-lookup"><span data-stu-id="61198-450">Resource</span></span>

* <span data-ttu-id="61198-451">重新添加了 `feature show`</span><span class="sxs-lookup"><span data-stu-id="61198-451">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="61198-452">角色</span><span class="sxs-lookup"><span data-stu-id="61198-452">Role</span></span>

* <span data-ttu-id="61198-453">为 `ad app update` 添加了 `--available-to-other-tenants` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-453">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="61198-454">SQL</span><span class="sxs-lookup"><span data-stu-id="61198-454">SQL</span></span>

* <span data-ttu-id="61198-455">添加了 `sql server dns-alias` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-455">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="61198-456">添加了 `sql db rename`</span><span class="sxs-lookup"><span data-stu-id="61198-456">Added `sql db rename`</span></span>
* <span data-ttu-id="61198-457">向所有 sql 命令添加了对 `--ids` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="61198-457">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="61198-458">存储</span><span class="sxs-lookup"><span data-stu-id="61198-458">Storage</span></span>

* <span data-ttu-id="61198-459">添加了 `storage blob service-properties delete-policy` 和 `storage blob undelete` 命令以启用软删除</span><span class="sxs-lookup"><span data-stu-id="61198-459">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="61198-460">VM</span><span class="sxs-lookup"><span data-stu-id="61198-460">VM</span></span>

* <span data-ttu-id="61198-461">修复了无法完全初始化 VM 加密时出现的崩溃</span><span class="sxs-lookup"><span data-stu-id="61198-461">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="61198-462">添加了启用 MSI 时的主体 ID 输出</span><span class="sxs-lookup"><span data-stu-id="61198-462">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="61198-463">固定 `vm boot-diagnostics get-boot-log`</span><span class="sxs-lookup"><span data-stu-id="61198-463">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="61198-464">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="61198-464">January 31, 2018</span></span>

<span data-ttu-id="61198-465">版本 2.0.26</span><span class="sxs-lookup"><span data-stu-id="61198-465">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="61198-466">核心</span><span class="sxs-lookup"><span data-stu-id="61198-466">Core</span></span>

* <span data-ttu-id="61198-467">添加了支持在 MSI 上下文中检索原始令牌</span><span class="sxs-lookup"><span data-stu-id="61198-467">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="61198-468">删除了完成对 Windows cmd.exe 进行 LRO 操作后轮询指示器字符串</span><span class="sxs-lookup"><span data-stu-id="61198-468">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="61198-469">添加了将使用配置的默认值时显示的警告更改为信息级别条目。</span><span class="sxs-lookup"><span data-stu-id="61198-469">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="61198-470">请使用 `--verbose` 查看</span><span class="sxs-lookup"><span data-stu-id="61198-470">Use `--verbose` to see</span></span>
* <span data-ttu-id="61198-471">为等待命令添加了进度指示器</span><span class="sxs-lookup"><span data-stu-id="61198-471">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="61198-472">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-472">ACS</span></span>

* <span data-ttu-id="61198-473">说明了 `--disable-browser` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-473">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="61198-474">改进了 `--vm-size` 参数的 tab 键补全功能</span><span class="sxs-lookup"><span data-stu-id="61198-474">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-475">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-475">Appservice</span></span>

* <span data-ttu-id="61198-476">固定 `webapp log [tail|download]`</span><span class="sxs-lookup"><span data-stu-id="61198-476">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="61198-477">删除了对 Web 应用和函数的 `kind` 检查</span><span class="sxs-lookup"><span data-stu-id="61198-477">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="61198-478">CDN</span><span class="sxs-lookup"><span data-stu-id="61198-478">CDN</span></span>

* <span data-ttu-id="61198-479">修复了运行 `cdn custom-domain create` 时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="61198-479">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="61198-480">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="61198-480">CosmosDB</span></span>

* <span data-ttu-id="61198-481">修复了故障转移策略的参数说明</span><span class="sxs-lookup"><span data-stu-id="61198-481">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="61198-482">交互</span><span class="sxs-lookup"><span data-stu-id="61198-482">Interactive</span></span>

* <span data-ttu-id="61198-483">修复了不再显示命令选项补全的问题</span><span class="sxs-lookup"><span data-stu-id="61198-483">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="61198-484">网络</span><span class="sxs-lookup"><span data-stu-id="61198-484">Network</span></span>

* <span data-ttu-id="61198-485">向 `application-gateway create` 添加了对 `--cert-password` 的保护</span><span class="sxs-lookup"><span data-stu-id="61198-485">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="61198-486">修复了 `application-gateway update` 出现的 `--sku` 错误应用默认值的问题</span><span class="sxs-lookup"><span data-stu-id="61198-486">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="61198-487">向 `vpn-connection create` 添加了对 `--shared-key` 和 `--authorization-key` 的保护</span><span class="sxs-lookup"><span data-stu-id="61198-487">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="61198-488">修复了运行 `asg create` 时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="61198-488">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="61198-489">向 `dns zone export` 添加了用于导出名称的 `--file-name / -f` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-489">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="61198-490">修复了 `dns zone export` 存在的以下问题：</span><span class="sxs-lookup"><span data-stu-id="61198-490">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="61198-491">修复了未正确导出长 TXT 记录的问题</span><span class="sxs-lookup"><span data-stu-id="61198-491">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="61198-492">修复了不使用转义引号无法正确导出带引号的 TXT 记录的问题</span><span class="sxs-lookup"><span data-stu-id="61198-492">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="61198-493">修复了使用 `dns zone import` 某些记录会导入两次的问题</span><span class="sxs-lookup"><span data-stu-id="61198-493">Fixed issue where certain records were imported twice with `dns zone import`</span></span> 
* <span data-ttu-id="61198-494">已还原 `vnet-gateway root-cert` 和 `vnet-gateway revoked-cert` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-494">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="61198-495">配置文件</span><span class="sxs-lookup"><span data-stu-id="61198-495">Profile</span></span>

* <span data-ttu-id="61198-496">修复了 `get-access-token`，使其在 VM 中使用标识正常工作</span><span class="sxs-lookup"><span data-stu-id="61198-496">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="61198-497">资源</span><span class="sxs-lookup"><span data-stu-id="61198-497">Resource</span></span>

* <span data-ttu-id="61198-498">修复了 `deployment [create|validate]` 存在的 bug，即当模板的 type 字段包含大写值时错误地显示警告</span><span class="sxs-lookup"><span data-stu-id="61198-498">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="61198-499">存储</span><span class="sxs-lookup"><span data-stu-id="61198-499">Storage</span></span>

* <span data-ttu-id="61198-500">修复了将存储 V1 帐户迁移到存储 V2 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="61198-500">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="61198-501">为所有上传/下载命令添加了进度报告</span><span class="sxs-lookup"><span data-stu-id="61198-501">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="61198-502">修复了 `storage account check-name` 不显示“-n”参数选项的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-502">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>  
* <span data-ttu-id="61198-503">向 `blob [list|show]` 的表输出添加了“snapshot”列</span><span class="sxs-lookup"><span data-stu-id="61198-503">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="61198-504">修复了需要作为整数分析的各种参数的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-504">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="61198-505">VM</span><span class="sxs-lookup"><span data-stu-id="61198-505">VM</span></span>

* <span data-ttu-id="61198-506">添加了 `vm image accept-terms` 命令，以允许使用额外费用从映像创建 VM</span><span class="sxs-lookup"><span data-stu-id="61198-506">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="61198-507">修复了 `[vm|vmss create]`，以确保可以在使用未签名证书的代理下运行命令</span><span class="sxs-lookup"><span data-stu-id="61198-507">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="61198-508">[预览] 向 VMSS 添加了对“低”优先级的支持</span><span class="sxs-lookup"><span data-stu-id="61198-508">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="61198-509">向 `[vm|vmss] create` 添加了对 `--admin-password` 的保护</span><span class="sxs-lookup"><span data-stu-id="61198-509">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="61198-510">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="61198-510">January 17, 2018</span></span>

<span data-ttu-id="61198-511">版本 2.0.25</span><span class="sxs-lookup"><span data-stu-id="61198-511">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="61198-512">ACR</span><span class="sxs-lookup"><span data-stu-id="61198-512">ACR</span></span>

* <span data-ttu-id="61198-513">添加了发生 Windows 凭据错误时执行 acr 登录回退的功能</span><span class="sxs-lookup"><span data-stu-id="61198-513">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="61198-514">启用了注册表日志</span><span class="sxs-lookup"><span data-stu-id="61198-514">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="61198-515">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-515">ACS</span></span>

* <span data-ttu-id="61198-516">修复了 `get-credentials` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-516">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="61198-517">删除了 SPN 角色要求</span><span class="sxs-lookup"><span data-stu-id="61198-517">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-518">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-518">Appservice</span></span>

* <span data-ttu-id="61198-519">修复了 `hosting_environment_profile` 为 null 时 `config ssl upload` 存在的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-519">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="61198-520">为 `browse` 添加了自定义 URL 支持</span><span class="sxs-lookup"><span data-stu-id="61198-520">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="61198-521">修复了 `log tail` 的槽位支持</span><span class="sxs-lookup"><span data-stu-id="61198-521">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="61198-522">备份</span><span class="sxs-lookup"><span data-stu-id="61198-522">Backup</span></span>

* <span data-ttu-id="61198-523">将 `backup item list` 的 `--container-name` 选项更改为可选</span><span class="sxs-lookup"><span data-stu-id="61198-523">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="61198-524">为 `backup restore restore-disks` 添加了存储帐户选项</span><span class="sxs-lookup"><span data-stu-id="61198-524">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="61198-525">修复了 `backup protection enable-for-vm` 中的位置检查，使之区分大小写</span><span class="sxs-lookup"><span data-stu-id="61198-525">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="61198-526">修复了容器名称无效时命令失败的问题</span><span class="sxs-lookup"><span data-stu-id="61198-526">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="61198-527">已将 `backup item list` 更改为默认包含“Health Status”</span><span class="sxs-lookup"><span data-stu-id="61198-527">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="61198-528">Batch</span><span class="sxs-lookup"><span data-stu-id="61198-528">Batch</span></span>

* <span data-ttu-id="61198-529">已将 `batch login` 更改为返回身份验证详细信息</span><span class="sxs-lookup"><span data-stu-id="61198-529">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="61198-530">云</span><span class="sxs-lookup"><span data-stu-id="61198-530">Cloud</span></span>

* <span data-ttu-id="61198-531">已更改为在云中设置 `--profile` 时不需要终结点</span><span class="sxs-lookup"><span data-stu-id="61198-531">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="61198-532">消耗</span><span class="sxs-lookup"><span data-stu-id="61198-532">Consumption</span></span>

* <span data-ttu-id="61198-533">添加了用于保留的新命令：`consumption reservations summaries` 和 `consumption reservations details`</span><span class="sxs-lookup"><span data-stu-id="61198-533">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="61198-534">事件网格</span><span class="sxs-lookup"><span data-stu-id="61198-534">Event Grid</span></span>

* <span data-ttu-id="61198-535">[重大更改] 已将 `az eventgrid topic event-subscription` 命令变动为 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="61198-535">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="61198-536">[重大更改] 已将 `az eventgrid resource event-subscription` 命令变动为 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="61198-536">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="61198-537">[重大更改] 已删除 `eventgrid event-subscription show-endpoint-url` 命令。</span><span class="sxs-lookup"><span data-stu-id="61198-537">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="61198-538">请改用 `eventgrid event-subscription show --include-full-endpoint-url`</span><span class="sxs-lookup"><span data-stu-id="61198-538">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="61198-539">添加了命令 `eventgrid topic update`</span><span class="sxs-lookup"><span data-stu-id="61198-539">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="61198-540">添加了命令 `eventgrid event-subscription update`</span><span class="sxs-lookup"><span data-stu-id="61198-540">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="61198-541">为 `eventgrid topic` 命令添加了 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-541">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="61198-542">添加了主题名称的 Tab 键补全支持</span><span class="sxs-lookup"><span data-stu-id="61198-542">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="61198-543">交互</span><span class="sxs-lookup"><span data-stu-id="61198-543">Interactive</span></span>

* <span data-ttu-id="61198-544">修复了无法在 Python 2.x 中使用交互模式的问题</span><span class="sxs-lookup"><span data-stu-id="61198-544">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="61198-545">修复了启动时出错的问题</span><span class="sxs-lookup"><span data-stu-id="61198-545">Fixed errors on startup</span></span>
* <span data-ttu-id="61198-546">修复了无法在交互模式下运行某些命令的问题</span><span class="sxs-lookup"><span data-stu-id="61198-546">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="61198-547">IoT</span><span class="sxs-lookup"><span data-stu-id="61198-547">IoT</span></span>

* <span data-ttu-id="61198-548">添加了对设备预配服务的支持</span><span class="sxs-lookup"><span data-stu-id="61198-548">Added support for device provisioning service</span></span>
* <span data-ttu-id="61198-549">在命令和命令帮助中添加了弃用消息</span><span class="sxs-lookup"><span data-stu-id="61198-549">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="61198-550">添加了 IoT 检查，以告知用户有 IoT 扩展可用</span><span class="sxs-lookup"><span data-stu-id="61198-550">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="61198-551">监视</span><span class="sxs-lookup"><span data-stu-id="61198-551">Monitor</span></span>

* <span data-ttu-id="61198-552">添加了多诊断设置支持。</span><span class="sxs-lookup"><span data-stu-id="61198-552">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="61198-553">`az monitor diagnostic-settings create` 现在必需 `--name` 参数。</span><span class="sxs-lookup"><span data-stu-id="61198-553">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="61198-554">添加了命令 `monitor diagnostic-settings categories` 用于获取诊断设置类别</span><span class="sxs-lookup"><span data-stu-id="61198-554">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="61198-555">网络</span><span class="sxs-lookup"><span data-stu-id="61198-555">Network</span></span>

* <span data-ttu-id="61198-556">修复了使用 `vnet-gateway update` 进入/退出主动-待机模式时出现的问题</span><span class="sxs-lookup"><span data-stu-id="61198-556">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="61198-557">在 `application-gateway [create|update]` 中添加了对 HTTP2 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-557">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="61198-558">配置文件</span><span class="sxs-lookup"><span data-stu-id="61198-558">Profile</span></span>

* <span data-ttu-id="61198-559">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="61198-559">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="61198-560">角色</span><span class="sxs-lookup"><span data-stu-id="61198-560">Role</span></span>

* <span data-ttu-id="61198-561">为 `role assignment create` 添加了 `--assignee-object-id` 参数用于绕过图形查询</span><span class="sxs-lookup"><span data-stu-id="61198-561">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="61198-562">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="61198-562">Service Fabric</span></span>

* <span data-ttu-id="61198-563">在创建群集时生成的验证响应中添加了详细错误</span><span class="sxs-lookup"><span data-stu-id="61198-563">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="61198-564">修复了运行多个命令时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="61198-564">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="61198-565">VM</span><span class="sxs-lookup"><span data-stu-id="61198-565">VM</span></span>

* <span data-ttu-id="61198-566">[预览] `vmss` 的跨区域支持</span><span class="sxs-lookup"><span data-stu-id="61198-566">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="61198-567">[重大更改] 已将单区域 `vmss` 默认值更改为“Standard”负载均衡器</span><span class="sxs-lookup"><span data-stu-id="61198-567">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="61198-568">[重大更改] 已将EMSI 的 `externalIdentities` 更改为 `userAssignedIdentities`</span><span class="sxs-lookup"><span data-stu-id="61198-568">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="61198-569">[预览] 添加了 OS 磁盘交换支持</span><span class="sxs-lookup"><span data-stu-id="61198-569">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="61198-570">添加了使用其他订阅中的 VM 映像的支持</span><span class="sxs-lookup"><span data-stu-id="61198-570">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="61198-571">为 `[vm|vmss] create` 添加了 `--plan-name`、`--plan-product`、`--plan-promotion-code` 和 `--plan-publisher` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-571">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="61198-572">修复了 `[vm|vmss] create` 出错问题</span><span class="sxs-lookup"><span data-stu-id="61198-572">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="61198-573">修复了 `vm image list --all` 导致资源使用过度的问题</span><span class="sxs-lookup"><span data-stu-id="61198-573">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="61198-574">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="61198-574">December 19, 2017</span></span>

<span data-ttu-id="61198-575">版本 2.0.23</span><span class="sxs-lookup"><span data-stu-id="61198-575">Version 2.0.23</span></span>

* <span data-ttu-id="61198-576">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="61198-576">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="61198-577">容器</span><span class="sxs-lookup"><span data-stu-id="61198-577">Container</span></span>

* <span data-ttu-id="61198-578">纠正了容器日志参数的错误顺序</span><span class="sxs-lookup"><span data-stu-id="61198-578">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="61198-579">网络</span><span class="sxs-lookup"><span data-stu-id="61198-579">Network</span></span>

* <span data-ttu-id="61198-580">为 `route-table [create|update]` 添加了 `--disable-bgp-route-propagation` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-580">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="61198-581">为 `public-ip [create|update]` 添加了 `--ip-tags` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-581">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="61198-582">存储</span><span class="sxs-lookup"><span data-stu-id="61198-582">Storage</span></span>

* <span data-ttu-id="61198-583">添加了对存储 V2 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-583">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="61198-584">VM</span><span class="sxs-lookup"><span data-stu-id="61198-584">VM</span></span>

* <span data-ttu-id="61198-585">[预览] 添加了对 VM 和 VMSS 的用户分配标识的支持</span><span class="sxs-lookup"><span data-stu-id="61198-585">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="61198-586">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="61198-586">December 5, 2017</span></span>

<span data-ttu-id="61198-587">版本 2.0.22</span><span class="sxs-lookup"><span data-stu-id="61198-587">Version 2.0.22</span></span>

* <span data-ttu-id="61198-588">已删除 `az component` 命令。</span><span class="sxs-lookup"><span data-stu-id="61198-588">Removed `az component` commands.</span></span> <span data-ttu-id="61198-589">请改用 `az extension`</span><span class="sxs-lookup"><span data-stu-id="61198-589">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="61198-590">核心</span><span class="sxs-lookup"><span data-stu-id="61198-590">Core</span></span>
* <span data-ttu-id="61198-591">已将 `AZURE_US_GOV_CLOUD` AAD 颁发机构终结点从 login.microsoftonline.com 修改为 login.microsoftonline.us</span><span class="sxs-lookup"><span data-stu-id="61198-591">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="61198-592">已修复持续重新发送遥测数据的问题</span><span class="sxs-lookup"><span data-stu-id="61198-592">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="61198-593">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-593">ACS</span></span>

* <span data-ttu-id="61198-594">已添加 `aks install-connector` 和 `aks remove-connector` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-594">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="61198-595">已改进 `acs create` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="61198-595">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="61198-596">已修复不带完全限定路径的 `aks get-credentials -f` 的用法</span><span class="sxs-lookup"><span data-stu-id="61198-596">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="61198-597">顾问</span><span class="sxs-lookup"><span data-stu-id="61198-597">Advisor</span></span>

* <span data-ttu-id="61198-598">初始版本</span><span class="sxs-lookup"><span data-stu-id="61198-598">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-599">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-599">Appservice</span></span>

* <span data-ttu-id="61198-600">已修复使用 `webapp config ssl upload` 时的证书名称生成问题</span><span class="sxs-lookup"><span data-stu-id="61198-600">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="61198-601">已修复 `webapp [list|show]` 和 `functionapp [list|show]` 以显示正确的应用</span><span class="sxs-lookup"><span data-stu-id="61198-601">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="61198-602">已为 `WEBSITE_NODE_DEFAULT_VERSION` 添加了默认值</span><span class="sxs-lookup"><span data-stu-id="61198-602">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="61198-603">消耗</span><span class="sxs-lookup"><span data-stu-id="61198-603">Consumption</span></span>

* <span data-ttu-id="61198-604">已添加对 API 版本 2017-11-30 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-604">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="61198-605">容器</span><span class="sxs-lookup"><span data-stu-id="61198-605">Container</span></span>

* <span data-ttu-id="61198-606">已修复默认端口回归</span><span class="sxs-lookup"><span data-stu-id="61198-606">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="61198-607">监视</span><span class="sxs-lookup"><span data-stu-id="61198-607">Monitor</span></span>

* <span data-ttu-id="61198-608">已添加对指标命令的多维支持</span><span class="sxs-lookup"><span data-stu-id="61198-608">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="61198-609">资源</span><span class="sxs-lookup"><span data-stu-id="61198-609">Resource</span></span>

* <span data-ttu-id="61198-610">为 `resource show` 添加了 `--include-response-body` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-610">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="61198-611">角色</span><span class="sxs-lookup"><span data-stu-id="61198-611">Role</span></span>

* <span data-ttu-id="61198-612">已将“经典”管理员的默认分配显示添加到 `role assignment list`</span><span class="sxs-lookup"><span data-stu-id="61198-612">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="61198-613">已添加对 `ad sp reset-credentials` 的支持以便添加凭据而不是覆盖</span><span class="sxs-lookup"><span data-stu-id="61198-613">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="61198-614">已改进 `ad sp create-for-rbac` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="61198-614">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="61198-615">SQL</span><span class="sxs-lookup"><span data-stu-id="61198-615">SQL</span></span>

* <span data-ttu-id="61198-616">已添加 `sql db list-usages` 和 `sql db show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-616">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="61198-617">已添加 `sql server conn-policy show` 和 `sql server conn-policy update` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-617">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="61198-618">VM</span><span class="sxs-lookup"><span data-stu-id="61198-618">VM</span></span>

* <span data-ttu-id="61198-619">已对 `az vm list-skus` 添加区域信息</span><span class="sxs-lookup"><span data-stu-id="61198-619">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="61198-620">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="61198-620">November 14, 2017</span></span>

<span data-ttu-id="61198-621">版本 2.0.21</span><span class="sxs-lookup"><span data-stu-id="61198-621">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="61198-622">ACR</span><span class="sxs-lookup"><span data-stu-id="61198-622">ACR</span></span>

* <span data-ttu-id="61198-623">添加了在复制区域中创建 Webhook 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-623">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="61198-624">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-624">ACS</span></span>

* <span data-ttu-id="61198-625">已在 AKS 中将所有“代理”一词更改为“节点”</span><span class="sxs-lookup"><span data-stu-id="61198-625">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="61198-626">弃用了 `acs create` 的 `--orchestrator-release` 选项</span><span class="sxs-lookup"><span data-stu-id="61198-626">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="61198-627">已将 AKS 的默认 VM 大小更改为 `Standard_D1_v2`</span><span class="sxs-lookup"><span data-stu-id="61198-627">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="61198-628">在 Windows 上修复了 `az aks browse`</span><span class="sxs-lookup"><span data-stu-id="61198-628">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="61198-629">在 Windows 上修复了 `az aks get-credentials`</span><span class="sxs-lookup"><span data-stu-id="61198-629">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-630">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-630">Appservice</span></span>

* <span data-ttu-id="61198-631">添加了 Web 应用和函数应用的部署源 `config-zip`</span><span class="sxs-lookup"><span data-stu-id="61198-631">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="61198-632">为 `az webapp log config` 添加了 `--docker-container-logging` 选项</span><span class="sxs-lookup"><span data-stu-id="61198-632">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="61198-633">从 `az webapp log config` 的参数 `--web-server-logging` 中删除了 `storage` 选项</span><span class="sxs-lookup"><span data-stu-id="61198-633">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="61198-634">完善了 `deployment user set` 的错误消息</span><span class="sxs-lookup"><span data-stu-id="61198-634">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="61198-635">添加了创建 Linux 函数应用的支持</span><span class="sxs-lookup"><span data-stu-id="61198-635">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="61198-636">固定 `list-locations`</span><span class="sxs-lookup"><span data-stu-id="61198-636">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="61198-637">Batch</span><span class="sxs-lookup"><span data-stu-id="61198-637">Batch</span></span>

* <span data-ttu-id="61198-638">修复了在 pool create 命令中结合 `--image` 标志使用资源 ID 时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-638">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="61198-639">Batchai</span><span class="sxs-lookup"><span data-stu-id="61198-639">Batchai</span></span>

* <span data-ttu-id="61198-640">在 `file-server create` 命令中提供了 `--vm-size` 的简短选项 `-s`（提供 VM 大小）</span><span class="sxs-lookup"><span data-stu-id="61198-640">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="61198-641">为 `cluster create` 参数添加了存储帐户名称和密钥自变量</span><span class="sxs-lookup"><span data-stu-id="61198-641">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="61198-642">纠正了 `job list-files` 和 `job stream-file` 的文档</span><span class="sxs-lookup"><span data-stu-id="61198-642">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="61198-643">在 `job create` 命令中提供了 `--cluster-name` 的简短选项 `-r`（提供群集名称）</span><span class="sxs-lookup"><span data-stu-id="61198-643">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="61198-644">云</span><span class="sxs-lookup"><span data-stu-id="61198-644">Cloud</span></span>

* <span data-ttu-id="61198-645">更改了 `cloud [register|update]`，以防止注册缺少所需终结点的云</span><span class="sxs-lookup"><span data-stu-id="61198-645">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="61198-646">容器</span><span class="sxs-lookup"><span data-stu-id="61198-646">Container</span></span>

* <span data-ttu-id="61198-647">添加了打开多个端口的支持</span><span class="sxs-lookup"><span data-stu-id="61198-647">Added support to open multiple ports</span></span>
* <span data-ttu-id="61198-648">添加了容器组重启策略</span><span class="sxs-lookup"><span data-stu-id="61198-648">Added container group restart policy</span></span>
* <span data-ttu-id="61198-649">添加了将 Azure 文件共享装载为卷的支持</span><span class="sxs-lookup"><span data-stu-id="61198-649">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="61198-650">更新了帮助器文档</span><span class="sxs-lookup"><span data-stu-id="61198-650">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="61198-651">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="61198-651">Data Lake Analytics</span></span>

* <span data-ttu-id="61198-652">更改了 `[job|account] list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="61198-652">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="61198-653">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="61198-653">Data Lake Store</span></span>

* <span data-ttu-id="61198-654">更改了 `account list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="61198-654">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="61198-655">分机</span><span class="sxs-lookup"><span data-stu-id="61198-655">Extension</span></span>

* <span data-ttu-id="61198-656">添加了 `extension list-available` 用于列出官方的 Microsoft 扩展</span><span class="sxs-lookup"><span data-stu-id="61198-656">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="61198-657">为 `extension [add|update]` 添加了 `--name`，以便按名称安装扩展</span><span class="sxs-lookup"><span data-stu-id="61198-657">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="61198-658">IoT</span><span class="sxs-lookup"><span data-stu-id="61198-658">IoT</span></span>

* <span data-ttu-id="61198-659">添加了对证书颁发机构 (CA) 和证书链的支持</span><span class="sxs-lookup"><span data-stu-id="61198-659">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="61198-660">监视</span><span class="sxs-lookup"><span data-stu-id="61198-660">Monitor</span></span>

* <span data-ttu-id="61198-661">添加了 `activity-log alert` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-661">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="61198-662">网络</span><span class="sxs-lookup"><span data-stu-id="61198-662">Network</span></span>

* <span data-ttu-id="61198-663">添加了对 CAA DNS 记录的支持</span><span class="sxs-lookup"><span data-stu-id="61198-663">Added support for CAA DNS records</span></span>
* <span data-ttu-id="61198-664">修复了无法使用 `traffic-manager profile update` 更新终结点的问题</span><span class="sxs-lookup"><span data-stu-id="61198-664">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="61198-665">修复了在采用某种 VNET 创建方式时 `vnet update --dns-servers` 无法正常运行的问题</span><span class="sxs-lookup"><span data-stu-id="61198-665">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="61198-666">修复了 `dns zone import` 错误导入相对 DNS 名称的问题</span><span class="sxs-lookup"><span data-stu-id="61198-666">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="61198-667">保留</span><span class="sxs-lookup"><span data-stu-id="61198-667">Reservations</span></span>

* <span data-ttu-id="61198-668">初始预览版</span><span class="sxs-lookup"><span data-stu-id="61198-668">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="61198-669">资源</span><span class="sxs-lookup"><span data-stu-id="61198-669">Resource</span></span>

* <span data-ttu-id="61198-670">添加了在 `--resource` 参数中指定资源 ID 的支持，以及对资源级锁的支持</span><span class="sxs-lookup"><span data-stu-id="61198-670">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="61198-671">SQL</span><span class="sxs-lookup"><span data-stu-id="61198-671">SQL</span></span>

* <span data-ttu-id="61198-672">为 `sql server vnet-rule [create|update]` 添加了 `--ignore-missing-vnet-service-endpoint` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-672">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="61198-673">存储</span><span class="sxs-lookup"><span data-stu-id="61198-673">Storage</span></span>

* <span data-ttu-id="61198-674">更改了 `storage account create` 以使用 SKU `Standard_RAGRS` 作为默认值</span><span class="sxs-lookup"><span data-stu-id="61198-674">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="61198-675">修复了处理包含非 ASCII 字符的文件/Blob 名称时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-675">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="61198-676">修复了阻止在 `storage [blob|file] copy start-batch` 中使用 `--source-uri` 的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-676">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="61198-677">添加了在 `storage [blob|file] delete-batch` 中包含和删除多个对象的命令</span><span class="sxs-lookup"><span data-stu-id="61198-677">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="61198-678">修复了使用 `storage metrics update` 启用指标时出现的问题</span><span class="sxs-lookup"><span data-stu-id="61198-678">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="61198-679">修复了使用 `storage blob upload-batch` 时，如果文件超过 200GB 所出现的问题</span><span class="sxs-lookup"><span data-stu-id="61198-679">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="61198-680">修复了 `storage account [create|update]` 忽略 `--bypass` 和 `--default-action` 的问题</span><span class="sxs-lookup"><span data-stu-id="61198-680">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="61198-681">VM</span><span class="sxs-lookup"><span data-stu-id="61198-681">VM</span></span>

* <span data-ttu-id="61198-682">修复了 `vmss create` 阻止使用 `Basic` 大小层的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-682">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="61198-683">针对包含计费信息的自定义映像，为 `[vm|vmss] create` 添加了 `--plan` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-683">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="61198-684">添加了 `vm secret `[add|remove|list]\` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-684">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="61198-685">已将 `vm format-secret` 重命名为 `vm secret format`</span><span class="sxs-lookup"><span data-stu-id="61198-685">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="61198-686">为 `vm encryption enable` 添加了 `--encrypt format` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-686">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="61198-687">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="61198-687">October 24, 2017</span></span>

<span data-ttu-id="61198-688">版本 2.0.20</span><span class="sxs-lookup"><span data-stu-id="61198-688">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="61198-689">核心</span><span class="sxs-lookup"><span data-stu-id="61198-689">Core</span></span>

* <span data-ttu-id="61198-690">已更新 `2017-03-09-profile` 以使用 `MGMT_STORAGE` API 版本 `2016-01-01`</span><span class="sxs-lookup"><span data-stu-id="61198-690">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="61198-691">ACR</span><span class="sxs-lookup"><span data-stu-id="61198-691">ACR</span></span>

* <span data-ttu-id="61198-692">已更新资源管理以指向 `2017-10-01` API 版本</span><span class="sxs-lookup"><span data-stu-id="61198-692">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="61198-693">已将“带来你自己的存储”SKU 更改为“经典”</span><span class="sxs-lookup"><span data-stu-id="61198-693">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="61198-694">已将注册表 SKU 重命名为“基本”、“标准”和“高级”</span><span class="sxs-lookup"><span data-stu-id="61198-694">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="61198-695">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-695">ACS</span></span>

* <span data-ttu-id="61198-696">[PREVIEW] 添加了 `az aks` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-696">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="61198-697">已修复 Kubernetes `get-credentials`</span><span class="sxs-lookup"><span data-stu-id="61198-697">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-698">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-698">Appservice</span></span>

* <span data-ttu-id="61198-699">已修复所下载 `webapp` 日志可能无效的问题</span><span class="sxs-lookup"><span data-stu-id="61198-699">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="61198-700">组件</span><span class="sxs-lookup"><span data-stu-id="61198-700">Component</span></span>

* <span data-ttu-id="61198-701">为所有安装程序添加了更清晰的弃用消息并添加了确认提示</span><span class="sxs-lookup"><span data-stu-id="61198-701">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="61198-702">监视</span><span class="sxs-lookup"><span data-stu-id="61198-702">Monitor</span></span>

* <span data-ttu-id="61198-703">添加了 `action-group` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-703">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="61198-704">资源</span><span class="sxs-lookup"><span data-stu-id="61198-704">Resource</span></span>

* <span data-ttu-id="61198-705">修复了 `group export` 中与 msrest 依赖项的最新版本不兼容的问题</span><span class="sxs-lookup"><span data-stu-id="61198-705">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="61198-706">修复了 `policy assignment create` 以使用内置策略定义和策略集定义</span><span class="sxs-lookup"><span data-stu-id="61198-706">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="61198-707">VM</span><span class="sxs-lookup"><span data-stu-id="61198-707">VM</span></span>

* <span data-ttu-id="61198-708">为 `vmss create` 添加了 `--accelerated-networking` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-708">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="61198-709">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="61198-709">October 9, 2017</span></span>

<span data-ttu-id="61198-710">版本 2.0.19</span><span class="sxs-lookup"><span data-stu-id="61198-710">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="61198-711">核心</span><span class="sxs-lookup"><span data-stu-id="61198-711">Core</span></span>

* <span data-ttu-id="61198-712">在 Azure Stack 中添加了一个尾随斜杠用于处理 ADFS 机构 URL</span><span class="sxs-lookup"><span data-stu-id="61198-712">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-713">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-713">Appservice</span></span>

* <span data-ttu-id="61198-714">添加了新命令 `webapp update` 用于执行常规更新</span><span class="sxs-lookup"><span data-stu-id="61198-714">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="61198-715">Batch</span><span class="sxs-lookup"><span data-stu-id="61198-715">Batch</span></span>

* <span data-ttu-id="61198-716">已更新为 Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="61198-716">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="61198-717">更新了 VirtualMachineConfiguration 的 `--image`，用于支持除 publish:offer:sku:version 以外的 ARM 映像引用</span><span class="sxs-lookup"><span data-stu-id="61198-717">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="61198-718">添加了对 Batch 扩展命令新 CLI 扩展模型的支持</span><span class="sxs-lookup"><span data-stu-id="61198-718">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="61198-719">从组件模型中删除了 Batch 支持</span><span class="sxs-lookup"><span data-stu-id="61198-719">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="61198-720">Batchai</span><span class="sxs-lookup"><span data-stu-id="61198-720">Batchai</span></span>

* <span data-ttu-id="61198-721">Batch AI 模块初始版本</span><span class="sxs-lookup"><span data-stu-id="61198-721">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="61198-722">KeyVault</span><span class="sxs-lookup"><span data-stu-id="61198-722">Keyvault</span></span>

* <span data-ttu-id="61198-723">修复了在 Azure Stack 中使用 ADFS 时发生的 Key Vault 身份验证问题。</span><span class="sxs-lookup"><span data-stu-id="61198-723">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="61198-724">(#4448)</span><span class="sxs-lookup"><span data-stu-id="61198-724">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="61198-725">网络</span><span class="sxs-lookup"><span data-stu-id="61198-725">Network</span></span>

* <span data-ttu-id="61198-726">已将 `application-gateway address-pool create` 的 `--server` 参数更改为可选，以允许空地址池</span><span class="sxs-lookup"><span data-stu-id="61198-726">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="61198-727">更新了 `traffic-manager` 以支持最新功能</span><span class="sxs-lookup"><span data-stu-id="61198-727">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="61198-728">资源</span><span class="sxs-lookup"><span data-stu-id="61198-728">Resource</span></span>

* <span data-ttu-id="61198-729">在 `group` 中添加了对资源组名称使用 `--resource-group/-g` 选项的支持</span><span class="sxs-lookup"><span data-stu-id="61198-729">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="61198-730">为 `account lock` 添加了命令用于处理订阅级锁</span><span class="sxs-lookup"><span data-stu-id="61198-730">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="61198-731">为 `group lock` 添加了命令用于处理组级锁</span><span class="sxs-lookup"><span data-stu-id="61198-731">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="61198-732">为 `resource lock` 添加了命令用于处理资源级锁</span><span class="sxs-lookup"><span data-stu-id="61198-732">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="61198-733">Sql</span><span class="sxs-lookup"><span data-stu-id="61198-733">Sql</span></span>

* <span data-ttu-id="61198-734">添加了 SQL 透明数据加密 (TDE) 和自带密钥 TDE 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-734">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="61198-735">添加了 `db list-deleted` 命令和 `db restore --deleted-time` 参数，以便能够找到和还原已删除的数据库</span><span class="sxs-lookup"><span data-stu-id="61198-735">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="61198-736">添加了 `db op list` 和 `db op cancel`，以便能够列出和取消正在对数据库执行的操作</span><span class="sxs-lookup"><span data-stu-id="61198-736">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="61198-737">存储</span><span class="sxs-lookup"><span data-stu-id="61198-737">Storage</span></span>

* <span data-ttu-id="61198-738">添加了对文件共享快照的支持</span><span class="sxs-lookup"><span data-stu-id="61198-738">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="61198-739">Vm</span><span class="sxs-lookup"><span data-stu-id="61198-739">Vm</span></span>

* <span data-ttu-id="61198-740">修复了 `vm show` 中的一个 bug：在缺少专用 IP 地址的情况下使用 `-d` 会导致崩溃</span><span class="sxs-lookup"><span data-stu-id="61198-740">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="61198-741">[预览] 添加了滚动升级到 `vmss create` 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-741">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="61198-742">添加了使用 `vm encryption enable` 更新加密设置的支持</span><span class="sxs-lookup"><span data-stu-id="61198-742">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="61198-743">为 `vm create` 添加了 `--os-disk-size-gb` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-743">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="61198-744">为 Windows 中的 `vmss create` 添加了 `--license-type` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-744">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="61198-745">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="61198-745">September 22, 2017</span></span>

<span data-ttu-id="61198-746">版本 2.0.18</span><span class="sxs-lookup"><span data-stu-id="61198-746">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="61198-747">资源</span><span class="sxs-lookup"><span data-stu-id="61198-747">Resource</span></span>

* <span data-ttu-id="61198-748">添加了对显示内置策略定义的支持</span><span class="sxs-lookup"><span data-stu-id="61198-748">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="61198-749">添加了用于创建策略定义的支持模式参数</span><span class="sxs-lookup"><span data-stu-id="61198-749">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="61198-750">为 `managedapp definition create` 添加了对 UI 定义和模板的支持</span><span class="sxs-lookup"><span data-stu-id="61198-750">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="61198-751">[重大更改] 已将 `managedapp` 资源类型从 `appliances` 更改到 `applications`，从 `applianceDefinitions` 更改到 `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="61198-751">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="61198-752">网络</span><span class="sxs-lookup"><span data-stu-id="61198-752">Network</span></span>

* <span data-ttu-id="61198-753">为 `network lb` 和 `network public-ip` 子命令添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="61198-753">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="61198-754">为 `express-route` 添加了对 IPv6 Microsoft 对等互连的支持</span><span class="sxs-lookup"><span data-stu-id="61198-754">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="61198-755">添加了 `asg` 应用程序安全组命令</span><span class="sxs-lookup"><span data-stu-id="61198-755">Added `asg` application security group commands</span></span>
* <span data-ttu-id="61198-756">为 `nic [create|ip-config create|ip-config update]` 添加了 `--application-security-groups` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-756">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="61198-757">为 `nsg rule [create|update]` 添加了 `--source-asgs` 和 `--destination-asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-757">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="61198-758">为 `vnet [create|update]` 添加了 `--ddos-protection` 和 `--vm-protection` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-758">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="61198-759">添加了 `network [vnet-gateway|vpn-client|show-url]` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-759">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="61198-760">存储</span><span class="sxs-lookup"><span data-stu-id="61198-760">Storage</span></span>

* <span data-ttu-id="61198-761">已修复了 `storage account network-rule` 命令在更新 SDK 后可能会失败的问题</span><span class="sxs-lookup"><span data-stu-id="61198-761">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="61198-762">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="61198-762">Eventgrid</span></span>

* <span data-ttu-id="61198-763">更新了 Azure 事件网格 Python SDK 以使用较新的 API 版本“2017-09-15-preview”</span><span class="sxs-lookup"><span data-stu-id="61198-763">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="61198-764">SQL</span><span class="sxs-lookup"><span data-stu-id="61198-764">SQL</span></span>

* <span data-ttu-id="61198-765">将 `sql server list` 的参数 `--resource-group` 更改为可选。</span><span class="sxs-lookup"><span data-stu-id="61198-765">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="61198-766">如果未指定，将返回订阅中的所有 SQL 服务器</span><span class="sxs-lookup"><span data-stu-id="61198-766">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="61198-767">为 `db [create|copy|restore|update|replica create|create|update]` 和 `dw [create|update]` 添加了 `--no-wait` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-767">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="61198-768">KeyVault</span><span class="sxs-lookup"><span data-stu-id="61198-768">Keyvault</span></span>

* <span data-ttu-id="61198-769">添加了对从代理后执行 Keyvault 命令的支持</span><span class="sxs-lookup"><span data-stu-id="61198-769">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="61198-770">VM</span><span class="sxs-lookup"><span data-stu-id="61198-770">VM</span></span>

* <span data-ttu-id="61198-771">为 `[vm|vmss|disk] create` 添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="61198-771">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="61198-772">已修复了将 `--app-gateway ID` 与 `vmss create` 一起使用会导致故障的问题</span><span class="sxs-lookup"><span data-stu-id="61198-772">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="61198-773">为 `vm create` 添加了 `--asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-773">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="61198-774">添加了对使用 `vm run-command` 在 VM 上运行命令的支持</span><span class="sxs-lookup"><span data-stu-id="61198-774">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="61198-775">[预览] 添加了对使用 `vmss encryption` 进行 VMSS 磁盘加密的支持</span><span class="sxs-lookup"><span data-stu-id="61198-775">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="61198-776">添加了对使用 `vm perform-maintenance` 在 VM 上执行维护的支持</span><span class="sxs-lookup"><span data-stu-id="61198-776">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="61198-777">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-777">ACS</span></span>

* <span data-ttu-id="61198-778">[预览] 为适用于 ACS 预览区域的 `acs create` 添加了 `--orchestrator-release` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-778">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-779">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-779">Appservice</span></span>

* <span data-ttu-id="61198-780">添加了使用 `webapp auth [update|show]` 更新和显示身份验证设置的功能</span><span class="sxs-lookup"><span data-stu-id="61198-780">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="61198-781">备份</span><span class="sxs-lookup"><span data-stu-id="61198-781">Backup</span></span>

* <span data-ttu-id="61198-782">预览版</span><span class="sxs-lookup"><span data-stu-id="61198-782">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="61198-783">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="61198-783">September 11, 2017</span></span>

<span data-ttu-id="61198-784">版本 2.0.17</span><span class="sxs-lookup"><span data-stu-id="61198-784">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="61198-785">核心</span><span class="sxs-lookup"><span data-stu-id="61198-785">Core</span></span>

* <span data-ttu-id="61198-786">启用了命令模块在遥测中设置其自己的相关 ID</span><span class="sxs-lookup"><span data-stu-id="61198-786">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="61198-787">修复了在遥测设置为诊断模式时的 JSON 转储问题</span><span class="sxs-lookup"><span data-stu-id="61198-787">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="61198-788">Acs</span><span class="sxs-lookup"><span data-stu-id="61198-788">Acs</span></span>

* <span data-ttu-id="61198-789">添加了 `acs list-locations` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-789">Added `acs list-locations` command</span></span>
* <span data-ttu-id="61198-790">使 `ssh-key-file` 附带预期的默认值</span><span class="sxs-lookup"><span data-stu-id="61198-790">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-791">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-791">Appservice</span></span>

* <span data-ttu-id="61198-792">添加了在未包含活动服务计划的资源组中创建 Web 应用的功能</span><span class="sxs-lookup"><span data-stu-id="61198-792">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="61198-793">CDN</span><span class="sxs-lookup"><span data-stu-id="61198-793">CDN</span></span>

* <span data-ttu-id="61198-794">修复了 `cdn custom-domain create` 的“CustomDomain is not interable”bug</span><span class="sxs-lookup"><span data-stu-id="61198-794">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="61198-795">分机</span><span class="sxs-lookup"><span data-stu-id="61198-795">Extension</span></span>

* <span data-ttu-id="61198-796">初始版本</span><span class="sxs-lookup"><span data-stu-id="61198-796">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="61198-797">KeyVault</span><span class="sxs-lookup"><span data-stu-id="61198-797">Keyvault</span></span>

* <span data-ttu-id="61198-798">为 `keyvault set-policy` 修复了权限区分大小写的问题</span><span class="sxs-lookup"><span data-stu-id="61198-798">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="61198-799">网络</span><span class="sxs-lookup"><span data-stu-id="61198-799">Network</span></span>

* <span data-ttu-id="61198-800">已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="61198-800">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="61198-801">已为 `vnet subnet create/update` 将 `--private-access-services` 参数重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="61198-801">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="61198-802">在 `nsg rule create/update` 中添加了对多个 IP 范围和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="61198-802">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="61198-803">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-803">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="61198-804">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-804">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="61198-805">资源</span><span class="sxs-lookup"><span data-stu-id="61198-805">Resource</span></span>

* <span data-ttu-id="61198-806">允许在 `policy definition create` 和 `policy definition update` 中传入资源策略参数定义</span><span class="sxs-lookup"><span data-stu-id="61198-806">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="61198-807">允许为 `policy assignment create` 传入参数值</span><span class="sxs-lookup"><span data-stu-id="61198-807">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="61198-808">允许为所有参数传入 JSON 或文件</span><span class="sxs-lookup"><span data-stu-id="61198-808">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="61198-809">更新了 API 版本</span><span class="sxs-lookup"><span data-stu-id="61198-809">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="61198-810">SQL</span><span class="sxs-lookup"><span data-stu-id="61198-810">SQL</span></span>

* <span data-ttu-id="61198-811">添加了 `sql server vnet-rule` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-811">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="61198-812">VM</span><span class="sxs-lookup"><span data-stu-id="61198-812">VM</span></span>

* <span data-ttu-id="61198-813">已修复：除非提供 `--scope`，否则不分配访问权限</span><span class="sxs-lookup"><span data-stu-id="61198-813">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="61198-814">已修复：使用与门户相同的扩展命名</span><span class="sxs-lookup"><span data-stu-id="61198-814">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="61198-815">已从 `[vm|vmss] create` 输出中删除了 `subscription`</span><span class="sxs-lookup"><span data-stu-id="61198-815">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="61198-816">已修复：`[vm|vmss] create` SKU 无法应用于带映像的数据磁盘</span><span class="sxs-lookup"><span data-stu-id="61198-816">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="61198-817">已修复：`vm format-secret --secrets` 不接受新行分隔的 ID</span><span class="sxs-lookup"><span data-stu-id="61198-817">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="61198-818">2017 年 8 月31 日</span><span class="sxs-lookup"><span data-stu-id="61198-818">August 31, 2017</span></span>

<span data-ttu-id="61198-819">版本 2.0.16</span><span class="sxs-lookup"><span data-stu-id="61198-819">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="61198-820">KeyVault</span><span class="sxs-lookup"><span data-stu-id="61198-820">Keyvault</span></span>

* <span data-ttu-id="61198-821">修复了在尝试使用 `secret download` 自动解析机密编码时的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-821">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="61198-822">Sf</span><span class="sxs-lookup"><span data-stu-id="61198-822">Sf</span></span>

* <span data-ttu-id="61198-823">弃用所有支持 Service Fabric CLI (sfctl) 的命令</span><span class="sxs-lookup"><span data-stu-id="61198-823">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="61198-824">存储</span><span class="sxs-lookup"><span data-stu-id="61198-824">Storage</span></span>

* <span data-ttu-id="61198-825">修复了无法在不支持 NetworkACLs 功能的区域中创建存储帐户的问题</span><span class="sxs-lookup"><span data-stu-id="61198-825">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="61198-826">在 Blob 和文件上载过程中确定内容类型和内容编码（如果既未指定内容类型，也未指定内容编码）</span><span class="sxs-lookup"><span data-stu-id="61198-826">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="61198-827">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="61198-827">August 28, 2017</span></span>

<span data-ttu-id="61198-828">版本 2.0.15</span><span class="sxs-lookup"><span data-stu-id="61198-828">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="61198-829">CLI</span><span class="sxs-lookup"><span data-stu-id="61198-829">CLI</span></span>

* <span data-ttu-id="61198-830">在 `--version` 中添加了法律说明</span><span class="sxs-lookup"><span data-stu-id="61198-830">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="61198-831">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-831">ACS</span></span>

* <span data-ttu-id="61198-832">更正了预览区域</span><span class="sxs-lookup"><span data-stu-id="61198-832">Corrected preview regions</span></span>
* <span data-ttu-id="61198-833">正确设置了默认 `dns_name_prefix` 的格式</span><span class="sxs-lookup"><span data-stu-id="61198-833">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="61198-834">优化了 acs 命令输出</span><span class="sxs-lookup"><span data-stu-id="61198-834">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-835">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-835">Appservice</span></span>

* <span data-ttu-id="61198-836">[重大更改] 修复了 `az webapp config appsettings [delete|set]` 输出中的不一致</span><span class="sxs-lookup"><span data-stu-id="61198-836">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="61198-837">为 `az webapp config container set --docker-custom-image-name` 的 `-i` 添加了新别名</span><span class="sxs-lookup"><span data-stu-id="61198-837">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="61198-838">公开了 `az webapp log show`</span><span class="sxs-lookup"><span data-stu-id="61198-838">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="61198-839">公开了 `az webapp delete` 中的新参数，用于保留应用服务计划、指标或 dns 注册</span><span class="sxs-lookup"><span data-stu-id="61198-839">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="61198-840">已修复：正确检测槽位设置</span><span class="sxs-lookup"><span data-stu-id="61198-840">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="61198-841">IoT</span><span class="sxs-lookup"><span data-stu-id="61198-841">IoT</span></span>

* <span data-ttu-id="61198-842">修复了 #3934：策略创建操作不再清除现有的策略</span><span class="sxs-lookup"><span data-stu-id="61198-842">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="61198-843">网络</span><span class="sxs-lookup"><span data-stu-id="61198-843">Network</span></span>

* <span data-ttu-id="61198-844">[重大更改] 已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="61198-844">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="61198-845">[重大更改] 已将 `vnet subnet [create|update]` 的选项 `--private-access-services` 重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="61198-845">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="61198-846">在 `nsg rule [create|update]` 中添加了对多个 IP 和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="61198-846">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="61198-847">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-847">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="61198-848">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-848">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="61198-849">配置文件</span><span class="sxs-lookup"><span data-stu-id="61198-849">Profile</span></span>

* <span data-ttu-id="61198-850">公开了 `--msi` 和 `--msi-port`，以便使用虚拟机的标识登录</span><span class="sxs-lookup"><span data-stu-id="61198-850">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="61198-851">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="61198-851">Service Fabric</span></span>

* <span data-ttu-id="61198-852">预览版</span><span class="sxs-lookup"><span data-stu-id="61198-852">Preview release</span></span>
* <span data-ttu-id="61198-853">简化了命令的注册表用户/密码规则</span><span class="sxs-lookup"><span data-stu-id="61198-853">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="61198-854">修复了即使在参数中传入了密码，也提示用户输入密码的问题</span><span class="sxs-lookup"><span data-stu-id="61198-854">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="61198-855">添加了对空 `registry_cred` 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-855">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="61198-856">存储</span><span class="sxs-lookup"><span data-stu-id="61198-856">Storage</span></span>

* <span data-ttu-id="61198-857">启用了设置 Blob 层</span><span class="sxs-lookup"><span data-stu-id="61198-857">Enabled setting blob tier</span></span>
* <span data-ttu-id="61198-858">为 `storage account [create|update]` 添加了 `--bypass` 和 `--default-action` 参数用于支持服务隧道</span><span class="sxs-lookup"><span data-stu-id="61198-858">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="61198-859">添加了用于在 `storage account network-rule` 中添加 VNET 规则和基于 IP 的规则的命令</span><span class="sxs-lookup"><span data-stu-id="61198-859">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="61198-860">启用了使用客户管理的密钥进行服务加密的功能</span><span class="sxs-lookup"><span data-stu-id="61198-860">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="61198-861">[重大更改] 已将 `az storage account create and az storage account update` 命令的选项 `--encryption` 重命名为 `--encryption-services`</span><span class="sxs-lookup"><span data-stu-id="61198-861">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="61198-862">修复了 #4220：`az storage account update encryption` - 语法不匹配</span><span class="sxs-lookup"><span data-stu-id="61198-862">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="61198-863">VM</span><span class="sxs-lookup"><span data-stu-id="61198-863">VM</span></span>

* <span data-ttu-id="61198-864">修复了使用 `--instance-id *` 时，针对 `vmss get-instance-view` 显示多余且错误的信息的问题</span><span class="sxs-lookup"><span data-stu-id="61198-864">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="61198-865">在 `vmss create` 中添加了对 `--lb-sku` 的支持：</span><span class="sxs-lookup"><span data-stu-id="61198-865">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="61198-866">从 `[vm|vmss] create` 的管理员名称方块列表中删除了人员名称</span><span class="sxs-lookup"><span data-stu-id="61198-866">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="61198-867">修复了当无法从映像中提取计划信息时，`[vm|vmss] create` 引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="61198-867">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="61198-868">修复了创建包含内部 LB 的 vmms 规模集时发生崩溃的问题</span><span class="sxs-lookup"><span data-stu-id="61198-868">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="61198-869">修复了 `--no-wait` 参数无法配合 `vm availability-set create` 工作的问题</span><span class="sxs-lookup"><span data-stu-id="61198-869">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="61198-870">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="61198-870">August 15, 2017</span></span>

<span data-ttu-id="61198-871">版本 2.0.14</span><span class="sxs-lookup"><span data-stu-id="61198-871">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="61198-872">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-872">ACS</span></span>

* <span data-ttu-id="61198-873">更正了 kubernetes 的 sshMaster0 端口号</span><span class="sxs-lookup"><span data-stu-id="61198-873">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-874">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-874">Appservice</span></span>

* <span data-ttu-id="61198-875">修复了创建基于新 Git 的 Linux Web 应用时发生异常的问题</span><span class="sxs-lookup"><span data-stu-id="61198-875">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="61198-876">事件网格</span><span class="sxs-lookup"><span data-stu-id="61198-876">Event Grid</span></span>

* <span data-ttu-id="61198-877">添加了 SDK 依赖项</span><span class="sxs-lookup"><span data-stu-id="61198-877">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="61198-878">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="61198-878">August 11, 2017</span></span>

<span data-ttu-id="61198-879">版本 2.0.13</span><span class="sxs-lookup"><span data-stu-id="61198-879">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="61198-880">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-880">ACS</span></span>

* <span data-ttu-id="61198-881">添加了更多预览区域</span><span class="sxs-lookup"><span data-stu-id="61198-881">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="61198-882">Batch</span><span class="sxs-lookup"><span data-stu-id="61198-882">Batch</span></span>

* <span data-ttu-id="61198-883">已更新到 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="61198-883">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="61198-884">添加了新命令用于显示作业的任务计数</span><span class="sxs-lookup"><span data-stu-id="61198-884">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="61198-885">修复了处理资源文件 SAS URL 时的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-885">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="61198-886">Batch 帐户终结点现在支持可选的“https://” 前缀</span><span class="sxs-lookup"><span data-stu-id="61198-886">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="61198-887">支持将包含 100 多个任务的列表添加到作业</span><span class="sxs-lookup"><span data-stu-id="61198-887">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="61198-888">添加了加载扩展命令模块的调试日志记录</span><span class="sxs-lookup"><span data-stu-id="61198-888">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="61198-889">组件</span><span class="sxs-lookup"><span data-stu-id="61198-889">Component</span></span>

* <span data-ttu-id="61198-890">为“az component”命令添加了弃用警告</span><span class="sxs-lookup"><span data-stu-id="61198-890">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="61198-891">容器</span><span class="sxs-lookup"><span data-stu-id="61198-891">Container</span></span>

* <span data-ttu-id="61198-892">`create`：修复了某个环境变量中不允许等于号的问题</span><span class="sxs-lookup"><span data-stu-id="61198-892">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="61198-893">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="61198-893">Data Lake Store</span></span>

* <span data-ttu-id="61198-894">启用了进度控件</span><span class="sxs-lookup"><span data-stu-id="61198-894">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="61198-895">事件网格</span><span class="sxs-lookup"><span data-stu-id="61198-895">Event Grid</span></span>

* <span data-ttu-id="61198-896">初始版本</span><span class="sxs-lookup"><span data-stu-id="61198-896">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="61198-897">网络</span><span class="sxs-lookup"><span data-stu-id="61198-897">Network</span></span>

* <span data-ttu-id="61198-898">`lb`：修复了某些子资源名称在省略时无法正确解析的问题</span><span class="sxs-lookup"><span data-stu-id="61198-898">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="61198-899">`application-gateway {subresource} delete`：修复了不遵循 `--no-wait` 的问题</span><span class="sxs-lookup"><span data-stu-id="61198-899">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="61198-900">`application-gateway http-settings update`：修复了无法关闭 `--connection-draining-timeout` 的问题</span><span class="sxs-lookup"><span data-stu-id="61198-900">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="61198-901">修复了 `az network vpn-connection ipsec-policy add` 包含意外关键字参数 `sa_data_size_kilobyes` 的错误</span><span class="sxs-lookup"><span data-stu-id="61198-901">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="61198-902">配置文件</span><span class="sxs-lookup"><span data-stu-id="61198-902">Profile</span></span>

* <span data-ttu-id="61198-903">`account list`：添加了 `--refresh` 用于从服务器同步最新订阅</span><span class="sxs-lookup"><span data-stu-id="61198-903">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="61198-904">存储</span><span class="sxs-lookup"><span data-stu-id="61198-904">Storage</span></span>

* <span data-ttu-id="61198-905">启用了使用系统分配的标识更新存储帐户的功能</span><span class="sxs-lookup"><span data-stu-id="61198-905">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="61198-906">VM</span><span class="sxs-lookup"><span data-stu-id="61198-906">VM</span></span>

* <span data-ttu-id="61198-907">`availability-set`：公开了转换时的容错域计数</span><span class="sxs-lookup"><span data-stu-id="61198-907">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="61198-908">公开了 `list-skus` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-908">Exposed `list-skus` command</span></span>
* <span data-ttu-id="61198-909">支持在不创建角色分配的情况下分配标识</span><span class="sxs-lookup"><span data-stu-id="61198-909">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="61198-910">附加数据磁盘时应用存储 SKU</span><span class="sxs-lookup"><span data-stu-id="61198-910">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="61198-911">删除了使用托管磁盘时的默认 OS 磁盘名称和存储 SKU</span><span class="sxs-lookup"><span data-stu-id="61198-911">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="61198-912">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="61198-912">July 28, 2017</span></span>

<span data-ttu-id="61198-913">版本 2.0.12</span><span class="sxs-lookup"><span data-stu-id="61198-913">Version 2.0.12</span></span>

* <span data-ttu-id="61198-914">添加了容器命令</span><span class="sxs-lookup"><span data-stu-id="61198-914">Added container commands</span></span>
* <span data-ttu-id="61198-915">添加了计费和消耗模块</span><span class="sxs-lookup"><span data-stu-id="61198-915">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="61198-916">核心</span><span class="sxs-lookup"><span data-stu-id="61198-916">Core</span></span>

* <span data-ttu-id="61198-917">输出包含证书的服务主体的 SDK 身份验证信息</span><span class="sxs-lookup"><span data-stu-id="61198-917">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="61198-918">修复了部署进度异常</span><span class="sxs-lookup"><span data-stu-id="61198-918">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="61198-919">使用当前云中的 arm 终结点创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="61198-919">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="61198-920">改进了 clouds.config 文件的并发处理 (#3636)</span><span class="sxs-lookup"><span data-stu-id="61198-920">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="61198-921">刷新每个命令执行进程的客户端请求 ID</span><span class="sxs-lookup"><span data-stu-id="61198-921">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="61198-922">使用适当的 SDK 配置文件创建订阅客户端 (#3635)</span><span class="sxs-lookup"><span data-stu-id="61198-922">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="61198-923">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="61198-923">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="61198-924">添加了通过 jmespath 查询选择表输出字段的支持 (#3581)</span><span class="sxs-lookup"><span data-stu-id="61198-924">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="61198-925">改进了分析参数的静默和包含手势的追加历史记录 (#3434)</span><span class="sxs-lookup"><span data-stu-id="61198-925">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="61198-926">使用适当的 SDK 配置文件创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="61198-926">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="61198-927">将所有现有记录文件移到最新的文件夹</span><span class="sxs-lookup"><span data-stu-id="61198-927">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="61198-928">修复了 VM/VMSS 创建操作的幂等性 (#3586)</span><span class="sxs-lookup"><span data-stu-id="61198-928">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="61198-929">命令路径不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="61198-929">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="61198-930">某些布尔类型的参数不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="61198-930">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="61198-931">支持登录到 Azure Stack 等本地服务器上的 ADFS</span><span class="sxs-lookup"><span data-stu-id="61198-931">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="61198-932">修复了并发写入 clouds.config 的问题 (#3255)</span><span class="sxs-lookup"><span data-stu-id="61198-932">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="61198-933">ACR</span><span class="sxs-lookup"><span data-stu-id="61198-933">ACR</span></span>

* <span data-ttu-id="61198-934">针对托管注册表添加了 `show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-934">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="61198-935">支持托管注册表的 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="61198-935">Support SKU update for managed registries</span></span>
* <span data-ttu-id="61198-936">添加了包含托管 SKU 的托管注册表</span><span class="sxs-lookup"><span data-stu-id="61198-936">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="61198-937">通过 ACR Webhook 命令模块添加了托管注册表的 Webhook</span><span class="sxs-lookup"><span data-stu-id="61198-937">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="61198-938">添加了使用 acr login 命令进行 AAD 身份验证的功能</span><span class="sxs-lookup"><span data-stu-id="61198-938">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="61198-939">添加了 Docker 存储库、清单和标记的 delete 命令</span><span class="sxs-lookup"><span data-stu-id="61198-939">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="61198-940">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-940">ACS</span></span>

* <span data-ttu-id="61198-941">API 版本 2017-07-01 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-941">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-942">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-942">Appservice</span></span>

* <span data-ttu-id="61198-943">修复了列出 Linux Web 应用时不返回任何内容的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-943">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="61198-944">支持从 ACR 检索凭据</span><span class="sxs-lookup"><span data-stu-id="61198-944">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="61198-945">删除 `appservice web` 下的所有命令</span><span class="sxs-lookup"><span data-stu-id="61198-945">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="61198-946">将命令输出中的 Docker 注册表密码掩码 (#3656)</span><span class="sxs-lookup"><span data-stu-id="61198-946">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="61198-947">确保在 macOS 上使用默认浏览器且不出错 (#3623)</span><span class="sxs-lookup"><span data-stu-id="61198-947">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="61198-948">改进了 `webapp log tail` 和 `webapp log download` 的帮助 (#3624)</span><span class="sxs-lookup"><span data-stu-id="61198-948">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="61198-949">公开了 `traffic-routing` 命令用于配置静态路由 (#3566)</span><span class="sxs-lookup"><span data-stu-id="61198-949">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="61198-950">添加了用于配置源代码管理的可靠性修复 (#3245)</span><span class="sxs-lookup"><span data-stu-id="61198-950">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="61198-951">从 `webapp config update` 中删除了 Windows Web 应用不支持的 `--node-version` 参数。</span><span class="sxs-lookup"><span data-stu-id="61198-951">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="61198-952">需改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`。</span><span class="sxs-lookup"><span data-stu-id="61198-952">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="61198-953">Batch</span><span class="sxs-lookup"><span data-stu-id="61198-953">Batch</span></span>

* <span data-ttu-id="61198-954">已更新到 Batch SDK 3.0.0，支持池中的低优先级 VM</span><span class="sxs-lookup"><span data-stu-id="61198-954">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="61198-955">已将 `pool create` 选项 `--target-dedicated` 重命名为 `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="61198-955">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="61198-956">添加了 `pool create` 选项 `--target-low-priority-nodes` 和 `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="61198-956">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="61198-957">CDN</span><span class="sxs-lookup"><span data-stu-id="61198-957">CDN</span></span>

* <span data-ttu-id="61198-958">当 `--profile-name` 指定的配置文件不存在时，为 `cdn endpoint list` 提供更完善的错误消息</span><span class="sxs-lookup"><span data-stu-id="61198-958">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="61198-959">云</span><span class="sxs-lookup"><span data-stu-id="61198-959">Cloud</span></span>

* <span data-ttu-id="61198-960">已将云元数据终结点的 API 版本更改为 YYYY-MM-DD 格式</span><span class="sxs-lookup"><span data-stu-id="61198-960">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="61198-961">不需要库终结点</span><span class="sxs-lookup"><span data-stu-id="61198-961">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="61198-962">支持只将云注册到 ARM 资源管理器终结点</span><span class="sxs-lookup"><span data-stu-id="61198-962">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="61198-963">提供 `cloud set` 的选项用于在选择当前云时选择配置文件</span><span class="sxs-lookup"><span data-stu-id="61198-963">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="61198-964">公开了 `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="61198-964">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="61198-965">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="61198-965">CosmosDB</span></span>

* <span data-ttu-id="61198-966">修复了允许使用自定义分区键创建集合的问题</span><span class="sxs-lookup"><span data-stu-id="61198-966">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="61198-967">添加了对集合默认 TTL 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-967">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="61198-968">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="61198-968">Data Lake Analytics</span></span>

* <span data-ttu-id="61198-969">在 `dla account compute-policy` 标题下添加了用于计算策略管理的命令</span><span class="sxs-lookup"><span data-stu-id="61198-969">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="61198-970">添加了 `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="61198-970">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="61198-971">添加了 `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="61198-971">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="61198-972">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="61198-972">Data Lake Store</span></span>

* <span data-ttu-id="61198-973">在 `dls account update` 中添加了用户管理的 Key Vault 密钥轮换的支持</span><span class="sxs-lookup"><span data-stu-id="61198-973">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="61198-974">更新了底层 Data Lake Store 文件系统 SDK 版本，解决了一个性能问题</span><span class="sxs-lookup"><span data-stu-id="61198-974">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="61198-975">添加了命令 `dls enable-key-vault`。</span><span class="sxs-lookup"><span data-stu-id="61198-975">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="61198-976">此命令尝试使用用户提供的 Key Vault 加密 Data Lake Store 帐户中的数据</span><span class="sxs-lookup"><span data-stu-id="61198-976">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="61198-977">交互</span><span class="sxs-lookup"><span data-stu-id="61198-977">Interactive</span></span>

* <span data-ttu-id="61198-978">使用缓存的命令改进启动时间</span><span class="sxs-lookup"><span data-stu-id="61198-978">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="61198-979">增大了测试覆盖率</span><span class="sxs-lookup"><span data-stu-id="61198-979">Increased test coverage</span></span>
* <span data-ttu-id="61198-980">增强了“?”手势，使之也可注入到下一条命令</span><span class="sxs-lookup"><span data-stu-id="61198-980">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="61198-981">修复了配置文件 2017-03-09-profile-preview 的交互错误 (#3587)</span><span class="sxs-lookup"><span data-stu-id="61198-981">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="61198-982">允许使用 `--version` 作为交互模式的参数 (#3645)</span><span class="sxs-lookup"><span data-stu-id="61198-982">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="61198-983">阻止交互模式在验证填写内容中引发错误 (#3570)</span><span class="sxs-lookup"><span data-stu-id="61198-983">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="61198-984">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="61198-984">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="61198-985">添加了 `--progress` 标志</span><span class="sxs-lookup"><span data-stu-id="61198-985">Added `--progress` flag</span></span>
* <span data-ttu-id="61198-986">从填写内容中删除了 `--debug` 和 `--verbose`</span><span class="sxs-lookup"><span data-stu-id="61198-986">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="61198-987">从填写内容中删除了 `interactive` (#3324)</span><span class="sxs-lookup"><span data-stu-id="61198-987">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="61198-988">IoT</span><span class="sxs-lookup"><span data-stu-id="61198-988">IoT</span></span>

* <span data-ttu-id="61198-989">修复了策略创建操作不再清除现有策略的问题。</span><span class="sxs-lookup"><span data-stu-id="61198-989">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="61198-990">(#3934)</span><span class="sxs-lookup"><span data-stu-id="61198-990">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="61198-991">密钥保管库</span><span class="sxs-lookup"><span data-stu-id="61198-991">Key vault</span></span>

* <span data-ttu-id="61198-992">添加了 Key Vault 恢复功能的命令：</span><span class="sxs-lookup"><span data-stu-id="61198-992">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="61198-993">`keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="61198-993">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="61198-994">`keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="61198-994">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="61198-995">`keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="61198-995">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="61198-996">`keyvault key` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="61198-996">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="61198-997">添加了服务主体的 Key Vault 集成 (#3133)</span><span class="sxs-lookup"><span data-stu-id="61198-997">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="61198-998">已将 Key Vault 数据平面更新到 0.3.2。</span><span class="sxs-lookup"><span data-stu-id="61198-998">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="61198-999">(#3307)</span><span class="sxs-lookup"><span data-stu-id="61198-999">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="61198-1000">实验室</span><span class="sxs-lookup"><span data-stu-id="61198-1000">Lab</span></span>

* <span data-ttu-id="61198-1001">添加了通过 `az lab vm claim` 在实验室中声明任何 VM 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1001">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="61198-1002">为 `az lab vm list` 和 `az lab vm show` 添加了表输出格式化程序</span><span class="sxs-lookup"><span data-stu-id="61198-1002">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="61198-1003">监视</span><span class="sxs-lookup"><span data-stu-id="61198-1003">Monitor</span></span>

* <span data-ttu-id="61198-1004">修复了与 `monitor autoscale-settings get-parameters-template` 命令结合使用的模板文件 (#3349)</span><span class="sxs-lookup"><span data-stu-id="61198-1004">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="61198-1005">已将 `monitor alert-rule-incidents list` 重命名为 `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="61198-1005">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="61198-1006">已将 `monitor alert-rule-incidents show` 重命名为 `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="61198-1006">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="61198-1007">已将 `monitor metric-defintions list` 重命名为 `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="61198-1007">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="61198-1008">已将 `monitor alert-rules` 重命名为 `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="61198-1008">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="61198-1009">更改了 `monitor alert create`：</span><span class="sxs-lookup"><span data-stu-id="61198-1009">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="61198-1010">`condition` 和 `action` 子命令不再接受 JSON</span><span class="sxs-lookup"><span data-stu-id="61198-1010">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="61198-1011">添加了大量的参数来简化规则创建过程</span><span class="sxs-lookup"><span data-stu-id="61198-1011">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="61198-1012">`location` 不再是必需的</span><span class="sxs-lookup"><span data-stu-id="61198-1012">`location` no longer required</span></span>
  * <span data-ttu-id="61198-1013">添加了目标的名称和 ID 支持</span><span class="sxs-lookup"><span data-stu-id="61198-1013">Add name and ID support for target</span></span>
  * <span data-ttu-id="61198-1014">删除了 `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="61198-1014">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="61198-1015">`is-enabled` 重命名为 `enabled`，不再是必需的</span><span class="sxs-lookup"><span data-stu-id="61198-1015">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="61198-1016">`description` 默认值现在基于提供的条件</span><span class="sxs-lookup"><span data-stu-id="61198-1016">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="61198-1017">添加了示例用于帮助澄清新格式</span><span class="sxs-lookup"><span data-stu-id="61198-1017">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="61198-1018">支持在 `monitor metric` 命令中使用名称或 ID</span><span class="sxs-lookup"><span data-stu-id="61198-1018">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="61198-1019">为 `monitor alert rule update` 添加了方便的参数和示例</span><span class="sxs-lookup"><span data-stu-id="61198-1019">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="61198-1020">网络</span><span class="sxs-lookup"><span data-stu-id="61198-1020">Network</span></span>

* <span data-ttu-id="61198-1021">添加了 `list-private-access-services` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-1021">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="61198-1022">为 `vnet subnet create` 和 `vnet subnet update` 添加了 `--private-access-services` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-1022">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="61198-1023">修复了 `application-gateway redirect-config create` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="61198-1023">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="61198-1024">修复了无法结合 `--no-wait` 使用 `application-gateway redirect-config update` 的问题</span><span class="sxs-lookup"><span data-stu-id="61198-1024">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="61198-1025">修复了结合 `application-gateway address-pool create` 和 `application-gateway address-pool update` 使用 `--servers` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-1025">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="61198-1026">添加了 `application-gateway redirect-config` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-1026">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="61198-1027">添加了 `application-gateway ssl-policy` 的命令：`list-options`、`predefined list`、`predefined show`</span><span class="sxs-lookup"><span data-stu-id="61198-1027">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="61198-1028">添加了 `application-gateway ssl-policy set` 的参数：`--name`、`--cipher-suites`、`--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="61198-1028">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="61198-1029">添加了 `application-gateway http-settings create` 和 `application-gateway http-settings update` 的参数：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`</span><span class="sxs-lookup"><span data-stu-id="61198-1029">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="61198-1030">添加了 `application-gateway url-path-map create` 和 `application-gateway url-path-map update` 的参数：`--default-redirect-config`、`--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="61198-1030">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="61198-1031">为 `application-gateway url-path-map rule create` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-1031">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="61198-1032">在 `application-gateway url-path-map rule delete` 中添加了对 `--no-wait` 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1032">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="61198-1033">添加了 `application-gateway probe create` 和 `application-gateway probe update` 的参数：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="61198-1033">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="61198-1034">为 `application-gateway rule create` 和 `application-gateway rule update` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-1034">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="61198-1035">在 `nic create` 和 `nic update` 中添加了对 `--accelerated-networking` 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1035">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="61198-1036">从 `nic create` 中删除了 `--internal-dns-name-suffix` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-1036">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="61198-1037">在 `nic update` 和 `nic create` 中添加了对 `--dns-servers` 的支持：添加了对 --dns-servers 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1037">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="61198-1038">修复了 `local-gateway create` 忽略 `--local-address-prefixes` 的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-1038">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="61198-1039">在 `vnet update` 中添加了对 `--dns-servers` 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1039">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="61198-1040">修复了使用 `express-route peering create` 创建不包含路由筛选的对等互连时的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-1040">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="61198-1041">修复了无法结合 `--provider` 和 `--bandwidth` 参数使用 `express-route update` 的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-1041">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="61198-1042">修复了 `network watcher show-topology` 默认逻辑的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-1042">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="61198-1043">改进了 `network list-usages` 的输出格式</span><span class="sxs-lookup"><span data-stu-id="61198-1043">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="61198-1044">如果只存在一个，则对 `application-gateway http-listener create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="61198-1044">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="61198-1045">如果只存在一个，则对 `application-gateway rule create` 使用默认地址池、HTTP 设置和 HTTP 侦听器</span><span class="sxs-lookup"><span data-stu-id="61198-1045">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="61198-1046">如果只存在一个，则对 `lb rule create` 使用默认前端 IP 和后端池</span><span class="sxs-lookup"><span data-stu-id="61198-1046">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="61198-1047">如果只存在一个，则对 `lb inbound-nat-rule create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="61198-1047">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="61198-1048">配置文件</span><span class="sxs-lookup"><span data-stu-id="61198-1048">Profile</span></span>

* <span data-ttu-id="61198-1049">支持使用托管标识在 VM 内部登录</span><span class="sxs-lookup"><span data-stu-id="61198-1049">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="61198-1050">支持采用 SDK 身份验证文件格式的 `account show` 输出</span><span class="sxs-lookup"><span data-stu-id="61198-1050">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="61198-1051">使用 '--expanded-view' 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="61198-1051">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="61198-1052">添加了 `get-access-token` 命令来提供原始 AAD 令牌</span><span class="sxs-lookup"><span data-stu-id="61198-1052">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="61198-1053">支持使用不包含关联订阅的用户帐户登录</span><span class="sxs-lookup"><span data-stu-id="61198-1053">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="61198-1054">RDBMS</span><span class="sxs-lookup"><span data-stu-id="61198-1054">RDBMS</span></span>

* <span data-ttu-id="61198-1055">支持跨订阅列出服务器 (#3417)</span><span class="sxs-lookup"><span data-stu-id="61198-1055">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="61198-1056">修复了由于缺少 `% server_type` 而不处理 `%s` 的问题 (#3393)</span><span class="sxs-lookup"><span data-stu-id="61198-1056">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="61198-1057">修复了文档源映射并添加了 CI 任务用于验证 (#3361)</span><span class="sxs-lookup"><span data-stu-id="61198-1057">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="61198-1058">修复了 MySQL 和 PostgreSQL 帮助 (#3369)</span><span class="sxs-lookup"><span data-stu-id="61198-1058">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="61198-1059">资源</span><span class="sxs-lookup"><span data-stu-id="61198-1059">Resource</span></span>

* <span data-ttu-id="61198-1060">改进了有关 `group deployment create` 缺少参数的提示</span><span class="sxs-lookup"><span data-stu-id="61198-1060">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="61198-1061">改进了 `--parameters KEY=VALUE` 语法分析</span><span class="sxs-lookup"><span data-stu-id="61198-1061">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="61198-1062">修复了不再能够使用 `@<file>` 语法识别 `group deployment create` 参数文件的问题</span><span class="sxs-lookup"><span data-stu-id="61198-1062">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="61198-1063">支持 `resource` 和 `managedapp` 命令的 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-1063">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="61198-1064">修复了一些分析和错误消息 (#3584)</span><span class="sxs-lookup"><span data-stu-id="61198-1064">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="61198-1065">修复了 `lock` 命令的 `--resource-type` 分析，接受 `<resource-namespace>` 和 `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="61198-1065">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="61198-1066">添加了模板链接模板的参数检查 (#3629)</span><span class="sxs-lookup"><span data-stu-id="61198-1066">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="61198-1067">添加了使用 `KEY=VALUE` 语法指定部署参数的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1067">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="61198-1068">角色</span><span class="sxs-lookup"><span data-stu-id="61198-1068">Role</span></span>

* <span data-ttu-id="61198-1069">支持采用 SDK 身份验证文件格式的 `create-for-rbac` 输出</span><span class="sxs-lookup"><span data-stu-id="61198-1069">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="61198-1070">删除服务主体时清理角色分配和相关的 AAD 应用程序 (#3610)</span><span class="sxs-lookup"><span data-stu-id="61198-1070">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="61198-1071">在 `app create` 参数 `--start-date` 和 `--end-date` 说明中包含时间格式</span><span class="sxs-lookup"><span data-stu-id="61198-1071">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="61198-1072">使用 `--expanded-view` 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="61198-1072">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="61198-1073">在 `create-for-rbac` 和 `reset-credentials` 命令中添加了 Key Vault 集成</span><span class="sxs-lookup"><span data-stu-id="61198-1073">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="61198-1074">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="61198-1074">Service Fabric</span></span>
* <span data-ttu-id="61198-1075">修复了上传时截断应用程序中的大型文件的问题 (#3666)</span><span class="sxs-lookup"><span data-stu-id="61198-1075">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="61198-1076">添加了 Service Fabric 命令的测试 (#3424)</span><span class="sxs-lookup"><span data-stu-id="61198-1076">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="61198-1077">添加了大量的 Service Fabric 命令 (#3234)</span><span class="sxs-lookup"><span data-stu-id="61198-1077">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="61198-1078">SQL</span><span class="sxs-lookup"><span data-stu-id="61198-1078">SQL</span></span>

* <span data-ttu-id="61198-1079">删除了无效的 `sql server create` `--identity` 参数</span><span class="sxs-lookup"><span data-stu-id="61198-1079">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="61198-1080">从 `sql server create` 和 `sql server update` 命令输出中删除了密码值</span><span class="sxs-lookup"><span data-stu-id="61198-1080">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="61198-1081">添加了命令 `sql db list-editions` 和 `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="61198-1081">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="61198-1082">存储</span><span class="sxs-lookup"><span data-stu-id="61198-1082">Storage</span></span>

* <span data-ttu-id="61198-1083">从 `storage blob list`、`storage container list` 和 `storage share list` 命令中删除了 `--marker` 选项 (#3745)</span><span class="sxs-lookup"><span data-stu-id="61198-1083">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="61198-1084">启用了创建仅限 https 的存储帐户</span><span class="sxs-lookup"><span data-stu-id="61198-1084">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="61198-1085">更新了存储指标、日志记录和 CORS 命令 (#3495)</span><span class="sxs-lookup"><span data-stu-id="61198-1085">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="61198-1086">重新编写了 CORS add 命令的异常消息 (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="61198-1086">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="61198-1087">已在下载批处理命令试运行模式下将生成器转换为列表 (#3592)</span><span class="sxs-lookup"><span data-stu-id="61198-1087">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="61198-1088">修复了 Blob 下载批处理试运行问题 (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="61198-1088">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="61198-1089">VM</span><span class="sxs-lookup"><span data-stu-id="61198-1089">VM</span></span>

* <span data-ttu-id="61198-1090">支持配置 NSG</span><span class="sxs-lookup"><span data-stu-id="61198-1090">Support configuring nsg</span></span>
* <span data-ttu-id="61198-1091">修复了无法正确配置 DNS 服务器的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-1091">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="61198-1092">支持托管服务标识</span><span class="sxs-lookup"><span data-stu-id="61198-1092">Support managed service identities</span></span>
* <span data-ttu-id="61198-1093">修复了包含现有负载均衡器的 `cmss create` 需要 `--backend-pool-name` 的问题</span><span class="sxs-lookup"><span data-stu-id="61198-1093">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="61198-1094">要求使用 `vm image create` LUN 创建的数据磁盘以 0 开头</span><span class="sxs-lookup"><span data-stu-id="61198-1094">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="61198-1095">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="61198-1095">May 10, 2017</span></span>

<span data-ttu-id="61198-1096">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="61198-1096">Version 2.0.6</span></span>

* <span data-ttu-id="61198-1097">Documentdb 已重命名为 Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="61198-1097">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="61198-1098">添加 rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="61198-1098">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="61198-1099">包括 Data Lake Analytics 和 Data Lake Store 模块</span><span class="sxs-lookup"><span data-stu-id="61198-1099">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="61198-1100">包括认知服务模块</span><span class="sxs-lookup"><span data-stu-id="61198-1100">Include Cognitive Services module</span></span>
* <span data-ttu-id="61198-1101">包括 Service Fabric 模块</span><span class="sxs-lookup"><span data-stu-id="61198-1101">Include Service Fabric module</span></span>
* <span data-ttu-id="61198-1102">包括交互式模块（重命名 az-shell）</span><span class="sxs-lookup"><span data-stu-id="61198-1102">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="61198-1103">添加对 CDN 命令的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1103">Add support for CDN commands</span></span>
* <span data-ttu-id="61198-1104">删除容器模块</span><span class="sxs-lookup"><span data-stu-id="61198-1104">Remove Container module</span></span>
* <span data-ttu-id="61198-1105">添加“az -v”作为“az --version”的快捷方式 ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="61198-1105">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="61198-1106">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="61198-1106">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="61198-1107">核心</span><span class="sxs-lookup"><span data-stu-id="61198-1107">Core</span></span>

* <span data-ttu-id="61198-1108">核心：捕获未注册提供程序引发的异常并自动注册</span><span class="sxs-lookup"><span data-stu-id="61198-1108">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="61198-1109">性能：将 ADAL 令牌缓存保留在内存中，直至进程退出 ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="61198-1109">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="61198-1110">修复从十六进制指纹 -o tsv 返回的字节 ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="61198-1110">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="61198-1111">改进的 Key Vault 证书下载和 AAD SP 集成 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="61198-1111">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="61198-1112">将 Python 位置添加到“az —version”([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="61198-1112">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="61198-1113">登录：无订阅时支持登录 ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="61198-1113">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="61198-1114">核心：修复重复使用服务主体登录时出现的故障 ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="61198-1114">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="61198-1115">核心：允许通过 env var 配置 accessTokens.json 的文件路径 ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="61198-1115">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="61198-1116">核心：允许配置的默认值应用于可选参数 ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="61198-1116">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="61198-1117">核心：提高了性能</span><span class="sxs-lookup"><span data-stu-id="61198-1117">core: Improved performance</span></span>
* <span data-ttu-id="61198-1118">核心：自定义 CA 证书 - 支持设置 REQUESTS_CA_BUNDLE 环境变量</span><span class="sxs-lookup"><span data-stu-id="61198-1118">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="61198-1119">核心：云配置 - 如果未设置“management”终结点，则使用“resource manager”终结点</span><span class="sxs-lookup"><span data-stu-id="61198-1119">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="61198-1120">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-1120">ACS</span></span>

* <span data-ttu-id="61198-1121">将主计数和代理计数修复为整数而不是字符串</span><span class="sxs-lookup"><span data-stu-id="61198-1121">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="61198-1122">公开“az acs create --no-wait”和“az acs wait”用于异步创建</span><span class="sxs-lookup"><span data-stu-id="61198-1122">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="61198-1123">公开“az acs create --validate”用于试运行验证</span><span class="sxs-lookup"><span data-stu-id="61198-1123">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="61198-1124">在 PUT 调用 scale 命令前删除 Windows 配置文件 ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="61198-1124">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-1125">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-1125">AppService</span></span>

* <span data-ttu-id="61198-1126">Function App：添加完整的 Function App 支持，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="61198-1126">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="61198-1127">将 Team Services (vsts) 作为持续交付选项添加到“appservice web source-control config”</span><span class="sxs-lookup"><span data-stu-id="61198-1127">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="61198-1128">创建“az webapp”以替换“az appservice web”（为了向后兼容，“az appservice web”将保留 2 个版本）</span><span class="sxs-lookup"><span data-stu-id="61198-1128">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="61198-1129">公开参数以针对 webapp create 配置部署和“运行时堆栈”</span><span class="sxs-lookup"><span data-stu-id="61198-1129">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="61198-1130">公开“webapp list-runtimes”</span><span class="sxs-lookup"><span data-stu-id="61198-1130">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="61198-1131">支持配置连接字符串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="61198-1131">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="61198-1132">支持与预览版交换槽</span><span class="sxs-lookup"><span data-stu-id="61198-1132">support slot swap with preview</span></span>
* <span data-ttu-id="61198-1133">修改 appservice 命令的错误 ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="61198-1133">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="61198-1134">将应用服务计划的资源组用于证书操作 ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="61198-1134">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="61198-1135">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="61198-1135">CosmosDB</span></span>

* <span data-ttu-id="61198-1136">将 documentdb 模块重命名为 cosmosdb</span><span class="sxs-lookup"><span data-stu-id="61198-1136">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="61198-1137">增加对 DocumentDB 数据平面 API 的支持：数据库和集合管理</span><span class="sxs-lookup"><span data-stu-id="61198-1137">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="61198-1138">增加对数据库帐户启用自动故障转移的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1138">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="61198-1139">增加对新一致性策略 ConsistentPrefix 的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1139">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="61198-1140">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="61198-1140">Data Lake Analytics</span></span>

* <span data-ttu-id="61198-1141">修复了在筛选作业结果和状态列表时会引发错误的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-1141">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="61198-1142">增加对新目录项类型的支持：包。</span><span class="sxs-lookup"><span data-stu-id="61198-1142">Add support for new catalog item type: package.</span></span> <span data-ttu-id="61198-1143">访问方法：`az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="61198-1143">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="61198-1144">可从数据库内列出下列目录项（无需架构规范）：</span><span class="sxs-lookup"><span data-stu-id="61198-1144">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="61198-1145">表</span><span class="sxs-lookup"><span data-stu-id="61198-1145">Table</span></span>
  * <span data-ttu-id="61198-1146">表值函数</span><span class="sxs-lookup"><span data-stu-id="61198-1146">Table valued function</span></span>
  * <span data-ttu-id="61198-1147">查看</span><span class="sxs-lookup"><span data-stu-id="61198-1147">View</span></span>
  * <span data-ttu-id="61198-1148">表统计信息。</span><span class="sxs-lookup"><span data-stu-id="61198-1148">Table Statistics.</span></span> <span data-ttu-id="61198-1149">这也可以使用架构（但无需指定表名）列出</span><span class="sxs-lookup"><span data-stu-id="61198-1149">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="61198-1150">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="61198-1150">Data Lake Store</span></span>

* <span data-ttu-id="61198-1151">更新基础文件系统 SDK 的版本，以便为处理服务器端限制场景提供更好的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1151">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="61198-1152">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="61198-1152">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="61198-1153">访问显示帮助丢失。</span><span class="sxs-lookup"><span data-stu-id="61198-1153">missed help for access show.</span></span> <span data-ttu-id="61198-1154">正在添加。</span><span class="sxs-lookup"><span data-stu-id="61198-1154">adding it.</span></span> <span data-ttu-id="61198-1155">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="61198-1155">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="61198-1156">查找</span><span class="sxs-lookup"><span data-stu-id="61198-1156">Find</span></span>

* <span data-ttu-id="61198-1157">改进搜索结果，允许搜索索引的版本控制</span><span class="sxs-lookup"><span data-stu-id="61198-1157">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="61198-1158">KeyVault</span><span class="sxs-lookup"><span data-stu-id="61198-1158">KeyVault</span></span>

* <span data-ttu-id="61198-1159">BC：`az keyvault certificate download` 将 -e 从字符串或二进制更改为 PEM 或 DER，从而更好地表示选项</span><span class="sxs-lookup"><span data-stu-id="61198-1159">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="61198-1160">BC：从 `keyvault certificate create` 删除 --expires 和 --not-before，因为此服务不支持这些参数</span><span class="sxs-lookup"><span data-stu-id="61198-1160">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="61198-1161">将 --validity 参数添加到 `keyvault certificate create`，有选择地替代 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="61198-1161">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="61198-1162">修复了 `keyvault certificate get-default-policy` 中已公开“expires”和“not_before”但未公开“validity_in_months”的问题</span><span class="sxs-lookup"><span data-stu-id="61198-1162">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="61198-1163">KeyVault 解决了 pem 和 pfx 的导入问题 ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="61198-1163">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="61198-1164">实验室</span><span class="sxs-lookup"><span data-stu-id="61198-1164">Lab</span></span>

* <span data-ttu-id="61198-1165">为实验室中的环境添加 create、show、delete 和 list 命令</span><span class="sxs-lookup"><span data-stu-id="61198-1165">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="61198-1166">添加 show 和 list 命令以查看实验室中的 ARM 模板</span><span class="sxs-lookup"><span data-stu-id="61198-1166">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="61198-1167">在 `az lab vm list` 中添加 --environment 标志，以便按实验室中的环境筛选 VM</span><span class="sxs-lookup"><span data-stu-id="61198-1167">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="61198-1168">添加方便命令 `az lab formula export-artifacts`，以便导出实验室公式中的项目基架</span><span class="sxs-lookup"><span data-stu-id="61198-1168">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="61198-1169">添加命令以管理实验室中的机密</span><span class="sxs-lookup"><span data-stu-id="61198-1169">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="61198-1170">监视</span><span class="sxs-lookup"><span data-stu-id="61198-1170">Monitor</span></span>

* <span data-ttu-id="61198-1171">Bug 修复：为 `az alert-rules create` 的 `--actions` 建模，以使用 JSON 字符串 ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="61198-1171">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="61198-1172">Bug 修复 - diagnostic settings create 不接受来自 show 命令的日志/指标 ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="61198-1172">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="61198-1173">网络</span><span class="sxs-lookup"><span data-stu-id="61198-1173">Network</span></span>

* <span data-ttu-id="61198-1174">添加 `network watcher test-connectivity` 命令</span><span class="sxs-lookup"><span data-stu-id="61198-1174">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="61198-1175">为 `network watcher packet-capture create` 添加对 `--filters` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1175">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="61198-1176">添加对应用程序网关连接排出的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1176">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="61198-1177">添加对应用程序网关 WAF 规则集配置的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1177">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="61198-1178">添加对 ExpressRoute 路由筛选器和规则的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1178">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="61198-1179">添加对 TrafficManager 地理路由的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1179">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="61198-1180">添加对基于 VPN 连接策略的流量选择器的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1180">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="61198-1181">添加对 VPN 连接 IPSec 策略的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1181">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="61198-1182">修复使用 `--no-wait` 或 `--validate` 参数时 `vpn-connection create` 出现的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-1182">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="61198-1183">添加对主动-主动 VNet 网关的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1183">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="61198-1184">从 `network vpn-connection list/show` 命令的输出中删除 null 值</span><span class="sxs-lookup"><span data-stu-id="61198-1184">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="61198-1185">BC：修复 `vpn-connection create` 输出中的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-1185">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="61198-1186">修复无法正确分析“vpn-connection create”的“--key-length”参数的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-1186">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="61198-1187">修复 `dns zone import` 中无法正确导入记录的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-1187">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="61198-1188">修复 `traffic-manager endpoint update` 不起作用的 bug</span><span class="sxs-lookup"><span data-stu-id="61198-1188">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="61198-1189">添加“network watcher”预览命令</span><span class="sxs-lookup"><span data-stu-id="61198-1189">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="61198-1190">配置文件</span><span class="sxs-lookup"><span data-stu-id="61198-1190">Profile</span></span>

* <span data-ttu-id="61198-1191">支持在未找到订阅时登录 ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="61198-1191">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="61198-1192">支持在 az account set --subscription 中使用短参数名 ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="61198-1192">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="61198-1193">Redis</span><span class="sxs-lookup"><span data-stu-id="61198-1193">Redis</span></span>

* <span data-ttu-id="61198-1194">添加 update 命令，也增加了对 redis 缓存进行缩放的功能</span><span class="sxs-lookup"><span data-stu-id="61198-1194">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="61198-1195">弃用“update-settings”命令</span><span class="sxs-lookup"><span data-stu-id="61198-1195">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="61198-1196">资源</span><span class="sxs-lookup"><span data-stu-id="61198-1196">Resource</span></span>

* <span data-ttu-id="61198-1197">添加 managedapp 和 managedapp 定义命令 ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="61198-1197">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="61198-1198">支持“provider operation”命令([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="61198-1198">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="61198-1199">支持 generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="61198-1199">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="61198-1200">修复资源分析和 API 版本查找。</span><span class="sxs-lookup"><span data-stu-id="61198-1200">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="61198-1201">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="61198-1201">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="61198-1202">为 az lock update 添加文档。</span><span class="sxs-lookup"><span data-stu-id="61198-1202">Add docs for az lock update.</span></span> <span data-ttu-id="61198-1203">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="61198-1203">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="61198-1204">尝试为不存在的组列出资源时出错。</span><span class="sxs-lookup"><span data-stu-id="61198-1204">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="61198-1205">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="61198-1205">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="61198-1206">[计算] 修复 VMSS 和 VM 可用性集更新的相关问题。</span><span class="sxs-lookup"><span data-stu-id="61198-1206">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="61198-1207">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="61198-1207">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="61198-1208">parent-resource-path 为 None 时修复 lock create 和 delete ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="61198-1208">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="61198-1209">角色</span><span class="sxs-lookup"><span data-stu-id="61198-1209">Role</span></span>

* <span data-ttu-id="61198-1210">create-for-rbac：确保 SP 的结束日期不超过证书的到期日期 ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="61198-1210">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="61198-1211">RBAC：添加对“ad group”的完整支持 ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="61198-1211">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="61198-1212">role：解决角色定义更新的相关问题 ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="61198-1212">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="61198-1213">create-for-rbac：确保已选取用户提供的密码</span><span class="sxs-lookup"><span data-stu-id="61198-1213">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="61198-1214">SQL</span><span class="sxs-lookup"><span data-stu-id="61198-1214">SQL</span></span>

* <span data-ttu-id="61198-1215">添加了 az sql server list-usages 和 az sql db list-usages 命令</span><span class="sxs-lookup"><span data-stu-id="61198-1215">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="61198-1216">SQL - 能够直接连接到资源提供程序 ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="61198-1216">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="61198-1217">存储</span><span class="sxs-lookup"><span data-stu-id="61198-1217">Storage</span></span>

* <span data-ttu-id="61198-1218">对于 `storage account create`，将位置默认为资源组位置</span><span class="sxs-lookup"><span data-stu-id="61198-1218">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="61198-1219">添加对增量 blob 复制的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1219">Add support for incremental blob copy</span></span>
* <span data-ttu-id="61198-1220">添加对大型块 blob 上传的支持</span><span class="sxs-lookup"><span data-stu-id="61198-1220">Add support for large block blob upload</span></span>
* <span data-ttu-id="61198-1221">如果要上传的文件大于 200GB，则将块大小更改为 100MB</span><span class="sxs-lookup"><span data-stu-id="61198-1221">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="61198-1222">VM</span><span class="sxs-lookup"><span data-stu-id="61198-1222">VM</span></span>

* <span data-ttu-id="61198-1223">avail-set：将 UD 和 FD 域计数设为可选</span><span class="sxs-lookup"><span data-stu-id="61198-1223">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="61198-1224">注意：最高等级云中的 VM 命令。请避免与托管磁盘相关的功能，包括以下项：</span><span class="sxs-lookup"><span data-stu-id="61198-1224">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="61198-1225">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="61198-1225">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="61198-1226">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="61198-1226">az vm/vmss disk</span></span>
  3. <span data-ttu-id="61198-1227">在“az vm/vmss create”内，使用“—use-unmanaged-disk”避免托管磁盘 其他命令应有效</span><span class="sxs-lookup"><span data-stu-id="61198-1227">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="61198-1228">vm/vmss：改进生成 SSH 密钥对时的警告文本</span><span class="sxs-lookup"><span data-stu-id="61198-1228">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="61198-1229">vm/vmss：支持通过需要计划信息的市场映像创建 ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="61198-1229">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="61198-1230">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="61198-1230">April 3, 2017</span></span>

<span data-ttu-id="61198-1231">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="61198-1231">Version 2.0.2</span></span>

<span data-ttu-id="61198-1232">此版本中已发布 ACR、Batch、KeyVault 和 SQL 组件</span><span class="sxs-lookup"><span data-stu-id="61198-1232">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="61198-1233">核心</span><span class="sxs-lookup"><span data-stu-id="61198-1233">Core</span></span>

* <span data-ttu-id="61198-1234">在默认列表中添加了 acr、lab、monitor 和 find 模块</span><span class="sxs-lookup"><span data-stu-id="61198-1234">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="61198-1235">登录：跳过错误的租户 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="61198-1235">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="61198-1236">登录：将默认订阅设置为处于“已启用”状态的订阅 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="61198-1236">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="61198-1237">添加了 wait 命令，并添加了对其他命令的 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="61198-1237">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="61198-1238">核心：支持结合证书使用服务主体登录 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="61198-1238">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="61198-1239">添加了有关缺少模板参数的提示。</span><span class="sxs-lookup"><span data-stu-id="61198-1239">Add prompting for missing template parameters.</span></span> <span data-ttu-id="61198-1240">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="61198-1240">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="61198-1241">支持为资源组、默认 Web、 默认 VM 等常见参数设置默认值</span><span class="sxs-lookup"><span data-stu-id="61198-1241">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="61198-1242">支持登录到特定的租户</span><span class="sxs-lookup"><span data-stu-id="61198-1242">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="61198-1243">ACS</span><span class="sxs-lookup"><span data-stu-id="61198-1243">ACS</span></span>

* <span data-ttu-id="61198-1244">[ACS] 添加了配置默认 ACS 群集的支持 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="61198-1244">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="61198-1245">添加了 SSH 密钥密码提示的支持。</span><span class="sxs-lookup"><span data-stu-id="61198-1245">Add support for ssh key password prompting.</span></span> <span data-ttu-id="61198-1246">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="61198-1246">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="61198-1247">添加了对 Windows 群集的支持。</span><span class="sxs-lookup"><span data-stu-id="61198-1247">Add support for windows clusters.</span></span> <span data-ttu-id="61198-1248">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="61198-1248">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="61198-1249">从“所有者”角色切换到“参与者”角色。</span><span class="sxs-lookup"><span data-stu-id="61198-1249">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="61198-1250">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="61198-1250">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="61198-1251">应用服务</span><span class="sxs-lookup"><span data-stu-id="61198-1251">AppService</span></span>

* <span data-ttu-id="61198-1252">应用服务：支持获取用于 DNS A 记录的外部 IP 地址 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="61198-1252">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="61198-1253">应用服务：支持绑定通配符证书 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="61198-1253">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="61198-1254">应用服务：支持列出发布配置文件 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="61198-1254">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="61198-1255">应用服务 - 配置后触发源代码管理同步 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="61198-1255">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="61198-1256">DataLake</span><span class="sxs-lookup"><span data-stu-id="61198-1256">DataLake</span></span>

* <span data-ttu-id="61198-1257">Data Lake Analytics 模块的初始版本</span><span class="sxs-lookup"><span data-stu-id="61198-1257">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="61198-1258">Data Lake Store 模块的初始版本</span><span class="sxs-lookup"><span data-stu-id="61198-1258">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="61198-1259">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="61198-1259">DocuemntDB</span></span>

* <span data-ttu-id="61198-1260">DocumentDB：添加了列出连接字符串的支持 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="61198-1260">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="61198-1261">VM</span><span class="sxs-lookup"><span data-stu-id="61198-1261">VM</span></span>

* <span data-ttu-id="61198-1262">[计算] 添加了用于创建虚拟机规模集的应用网关支持 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="61198-1262">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="61198-1263">[VM/VMSS] 改进了磁盘缓存支持 ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="61198-1263">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="61198-1264">VM/VMSS：合并了门户使用的凭据验证逻辑 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="61198-1264">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="61198-1265">添加了 wait 命令和 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="61198-1265">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="61198-1266">虚拟机规模集：支持使用 \* 列出不同 VM 上的实例视图 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="61198-1266">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="61198-1267">为 VM 和虚拟机规模集添加了 --secrets ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="61198-1267">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="61198-1268">允许使用专用 VHD 创建 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="61198-1268">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="61198-1269">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="61198-1269">February 27, 2017</span></span>

<span data-ttu-id="61198-1270">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="61198-1270">Version 2.0.0</span></span>

<span data-ttu-id="61198-1271">此 Azure CLI 2.0 发布版是第一个“正式版”。正式版适用于以下命令模块：</span><span class="sxs-lookup"><span data-stu-id="61198-1271">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="61198-1272">容器服务 (ACS)</span><span class="sxs-lookup"><span data-stu-id="61198-1272">Container Service (acs)</span></span>
- <span data-ttu-id="61198-1273">计算（包括 Resource Manager、VM、虚拟机规模集、托管磁盘）</span><span class="sxs-lookup"><span data-stu-id="61198-1273">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="61198-1274">网络</span><span class="sxs-lookup"><span data-stu-id="61198-1274">Networking</span></span>
- <span data-ttu-id="61198-1275">存储</span><span class="sxs-lookup"><span data-stu-id="61198-1275">Storage</span></span>

<span data-ttu-id="61198-1276">这些命令模块可在生产中使用，并且受标准 Microsoft SLA 支持。可以直接通过 Microsoft 支持部门创建问题，也可以在我们的 [github 问题列表](https://github.com/azure/azure-cli/issues/)中创建问题。可以[使用 azure-cli 标记在 StackOverflow 上](http://stackoverflow.com/questions/tagged/azure-cli)提问，也可以通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队。可以从命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="61198-1276">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="61198-1277">这些模块中的命令非常稳定，其语法在此 Azure CLI 版本即将到来的发行版中预期不会变化。</span><span class="sxs-lookup"><span data-stu-id="61198-1277">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="61198-1278">若要验证 CLI 的版本，请使用 `az --version`。输出中将列出 CLI 本身的版本（在此发行版中为 2.0.0）、各个命令模块的版本，以及所用 Python 和 GCC 的版本。</span><span class="sxs-lookup"><span data-stu-id="61198-1278">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="61198-1279">其中的一些命令模块有“b*n*”或“rc*n*”后缀。这些命令模块仍在预览版中提供，将来会发布正式版。</span><span class="sxs-lookup"><span data-stu-id="61198-1279">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="61198-1280">此外，我们还提供 CLI 夜间预览版。有关信息，请参阅有关[获取夜间预览版](https://github.com/Azure/azure-cli#nightly-builds)的说明，以及有关[开发人员设置与贡献代码](https://github.com/Azure/azure-cli#developer-setup)的说明。</span><span class="sxs-lookup"><span data-stu-id="61198-1280">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="61198-1281">可通过以下方式报告夜间预览版的问题：</span><span class="sxs-lookup"><span data-stu-id="61198-1281">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="61198-1282">在 [github 问题列表](https://github.com/azure/azure-cli/issues/)中报告问题</span><span class="sxs-lookup"><span data-stu-id="61198-1282">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="61198-1283">通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队</span><span class="sxs-lookup"><span data-stu-id="61198-1283">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="61198-1284">通过命令行使用 `az feedback` 命令提供反馈</span><span class="sxs-lookup"><span data-stu-id="61198-1284">Provide feedback from the command line with the `az feedback` command</span></span>

