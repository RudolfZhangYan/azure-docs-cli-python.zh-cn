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
ms.openlocfilehash: e02b84891f4bf60cde12591b8e85987f4b3c9e79
ms.sourcegitcommit: 2e4d0bdd94c626e061434883032367b5619de4fe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="4e757-104">Azure CLI 2.0 发行说明</span><span class="sxs-lookup"><span data-stu-id="4e757-104">Azure CLI 2.0 release notes</span></span>

## <a name="december-5-2017"></a><span data-ttu-id="4e757-105">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="4e757-105">December 5, 2017</span></span>

<span data-ttu-id="4e757-106">版本 2.0.22</span><span class="sxs-lookup"><span data-stu-id="4e757-106">Version 2.0.22</span></span>

* <span data-ttu-id="4e757-107">已删除 `az component` 命令。</span><span class="sxs-lookup"><span data-stu-id="4e757-107">Removed `az component` commands.</span></span> <span data-ttu-id="4e757-108">请改用 `az extension`</span><span class="sxs-lookup"><span data-stu-id="4e757-108">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="4e757-109">核心</span><span class="sxs-lookup"><span data-stu-id="4e757-109">Core</span></span>
* <span data-ttu-id="4e757-110">已将 `AZURE_US_GOV_CLOUD` AAD 颁发机构终结点从 login.microsoftonline.com 修改为 login.microsoftonline.us</span><span class="sxs-lookup"><span data-stu-id="4e757-110">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="4e757-111">已修复持续重新发送遥测数据的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-111">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="4e757-112">ACS</span><span class="sxs-lookup"><span data-stu-id="4e757-112">ACS</span></span>

* <span data-ttu-id="4e757-113">已添加 `aks install-connector` 和 `aks remove-connector` 命令</span><span class="sxs-lookup"><span data-stu-id="4e757-113">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="4e757-114">已改进 `acs create` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="4e757-114">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="4e757-115">已修复不带完全限定路径的 `aks get-credentials -f` 的用法</span><span class="sxs-lookup"><span data-stu-id="4e757-115">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="4e757-116">顾问</span><span class="sxs-lookup"><span data-stu-id="4e757-116">Advisor</span></span>

* <span data-ttu-id="4e757-117">初始版本</span><span class="sxs-lookup"><span data-stu-id="4e757-117">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="4e757-118">应用服务</span><span class="sxs-lookup"><span data-stu-id="4e757-118">Appservice</span></span>

* <span data-ttu-id="4e757-119">已修复使用 `webapp config ssl upload` 时的证书名称生成问题</span><span class="sxs-lookup"><span data-stu-id="4e757-119">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="4e757-120">已修复 `webapp [list|show]` 和 `functionapp [list|show]` 以显示正确的应用</span><span class="sxs-lookup"><span data-stu-id="4e757-120">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="4e757-121">已为 `WEBSITE_NODE_DEFAULT_VERSION` 添加了默认值</span><span class="sxs-lookup"><span data-stu-id="4e757-121">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="4e757-122">消耗</span><span class="sxs-lookup"><span data-stu-id="4e757-122">Consumption</span></span>

* <span data-ttu-id="4e757-123">已添加对 API 版本 2017-11-30 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-123">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="4e757-124">容器</span><span class="sxs-lookup"><span data-stu-id="4e757-124">Container</span></span>

* <span data-ttu-id="4e757-125">已修复默认端口回归</span><span class="sxs-lookup"><span data-stu-id="4e757-125">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="4e757-126">监视</span><span class="sxs-lookup"><span data-stu-id="4e757-126">Monitor</span></span>

* <span data-ttu-id="4e757-127">已添加对指标命令的多维支持</span><span class="sxs-lookup"><span data-stu-id="4e757-127">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="4e757-128">资源</span><span class="sxs-lookup"><span data-stu-id="4e757-128">Resource</span></span>

* <span data-ttu-id="4e757-129">为 `resource show` 添加了 `--include-response-body` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-129">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="4e757-130">角色</span><span class="sxs-lookup"><span data-stu-id="4e757-130">Role</span></span>

* <span data-ttu-id="4e757-131">已将“经典”管理员的默认分配显示添加到 `role assignment list`</span><span class="sxs-lookup"><span data-stu-id="4e757-131">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="4e757-132">已添加对 `ad sp reset-credentials` 的支持以便添加凭据而不是覆盖</span><span class="sxs-lookup"><span data-stu-id="4e757-132">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="4e757-133">已改进 `ad sp create-for-rbac` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="4e757-133">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="4e757-134">SQL</span><span class="sxs-lookup"><span data-stu-id="4e757-134">SQL</span></span>

* <span data-ttu-id="4e757-135">已添加 `sql db list-usages` 和 `sql db show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="4e757-135">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="4e757-136">已添加 `sql server conn-policy show` 和 `sql server conn-policy update` 命令</span><span class="sxs-lookup"><span data-stu-id="4e757-136">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="4e757-137">VM</span><span class="sxs-lookup"><span data-stu-id="4e757-137">VM</span></span>

* <span data-ttu-id="4e757-138">已对 `az vm list-skus` 添加区域信息</span><span class="sxs-lookup"><span data-stu-id="4e757-138">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="4e757-139">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="4e757-139">November 14, 2017</span></span>

<span data-ttu-id="4e757-140">版本 2.0.21</span><span class="sxs-lookup"><span data-stu-id="4e757-140">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="4e757-141">ACR</span><span class="sxs-lookup"><span data-stu-id="4e757-141">ACR</span></span>

* <span data-ttu-id="4e757-142">添加了在复制区域中创建 Webhook 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-142">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="4e757-143">ACS</span><span class="sxs-lookup"><span data-stu-id="4e757-143">ACS</span></span>

* <span data-ttu-id="4e757-144">已在 AKS 中将所有“代理”一词更改为“节点”</span><span class="sxs-lookup"><span data-stu-id="4e757-144">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="4e757-145">弃用了 `acs create` 的 `--orchestrator-release` 选项</span><span class="sxs-lookup"><span data-stu-id="4e757-145">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="4e757-146">已将 AKS 的默认 VM 大小更改为 `Standard_D1_v2`</span><span class="sxs-lookup"><span data-stu-id="4e757-146">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="4e757-147">在 Windows 上修复了 `az aks browse`</span><span class="sxs-lookup"><span data-stu-id="4e757-147">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="4e757-148">在 Windows 上修复了 `az aks get-credentials`</span><span class="sxs-lookup"><span data-stu-id="4e757-148">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="4e757-149">应用服务</span><span class="sxs-lookup"><span data-stu-id="4e757-149">Appservice</span></span>

* <span data-ttu-id="4e757-150">添加了 Web 应用和函数应用的部署源 `config-zip`</span><span class="sxs-lookup"><span data-stu-id="4e757-150">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="4e757-151">为 `az webapp log config` 添加了 `--docker-container-logging` 选项</span><span class="sxs-lookup"><span data-stu-id="4e757-151">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="4e757-152">从 `az webapp log config` 的参数 `--web-server-logging` 中删除了 `storage` 选项</span><span class="sxs-lookup"><span data-stu-id="4e757-152">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="4e757-153">完善了 `deployment user set` 的错误消息</span><span class="sxs-lookup"><span data-stu-id="4e757-153">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="4e757-154">添加了创建 Linux 函数应用的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-154">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="4e757-155">固定 `list-locations`</span><span class="sxs-lookup"><span data-stu-id="4e757-155">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="4e757-156">批处理</span><span class="sxs-lookup"><span data-stu-id="4e757-156">Batch</span></span>

* <span data-ttu-id="4e757-157">修复了在 pool create 命令中结合 `--image` 标志使用资源 ID 时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="4e757-157">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="4e757-158">Batchai</span><span class="sxs-lookup"><span data-stu-id="4e757-158">Batchai</span></span>

* <span data-ttu-id="4e757-159">在 `file-server create` 命令中提供了 `--vm-size` 的简短选项 `-s`（提供 VM 大小）</span><span class="sxs-lookup"><span data-stu-id="4e757-159">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="4e757-160">为 `cluster create` 参数添加了存储帐户名称和密钥自变量</span><span class="sxs-lookup"><span data-stu-id="4e757-160">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="4e757-161">纠正了 `job list-files` 和 `job stream-file` 的文档</span><span class="sxs-lookup"><span data-stu-id="4e757-161">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="4e757-162">在 `job create` 命令中提供了 `--cluster-name` 的简短选项 `-r`（提供群集名称）</span><span class="sxs-lookup"><span data-stu-id="4e757-162">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="4e757-163">云</span><span class="sxs-lookup"><span data-stu-id="4e757-163">Cloud</span></span>

* <span data-ttu-id="4e757-164">更改了 `cloud [register|update]`，以防止注册缺少所需终结点的云</span><span class="sxs-lookup"><span data-stu-id="4e757-164">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="4e757-165">容器</span><span class="sxs-lookup"><span data-stu-id="4e757-165">Container</span></span>

* <span data-ttu-id="4e757-166">添加了打开多个端口的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-166">Added support to open multiple ports</span></span>
* <span data-ttu-id="4e757-167">添加了容器组重启策略</span><span class="sxs-lookup"><span data-stu-id="4e757-167">Added container group restart policy</span></span>
* <span data-ttu-id="4e757-168">添加了将 Azure 文件共享装载为卷的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-168">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="4e757-169">更新了帮助器文档</span><span class="sxs-lookup"><span data-stu-id="4e757-169">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="4e757-170">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="4e757-170">Data Lake Analytics</span></span>

* <span data-ttu-id="4e757-171">更改了 `[job|account] list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="4e757-171">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="4e757-172">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4e757-172">Data Lake Store</span></span>

* <span data-ttu-id="4e757-173">更改了 `account list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="4e757-173">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="4e757-174">分机</span><span class="sxs-lookup"><span data-stu-id="4e757-174">Extension</span></span>

* <span data-ttu-id="4e757-175">添加了 `extension list-available` 用于列出官方的 Microsoft 扩展</span><span class="sxs-lookup"><span data-stu-id="4e757-175">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="4e757-176">为 `extension [add|update]` 添加了 `--name`，以便按名称安装扩展</span><span class="sxs-lookup"><span data-stu-id="4e757-176">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="4e757-177">IoT</span><span class="sxs-lookup"><span data-stu-id="4e757-177">IoT</span></span>

* <span data-ttu-id="4e757-178">添加了对证书颁发机构 (CA) 和证书链的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-178">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="4e757-179">监视</span><span class="sxs-lookup"><span data-stu-id="4e757-179">Monitor</span></span>

* <span data-ttu-id="4e757-180">添加了 `activity-log alert` 命令</span><span class="sxs-lookup"><span data-stu-id="4e757-180">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="4e757-181">网络</span><span class="sxs-lookup"><span data-stu-id="4e757-181">Network</span></span>

* <span data-ttu-id="4e757-182">添加了对 CAA DNS 记录的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-182">Added support for CAA DNS records</span></span>
* <span data-ttu-id="4e757-183">修复了无法使用 `traffic-manager profile update` 更新终结点的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-183">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="4e757-184">修复了在采用某种 VNET 创建方式时 `vnet update --dns-servers` 无法正常运行的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-184">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="4e757-185">修复了 `dns zone import` 错误导入相对 DNS 名称的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-185">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="4e757-186">保留</span><span class="sxs-lookup"><span data-stu-id="4e757-186">Reservations</span></span>

* <span data-ttu-id="4e757-187">初始预览版</span><span class="sxs-lookup"><span data-stu-id="4e757-187">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="4e757-188">资源</span><span class="sxs-lookup"><span data-stu-id="4e757-188">Resource</span></span>

* <span data-ttu-id="4e757-189">添加了在 `--resource` 参数中指定资源 ID 的支持，以及对资源级锁的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-189">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="4e757-190">SQL</span><span class="sxs-lookup"><span data-stu-id="4e757-190">SQL</span></span>

* <span data-ttu-id="4e757-191">为 `sql server vnet-rule [create|update]` 添加了 `--ignore-missing-vnet-service-endpoint` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-191">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="4e757-192">存储</span><span class="sxs-lookup"><span data-stu-id="4e757-192">Storage</span></span>

* <span data-ttu-id="4e757-193">更改了 `storage account create` 以使用 SKU `Standard_RAGRS` 作为默认值</span><span class="sxs-lookup"><span data-stu-id="4e757-193">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="4e757-194">修复了处理包含非 ASCII 字符的文件/Blob 名称时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="4e757-194">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="4e757-195">修复了阻止在 `storage [blob|file] copy start-batch` 中使用 `--source-uri` 的 bug</span><span class="sxs-lookup"><span data-stu-id="4e757-195">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="4e757-196">添加了在 `storage [blob|file] delete-batch` 中包含和删除多个对象的命令</span><span class="sxs-lookup"><span data-stu-id="4e757-196">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="4e757-197">修复了使用 `storage metrics update` 启用指标时出现的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-197">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="4e757-198">修复了使用 `storage blob upload-batch` 时，如果文件超过 200GB 所出现的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-198">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="4e757-199">修复了 `storage account [create|update]` 忽略 `--bypass` 和 `--default-action` 的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-199">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="4e757-200">VM</span><span class="sxs-lookup"><span data-stu-id="4e757-200">VM</span></span>

* <span data-ttu-id="4e757-201">修复了 `vmss create` 阻止使用 `Basic` 大小层的 bug</span><span class="sxs-lookup"><span data-stu-id="4e757-201">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="4e757-202">针对包含计费信息的自定义映像，为 `[vm|vmss] create` 添加了 `--plan` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-202">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="4e757-203">添加了 `vm secret `[add|remove|list]\` 命令</span><span class="sxs-lookup"><span data-stu-id="4e757-203">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="4e757-204">已将 `vm format-secret` 重命名为 `vm secret format`</span><span class="sxs-lookup"><span data-stu-id="4e757-204">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="4e757-205">为 `vm encryption enable` 添加了 `--encrypt format` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-205">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="4e757-206">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="4e757-206">October 24, 2017</span></span>

<span data-ttu-id="4e757-207">版本 2.0.20</span><span class="sxs-lookup"><span data-stu-id="4e757-207">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="4e757-208">核心</span><span class="sxs-lookup"><span data-stu-id="4e757-208">Core</span></span>

* <span data-ttu-id="4e757-209">已更新 `2017-03-09-profile` 以使用 `MGMT_STORAGE` API 版本 `2016-01-01`</span><span class="sxs-lookup"><span data-stu-id="4e757-209">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="4e757-210">ACR</span><span class="sxs-lookup"><span data-stu-id="4e757-210">ACR</span></span>

* <span data-ttu-id="4e757-211">已更新资源管理以指向 `2017-10-01` API 版本</span><span class="sxs-lookup"><span data-stu-id="4e757-211">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="4e757-212">已将“带来你自己的存储”SKU 更改为“经典”</span><span class="sxs-lookup"><span data-stu-id="4e757-212">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="4e757-213">已将注册表 SKU 重命名为“基本”、“标准”和“高级”</span><span class="sxs-lookup"><span data-stu-id="4e757-213">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="4e757-214">ACS</span><span class="sxs-lookup"><span data-stu-id="4e757-214">ACS</span></span>

* <span data-ttu-id="4e757-215">[PREVIEW] 添加了 `az aks` 命令</span><span class="sxs-lookup"><span data-stu-id="4e757-215">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="4e757-216">已修复 Kubernetes `get-credentials`</span><span class="sxs-lookup"><span data-stu-id="4e757-216">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="4e757-217">应用服务</span><span class="sxs-lookup"><span data-stu-id="4e757-217">Appservice</span></span>

* <span data-ttu-id="4e757-218">已修复所下载 `webapp` 日志可能无效的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-218">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="4e757-219">组件</span><span class="sxs-lookup"><span data-stu-id="4e757-219">Component</span></span>

* <span data-ttu-id="4e757-220">为所有安装程序添加了更清晰的弃用消息并添加了确认提示</span><span class="sxs-lookup"><span data-stu-id="4e757-220">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="4e757-221">监视</span><span class="sxs-lookup"><span data-stu-id="4e757-221">Monitor</span></span>

* <span data-ttu-id="4e757-222">添加了 `action-group` 命令</span><span class="sxs-lookup"><span data-stu-id="4e757-222">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="4e757-223">资源</span><span class="sxs-lookup"><span data-stu-id="4e757-223">Resource</span></span>

* <span data-ttu-id="4e757-224">修复了 `group export` 中与 msrest 依赖项的最新版本不兼容的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-224">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="4e757-225">修复了 `policy assignment create` 以使用内置策略定义和策略集定义</span><span class="sxs-lookup"><span data-stu-id="4e757-225">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="4e757-226">VM</span><span class="sxs-lookup"><span data-stu-id="4e757-226">VM</span></span>

* <span data-ttu-id="4e757-227">为 `vmss create` 添加了 `--accelerated-networking` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-227">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="4e757-228">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="4e757-228">October 9, 2017</span></span>

<span data-ttu-id="4e757-229">版本 2.0.19</span><span class="sxs-lookup"><span data-stu-id="4e757-229">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="4e757-230">核心</span><span class="sxs-lookup"><span data-stu-id="4e757-230">Core</span></span>

* <span data-ttu-id="4e757-231">在 Azure Stack 中添加了一个尾随斜杠用于处理 ADFS 机构 URL</span><span class="sxs-lookup"><span data-stu-id="4e757-231">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="4e757-232">应用服务</span><span class="sxs-lookup"><span data-stu-id="4e757-232">Appservice</span></span>

* <span data-ttu-id="4e757-233">添加了新命令 `webapp update` 用于执行常规更新</span><span class="sxs-lookup"><span data-stu-id="4e757-233">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="4e757-234">批处理</span><span class="sxs-lookup"><span data-stu-id="4e757-234">Batch</span></span>

* <span data-ttu-id="4e757-235">已更新为 Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="4e757-235">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="4e757-236">更新了 VirtualMachineConfiguration 的 `--image`，用于支持除 publish:offer:sku:version 以外的 ARM 映像引用</span><span class="sxs-lookup"><span data-stu-id="4e757-236">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="4e757-237">添加了对 Batch 扩展命令新 CLI 扩展模型的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-237">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="4e757-238">从组件模型中删除了 Batch 支持</span><span class="sxs-lookup"><span data-stu-id="4e757-238">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="4e757-239">Batchai</span><span class="sxs-lookup"><span data-stu-id="4e757-239">Batchai</span></span>

* <span data-ttu-id="4e757-240">Batch AI 模块初始版本</span><span class="sxs-lookup"><span data-stu-id="4e757-240">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="4e757-241">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4e757-241">Keyvault</span></span>

* <span data-ttu-id="4e757-242">修复了在 Azure Stack 中使用 ADFS 时发生的 Key Vault 身份验证问题。</span><span class="sxs-lookup"><span data-stu-id="4e757-242">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="4e757-243">(#4448)</span><span class="sxs-lookup"><span data-stu-id="4e757-243">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="4e757-244">网络</span><span class="sxs-lookup"><span data-stu-id="4e757-244">Network</span></span>

* <span data-ttu-id="4e757-245">已将 `application-gateway address-pool create` 的 `--server` 参数更改为可选，以允许空地址池</span><span class="sxs-lookup"><span data-stu-id="4e757-245">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="4e757-246">更新了 `traffic-manager` 以支持最新功能</span><span class="sxs-lookup"><span data-stu-id="4e757-246">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="4e757-247">资源</span><span class="sxs-lookup"><span data-stu-id="4e757-247">Resource</span></span>

* <span data-ttu-id="4e757-248">在 `group` 中添加了对资源组名称使用 `--resource-group/-g` 选项的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-248">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="4e757-249">为 `account lock` 添加了命令用于处理订阅级锁</span><span class="sxs-lookup"><span data-stu-id="4e757-249">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="4e757-250">为 `group lock` 添加了命令用于处理组级锁</span><span class="sxs-lookup"><span data-stu-id="4e757-250">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="4e757-251">为 `resource lock` 添加了命令用于处理资源级锁</span><span class="sxs-lookup"><span data-stu-id="4e757-251">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="4e757-252">Sql</span><span class="sxs-lookup"><span data-stu-id="4e757-252">Sql</span></span>

* <span data-ttu-id="4e757-253">添加了 SQL 透明数据加密 (TDE) 和自带密钥 TDE 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-253">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="4e757-254">添加了 `db list-deleted` 命令和 `db restore --deleted-time` 参数，以便能够找到和还原已删除的数据库</span><span class="sxs-lookup"><span data-stu-id="4e757-254">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="4e757-255">添加了 `db op list` 和 `db op cancel`，以便能够列出和取消正在对数据库执行的操作</span><span class="sxs-lookup"><span data-stu-id="4e757-255">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="4e757-256">存储</span><span class="sxs-lookup"><span data-stu-id="4e757-256">Storage</span></span>

* <span data-ttu-id="4e757-257">添加了对文件共享快照的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-257">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="4e757-258">Vm</span><span class="sxs-lookup"><span data-stu-id="4e757-258">Vm</span></span>

* <span data-ttu-id="4e757-259">修复了 `vm show` 中的一个 bug：在缺少专用 IP 地址的情况下使用 `-d` 会导致崩溃</span><span class="sxs-lookup"><span data-stu-id="4e757-259">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="4e757-260">[预览] 添加了滚动升级到 `vmss create` 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-260">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="4e757-261">添加了使用 `vm encryption enable` 更新加密设置的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-261">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="4e757-262">为 `vm create` 添加了 `--os-disk-size-gb` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-262">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="4e757-263">为 Windows 中的 `vmss create` 添加了 `--license-type` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-263">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="4e757-264">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="4e757-264">September 22, 2017</span></span>

<span data-ttu-id="4e757-265">版本 2.0.18</span><span class="sxs-lookup"><span data-stu-id="4e757-265">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="4e757-266">资源</span><span class="sxs-lookup"><span data-stu-id="4e757-266">Resource</span></span>

* <span data-ttu-id="4e757-267">添加了对显示内置策略定义的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-267">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="4e757-268">添加了用于创建策略定义的支持模式参数</span><span class="sxs-lookup"><span data-stu-id="4e757-268">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="4e757-269">为 `managedapp definition create` 添加了对 UI 定义和模板的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-269">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="4e757-270">[重大更改] 将 `managedapp` 资源类型从 `appliances` 更改到 `applications`，从 `applianceDefinitions` 更改到 `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="4e757-270">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="4e757-271">网络</span><span class="sxs-lookup"><span data-stu-id="4e757-271">Network</span></span>

* <span data-ttu-id="4e757-272">为 `network lb` 和 `network public-ip` 子命令添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-272">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="4e757-273">为 `express-route` 添加了对 IPv6 Microsoft 对等互连的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-273">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="4e757-274">添加了 `asg` 应用程序安全组命令</span><span class="sxs-lookup"><span data-stu-id="4e757-274">Added `asg` application security group commands</span></span>
* <span data-ttu-id="4e757-275">为 `nic [create|ip-config create|ip-config update]` 添加了 `--application-security-groups` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-275">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="4e757-276">为 `nsg rule [create|update]` 添加了 `--source-asgs` 和 `--destination-asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-276">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="4e757-277">为 `vnet [create|update]` 添加了 `--ddos-protection` 和 `--vm-protection` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-277">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="4e757-278">添加了 `network [vnet-gateway|vpn-client|show-url]` 命令</span><span class="sxs-lookup"><span data-stu-id="4e757-278">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="4e757-279">存储</span><span class="sxs-lookup"><span data-stu-id="4e757-279">Storage</span></span>

* <span data-ttu-id="4e757-280">已修复了 `storage account network-rule` 命令在更新 SDK 后可能会失败的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-280">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="4e757-281">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="4e757-281">Eventgrid</span></span>

* <span data-ttu-id="4e757-282">更新了 Azure 事件网格 Python SDK 以使用较新的 API 版本“2017-09-15-preview”</span><span class="sxs-lookup"><span data-stu-id="4e757-282">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="4e757-283">SQL</span><span class="sxs-lookup"><span data-stu-id="4e757-283">SQL</span></span>

* <span data-ttu-id="4e757-284">将 `sql server list` 的参数 `--resource-group` 更改为可选。</span><span class="sxs-lookup"><span data-stu-id="4e757-284">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="4e757-285">如果未指定，将返回订阅中的所有 SQL 服务器</span><span class="sxs-lookup"><span data-stu-id="4e757-285">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="4e757-286">为 `db [create|copy|restore|update|replica create|create|update]` 和 `dw [create|update]` 添加了 `--no-wait` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-286">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="4e757-287">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4e757-287">Keyvault</span></span>

* <span data-ttu-id="4e757-288">添加了对从代理后执行 Keyvault 命令的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-288">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="4e757-289">VM</span><span class="sxs-lookup"><span data-stu-id="4e757-289">VM</span></span>

* <span data-ttu-id="4e757-290">为 `[vm|vmss|disk] create` 添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-290">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="4e757-291">已修复了将 `--app-gateway ID` 与 `vmss create` 一起使用会导致故障的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-291">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="4e757-292">为 `vm create` 添加了 `--asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-292">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="4e757-293">添加了对使用 `vm run-command` 在 VM 上运行命令的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-293">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="4e757-294">[预览] 添加了对使用 `vmss encryption` 进行 VMSS 磁盘加密的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-294">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="4e757-295">添加了对使用 `vm perform-maintenance` 在 VM 上执行维护的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-295">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="4e757-296">ACS</span><span class="sxs-lookup"><span data-stu-id="4e757-296">ACS</span></span>

* <span data-ttu-id="4e757-297">[预览] 为适用于 ACS 预览区域的 `acs create` 添加了 `--orchestrator-release` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-297">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="4e757-298">应用服务</span><span class="sxs-lookup"><span data-stu-id="4e757-298">Appservice</span></span>

* <span data-ttu-id="4e757-299">添加了使用 `webapp auth [update|show]` 更新和显示身份验证设置的功能</span><span class="sxs-lookup"><span data-stu-id="4e757-299">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="4e757-300">备份</span><span class="sxs-lookup"><span data-stu-id="4e757-300">Backup</span></span>

* <span data-ttu-id="4e757-301">预览版</span><span class="sxs-lookup"><span data-stu-id="4e757-301">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="4e757-302">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="4e757-302">September 11, 2017</span></span>

<span data-ttu-id="4e757-303">版本 2.0.17</span><span class="sxs-lookup"><span data-stu-id="4e757-303">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="4e757-304">核心</span><span class="sxs-lookup"><span data-stu-id="4e757-304">Core</span></span>

* <span data-ttu-id="4e757-305">启用了命令模块在遥测中设置其自己的相关 ID</span><span class="sxs-lookup"><span data-stu-id="4e757-305">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="4e757-306">修复了在遥测设置为诊断模式时的 JSON 转储问题</span><span class="sxs-lookup"><span data-stu-id="4e757-306">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="4e757-307">Acs</span><span class="sxs-lookup"><span data-stu-id="4e757-307">Acs</span></span>

* <span data-ttu-id="4e757-308">添加了 `acs list-locations` 命令</span><span class="sxs-lookup"><span data-stu-id="4e757-308">Added `acs list-locations` command</span></span>
* <span data-ttu-id="4e757-309">使 `ssh-key-file` 附带预期的默认值</span><span class="sxs-lookup"><span data-stu-id="4e757-309">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="4e757-310">应用服务</span><span class="sxs-lookup"><span data-stu-id="4e757-310">Appservice</span></span>

* <span data-ttu-id="4e757-311">添加了在未包含活动服务计划的资源组中创建 Web 应用的功能</span><span class="sxs-lookup"><span data-stu-id="4e757-311">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="4e757-312">CDN</span><span class="sxs-lookup"><span data-stu-id="4e757-312">CDN</span></span>

* <span data-ttu-id="4e757-313">修复了 `cdn custom-domain create` 的“CustomDomain 不可迭代” bug。</span><span class="sxs-lookup"><span data-stu-id="4e757-313">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="4e757-314">分机</span><span class="sxs-lookup"><span data-stu-id="4e757-314">Extension</span></span>

* <span data-ttu-id="4e757-315">初始版本。</span><span class="sxs-lookup"><span data-stu-id="4e757-315">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="4e757-316">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4e757-316">Keyvault</span></span>

* <span data-ttu-id="4e757-317">修复了 `keyvault set-policy` 的权限区分大小写的问题。</span><span class="sxs-lookup"><span data-stu-id="4e757-317">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="4e757-318">网络</span><span class="sxs-lookup"><span data-stu-id="4e757-318">Network</span></span>

* <span data-ttu-id="4e757-319">已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="4e757-319">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="4e757-320">已为 `vnet subnet create/update` 将 `--private-access-services` 参数重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="4e757-320">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="4e757-321">在 `nsg rule create/update` 中添加了对多个 IP 范围和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-321">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="4e757-322">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-322">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="4e757-323">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-323">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="4e757-324">资源</span><span class="sxs-lookup"><span data-stu-id="4e757-324">Resource</span></span>

* <span data-ttu-id="4e757-325">允许在 `policy definition create` 和 `policy definition update` 中传入资源策略参数定义</span><span class="sxs-lookup"><span data-stu-id="4e757-325">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="4e757-326">允许为 `policy assignment create` 传入参数值</span><span class="sxs-lookup"><span data-stu-id="4e757-326">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="4e757-327">允许为所有参数传入 JSON 或文件</span><span class="sxs-lookup"><span data-stu-id="4e757-327">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="4e757-328">更新了 API 版本</span><span class="sxs-lookup"><span data-stu-id="4e757-328">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="4e757-329">SQL</span><span class="sxs-lookup"><span data-stu-id="4e757-329">SQL</span></span>

* <span data-ttu-id="4e757-330">添加了 `sql server vnet-rule` 命令</span><span class="sxs-lookup"><span data-stu-id="4e757-330">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="4e757-331">VM</span><span class="sxs-lookup"><span data-stu-id="4e757-331">VM</span></span>

* <span data-ttu-id="4e757-332">已修复：除非提供 `--scope`，否则不分配访问权限</span><span class="sxs-lookup"><span data-stu-id="4e757-332">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="4e757-333">已修复：使用与门户相同的扩展命名</span><span class="sxs-lookup"><span data-stu-id="4e757-333">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="4e757-334">已从 `[vm|vmss] create` 输出中删除了 `subscription`</span><span class="sxs-lookup"><span data-stu-id="4e757-334">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="4e757-335">已修复：`[vm|vmss] create` SKU 无法应用于带映像的数据磁盘</span><span class="sxs-lookup"><span data-stu-id="4e757-335">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="4e757-336">已修复：`vm format-secret --secrets` 不接受新行分隔的 ID</span><span class="sxs-lookup"><span data-stu-id="4e757-336">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="4e757-337">2017 年 8 月31 日</span><span class="sxs-lookup"><span data-stu-id="4e757-337">August 31, 2017</span></span>

<span data-ttu-id="4e757-338">版本 2.0.16</span><span class="sxs-lookup"><span data-stu-id="4e757-338">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="4e757-339">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4e757-339">Keyvault</span></span>

* <span data-ttu-id="4e757-340">修复了在尝试使用 `secret download` 自动解析机密编码时的 bug</span><span class="sxs-lookup"><span data-stu-id="4e757-340">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="4e757-341">Sf</span><span class="sxs-lookup"><span data-stu-id="4e757-341">Sf</span></span>

* <span data-ttu-id="4e757-342">弃用所有支持 Service Fabric CLI (sfctl) 的命令</span><span class="sxs-lookup"><span data-stu-id="4e757-342">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="4e757-343">存储</span><span class="sxs-lookup"><span data-stu-id="4e757-343">Storage</span></span>

* <span data-ttu-id="4e757-344">修复了无法在不支持 NetworkACLs 功能的区域中创建存储帐户的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-344">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="4e757-345">在 Blob 和文件上载过程中确定内容类型和内容编码（如果既未指定内容类型，也未指定内容编码）</span><span class="sxs-lookup"><span data-stu-id="4e757-345">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="4e757-346">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="4e757-346">August 28, 2017</span></span>

<span data-ttu-id="4e757-347">版本 2.0.15</span><span class="sxs-lookup"><span data-stu-id="4e757-347">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="4e757-348">CLI</span><span class="sxs-lookup"><span data-stu-id="4e757-348">CLI</span></span>

* <span data-ttu-id="4e757-349">在 `--version` 中添加了法律说明。</span><span class="sxs-lookup"><span data-stu-id="4e757-349">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="4e757-350">ACS</span><span class="sxs-lookup"><span data-stu-id="4e757-350">ACS</span></span>

* <span data-ttu-id="4e757-351">更正了预览区域。</span><span class="sxs-lookup"><span data-stu-id="4e757-351">Corrected preview regions.</span></span>
* <span data-ttu-id="4e757-352">正确设置了默认 `dns_name_prefix` 的格式。</span><span class="sxs-lookup"><span data-stu-id="4e757-352">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="4e757-353">优化了 acs 命令输出。</span><span class="sxs-lookup"><span data-stu-id="4e757-353">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="4e757-354">应用服务</span><span class="sxs-lookup"><span data-stu-id="4e757-354">Appservice</span></span>

* <span data-ttu-id="4e757-355">[重大更改] 修复了 `az webapp config appsettings [delete|set]` 输出中的不一致问题</span><span class="sxs-lookup"><span data-stu-id="4e757-355">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="4e757-356">为 `az webapp config container set --docker-custom-image-name` 的 `-i` 添加了新别名</span><span class="sxs-lookup"><span data-stu-id="4e757-356">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="4e757-357">公开了 `az webapp log show`</span><span class="sxs-lookup"><span data-stu-id="4e757-357">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="4e757-358">公开了 `az webapp delete` 中的新参数，用于保留应用服务计划、指标或 dns 注册</span><span class="sxs-lookup"><span data-stu-id="4e757-358">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="4e757-359">已修复：正确检测槽位设置</span><span class="sxs-lookup"><span data-stu-id="4e757-359">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="4e757-360">IoT</span><span class="sxs-lookup"><span data-stu-id="4e757-360">IoT</span></span>

* <span data-ttu-id="4e757-361">修复了 #3934：策略创建操作不再清除现有的策略</span><span class="sxs-lookup"><span data-stu-id="4e757-361">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="4e757-362">网络</span><span class="sxs-lookup"><span data-stu-id="4e757-362">Network</span></span>

* <span data-ttu-id="4e757-363">[重大更改] 已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="4e757-363">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="4e757-364">[重大更改] 已将 `vnet subnet [create|update]` 的选项 `--private-access-services` 重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="4e757-364">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="4e757-365">在 `nsg rule [create|update]` 中添加了对多个 IP 和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-365">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="4e757-366">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-366">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="4e757-367">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-367">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="4e757-368">配置文件</span><span class="sxs-lookup"><span data-stu-id="4e757-368">Profile</span></span>

* <span data-ttu-id="4e757-369">公开了 `--msi` 和 `--msi-port`，以便使用虚拟机的标识登录</span><span class="sxs-lookup"><span data-stu-id="4e757-369">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="4e757-370">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="4e757-370">Service Fabric</span></span>

* <span data-ttu-id="4e757-371">预览版</span><span class="sxs-lookup"><span data-stu-id="4e757-371">Preview release</span></span>
* <span data-ttu-id="4e757-372">简化了命令的注册表用户/密码规则</span><span class="sxs-lookup"><span data-stu-id="4e757-372">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="4e757-373">修复了即使在参数中传入了密码，也提示用户输入密码的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-373">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="4e757-374">添加了对空 `registry_cred` 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-374">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="4e757-375">存储</span><span class="sxs-lookup"><span data-stu-id="4e757-375">Storage</span></span>

* <span data-ttu-id="4e757-376">启用了设置 Blob 层</span><span class="sxs-lookup"><span data-stu-id="4e757-376">Enabled setting blob tier</span></span>
* <span data-ttu-id="4e757-377">为 `storage account [create|update]` 添加了 `--bypass` 和 `--default-action` 参数用于支持服务隧道</span><span class="sxs-lookup"><span data-stu-id="4e757-377">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="4e757-378">添加了用于在 `storage account network-rule` 中添加 VNET 规则和基于 IP 的规则的命令</span><span class="sxs-lookup"><span data-stu-id="4e757-378">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="4e757-379">启用了使用客户管理的密钥进行服务加密的功能</span><span class="sxs-lookup"><span data-stu-id="4e757-379">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="4e757-380">[重大更改] 已将 `az storage account create and az storage account update` 命令的选项 `--encryption` 重命名为 `--encryption-services`</span><span class="sxs-lookup"><span data-stu-id="4e757-380">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="4e757-381">修复了 #4220：`az storage account update encryption` - 语法不匹配</span><span class="sxs-lookup"><span data-stu-id="4e757-381">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="4e757-382">VM</span><span class="sxs-lookup"><span data-stu-id="4e757-382">VM</span></span>

* <span data-ttu-id="4e757-383">修复了使用 `--instance-id *` 时，针对 `vmss get-instance-view` 显示多余且错误的信息的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-383">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="4e757-384">在 `vmss create` 中添加了对 `--lb-sku` 的支持：</span><span class="sxs-lookup"><span data-stu-id="4e757-384">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="4e757-385">从 `[vm|vmss] create` 的管理员名称方块列表中删除了人员名称</span><span class="sxs-lookup"><span data-stu-id="4e757-385">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="4e757-386">修复了当无法从映像中提取计划信息时，`[vm|vmss] create` 引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-386">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="4e757-387">修复了创建包含内部 LB 的 vmms 规模集时发生崩溃的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-387">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="4e757-388">修复了 `--no-wait` 参数无法配合 `vm availability-set create` 工作的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-388">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="4e757-389">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="4e757-389">August 15, 2017</span></span>

<span data-ttu-id="4e757-390">版本 2.0.14</span><span class="sxs-lookup"><span data-stu-id="4e757-390">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="4e757-391">ACS</span><span class="sxs-lookup"><span data-stu-id="4e757-391">ACS</span></span>

* <span data-ttu-id="4e757-392">更正了 kubernetes 的 sshMaster0 端口号</span><span class="sxs-lookup"><span data-stu-id="4e757-392">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="4e757-393">应用服务</span><span class="sxs-lookup"><span data-stu-id="4e757-393">Appservice</span></span>

* <span data-ttu-id="4e757-394">修复了创建基于新 Git 的 Linux Web 应用时发生异常的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-394">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="4e757-395">事件网格</span><span class="sxs-lookup"><span data-stu-id="4e757-395">Event Grid</span></span>

* <span data-ttu-id="4e757-396">添加了 SDK 依赖项</span><span class="sxs-lookup"><span data-stu-id="4e757-396">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="4e757-397">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="4e757-397">August 11, 2017</span></span>

<span data-ttu-id="4e757-398">版本 2.0.13</span><span class="sxs-lookup"><span data-stu-id="4e757-398">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="4e757-399">ACS</span><span class="sxs-lookup"><span data-stu-id="4e757-399">ACS</span></span>

* <span data-ttu-id="4e757-400">添加了更多预览区域</span><span class="sxs-lookup"><span data-stu-id="4e757-400">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="4e757-401">批处理</span><span class="sxs-lookup"><span data-stu-id="4e757-401">Batch</span></span>

* <span data-ttu-id="4e757-402">已更新到 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="4e757-402">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="4e757-403">添加了新命令用于显示作业的任务计数</span><span class="sxs-lookup"><span data-stu-id="4e757-403">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="4e757-404">修复了处理资源文件 SAS URL 时的 bug</span><span class="sxs-lookup"><span data-stu-id="4e757-404">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="4e757-405">Batch 帐户终结点现在支持可选的“https://” 前缀</span><span class="sxs-lookup"><span data-stu-id="4e757-405">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="4e757-406">支持将包含 100 多个任务的列表添加到作业</span><span class="sxs-lookup"><span data-stu-id="4e757-406">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="4e757-407">添加了加载扩展命令模块的调试日志记录</span><span class="sxs-lookup"><span data-stu-id="4e757-407">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="4e757-408">组件</span><span class="sxs-lookup"><span data-stu-id="4e757-408">Component</span></span>

* <span data-ttu-id="4e757-409">为“az component”命令添加了弃用警告</span><span class="sxs-lookup"><span data-stu-id="4e757-409">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="4e757-410">容器</span><span class="sxs-lookup"><span data-stu-id="4e757-410">Container</span></span>

* <span data-ttu-id="4e757-411">`create`：修复了某个环境变量中不允许等于号的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-411">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="4e757-412">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4e757-412">Data Lake Store</span></span>

* <span data-ttu-id="4e757-413">启用了进度控件</span><span class="sxs-lookup"><span data-stu-id="4e757-413">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="4e757-414">事件网格</span><span class="sxs-lookup"><span data-stu-id="4e757-414">Event Grid</span></span>

* <span data-ttu-id="4e757-415">初始版本</span><span class="sxs-lookup"><span data-stu-id="4e757-415">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="4e757-416">网络</span><span class="sxs-lookup"><span data-stu-id="4e757-416">Network</span></span>

* <span data-ttu-id="4e757-417">`lb`：修复了某些子资源名称在省略时无法正确解析的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-417">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="4e757-418">`application-gateway {subresource} delete`：修复了不遵循 `--no-wait` 的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-418">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="4e757-419">`application-gateway http-settings update`：修复了无法关闭 `--connection-draining-timeout` 的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-419">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="4e757-420">修复了 `az network vpn-connection ipsec-policy add` 包含意外关键字参数 `sa_data_size_kilobyes` 的错误</span><span class="sxs-lookup"><span data-stu-id="4e757-420">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="4e757-421">配置文件</span><span class="sxs-lookup"><span data-stu-id="4e757-421">Profile</span></span>

* <span data-ttu-id="4e757-422">`account list`：添加了 `--refresh` 用于从服务器同步最新订阅</span><span class="sxs-lookup"><span data-stu-id="4e757-422">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="4e757-423">存储</span><span class="sxs-lookup"><span data-stu-id="4e757-423">Storage</span></span>

* <span data-ttu-id="4e757-424">启用了使用系统分配的标识更新存储帐户的功能</span><span class="sxs-lookup"><span data-stu-id="4e757-424">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="4e757-425">VM</span><span class="sxs-lookup"><span data-stu-id="4e757-425">VM</span></span>

* <span data-ttu-id="4e757-426">`availability-set`：公开了转换时的容错域计数</span><span class="sxs-lookup"><span data-stu-id="4e757-426">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="4e757-427">公开了 `list-skus` 命令</span><span class="sxs-lookup"><span data-stu-id="4e757-427">Exposed `list-skus` command</span></span>
* <span data-ttu-id="4e757-428">支持在不创建角色分配的情况下分配标识</span><span class="sxs-lookup"><span data-stu-id="4e757-428">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="4e757-429">附加数据磁盘时应用存储 SKU</span><span class="sxs-lookup"><span data-stu-id="4e757-429">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="4e757-430">删除了使用托管磁盘时的默认 OS 磁盘名称和存储 SKU</span><span class="sxs-lookup"><span data-stu-id="4e757-430">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="4e757-431">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="4e757-431">July 28, 2017</span></span>

<span data-ttu-id="4e757-432">版本 2.0.12</span><span class="sxs-lookup"><span data-stu-id="4e757-432">Version 2.0.12</span></span>

* <span data-ttu-id="4e757-433">添加了容器命令</span><span class="sxs-lookup"><span data-stu-id="4e757-433">Added container commands</span></span>
* <span data-ttu-id="4e757-434">添加了计费和消耗模块</span><span class="sxs-lookup"><span data-stu-id="4e757-434">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="4e757-435">核心</span><span class="sxs-lookup"><span data-stu-id="4e757-435">Core</span></span>

* <span data-ttu-id="4e757-436">输出包含证书的服务主体的 SDK 身份验证信息</span><span class="sxs-lookup"><span data-stu-id="4e757-436">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="4e757-437">修复了部署进度异常</span><span class="sxs-lookup"><span data-stu-id="4e757-437">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="4e757-438">使用当前云中的 arm 终结点创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="4e757-438">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="4e757-439">改进了 clouds.config 文件的并发处理 (#3636)</span><span class="sxs-lookup"><span data-stu-id="4e757-439">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="4e757-440">刷新每个命令执行进程的客户端请求 ID</span><span class="sxs-lookup"><span data-stu-id="4e757-440">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="4e757-441">使用适当的 SDK 配置文件创建订阅客户端 (#3635)</span><span class="sxs-lookup"><span data-stu-id="4e757-441">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="4e757-442">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="4e757-442">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="4e757-443">添加了通过 jmespath 查询选择表输出字段的支持 (#3581)</span><span class="sxs-lookup"><span data-stu-id="4e757-443">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="4e757-444">改进了分析参数的静默和包含手势的追加历史记录 (#3434)</span><span class="sxs-lookup"><span data-stu-id="4e757-444">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="4e757-445">使用适当的 SDK 配置文件创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="4e757-445">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="4e757-446">将所有现有记录文件移到最新的文件夹</span><span class="sxs-lookup"><span data-stu-id="4e757-446">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="4e757-447">修复了 VM/VMSS 创建操作的幂等性 (#3586)</span><span class="sxs-lookup"><span data-stu-id="4e757-447">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="4e757-448">命令路径不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="4e757-448">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="4e757-449">某些布尔类型的参数不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="4e757-449">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="4e757-450">支持登录到 Azure Stack 等本地服务器上的 ADFS</span><span class="sxs-lookup"><span data-stu-id="4e757-450">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="4e757-451">修复了并发写入 clouds.config 的问题 (#3255)</span><span class="sxs-lookup"><span data-stu-id="4e757-451">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="4e757-452">ACR</span><span class="sxs-lookup"><span data-stu-id="4e757-452">ACR</span></span>

* <span data-ttu-id="4e757-453">针对托管注册表添加了 `show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="4e757-453">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="4e757-454">支持托管注册表的 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="4e757-454">Support SKU update for managed registries</span></span>
* <span data-ttu-id="4e757-455">添加了包含托管 SKU 的托管注册表</span><span class="sxs-lookup"><span data-stu-id="4e757-455">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="4e757-456">通过 ACR Webhook 命令模块添加了托管注册表的 Webhook</span><span class="sxs-lookup"><span data-stu-id="4e757-456">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="4e757-457">添加了使用 acr login 命令进行 AAD 身份验证的功能</span><span class="sxs-lookup"><span data-stu-id="4e757-457">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="4e757-458">添加了 Docker 存储库、清单和标记的 delete 命令</span><span class="sxs-lookup"><span data-stu-id="4e757-458">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="4e757-459">ACS</span><span class="sxs-lookup"><span data-stu-id="4e757-459">ACS</span></span>

* <span data-ttu-id="4e757-460">API 版本 2017-07-01 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-460">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="4e757-461">应用服务</span><span class="sxs-lookup"><span data-stu-id="4e757-461">Appservice</span></span>

* <span data-ttu-id="4e757-462">修复了列出 Linux Web 应用时不返回任何内容的 bug</span><span class="sxs-lookup"><span data-stu-id="4e757-462">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="4e757-463">支持从 ACR 检索凭据</span><span class="sxs-lookup"><span data-stu-id="4e757-463">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="4e757-464">删除 `appservice web` 下的所有命令</span><span class="sxs-lookup"><span data-stu-id="4e757-464">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="4e757-465">将命令输出中的 Docker 注册表密码掩码 (#3656)</span><span class="sxs-lookup"><span data-stu-id="4e757-465">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="4e757-466">确保在 macOS 上使用默认浏览器且不出错 (#3623)</span><span class="sxs-lookup"><span data-stu-id="4e757-466">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="4e757-467">改进了 `webapp log tail` 和 `webapp log download` 的帮助 (#3624)</span><span class="sxs-lookup"><span data-stu-id="4e757-467">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="4e757-468">公开了 `traffic-routing` 命令用于配置静态路由 (#3566)</span><span class="sxs-lookup"><span data-stu-id="4e757-468">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="4e757-469">添加了用于配置源代码管理的可靠性修复 (#3245)</span><span class="sxs-lookup"><span data-stu-id="4e757-469">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="4e757-470">从 `webapp config update` 中删除了 Windows Web 应用不支持的 `--node-version` 参数。</span><span class="sxs-lookup"><span data-stu-id="4e757-470">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="4e757-471">需改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`。</span><span class="sxs-lookup"><span data-stu-id="4e757-471">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="4e757-472">批处理</span><span class="sxs-lookup"><span data-stu-id="4e757-472">Batch</span></span>

* <span data-ttu-id="4e757-473">已更新到 Batch SDK 3.0.0，支持池中的低优先级 VM</span><span class="sxs-lookup"><span data-stu-id="4e757-473">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="4e757-474">已将 `pool create` 选项 `--target-dedicated` 重命名为 `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="4e757-474">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="4e757-475">添加了 `pool create` 选项 `--target-low-priority-nodes` 和 `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="4e757-475">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="4e757-476">CDN</span><span class="sxs-lookup"><span data-stu-id="4e757-476">CDN</span></span>

* <span data-ttu-id="4e757-477">当 `--profile-name` 指定的配置文件不存在时，针对 `cdn endpoint list` 提供更完善的错误消息。</span><span class="sxs-lookup"><span data-stu-id="4e757-477">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="4e757-478">云</span><span class="sxs-lookup"><span data-stu-id="4e757-478">Cloud</span></span>

* <span data-ttu-id="4e757-479">已将云元数据终结点的 API 版本更改为 YYYY-MM-DD 格式</span><span class="sxs-lookup"><span data-stu-id="4e757-479">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="4e757-480">不需要库终结点</span><span class="sxs-lookup"><span data-stu-id="4e757-480">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="4e757-481">支持只将云注册到 ARM 资源管理器终结点</span><span class="sxs-lookup"><span data-stu-id="4e757-481">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="4e757-482">提供 `cloud set` 的选项用于在选择当前云时选择配置文件</span><span class="sxs-lookup"><span data-stu-id="4e757-482">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="4e757-483">公开了 `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="4e757-483">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4e757-484">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="4e757-484">CosmosDB</span></span>

* <span data-ttu-id="4e757-485">修复了允许使用自定义分区键创建集合的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-485">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="4e757-486">添加了对集合默认 TTL 的支持。</span><span class="sxs-lookup"><span data-stu-id="4e757-486">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="4e757-487">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="4e757-487">Data Lake Analytics</span></span>

* <span data-ttu-id="4e757-488">在 `dla account compute-policy` 标题下添加了用于计算策略管理的命令</span><span class="sxs-lookup"><span data-stu-id="4e757-488">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="4e757-489">添加了 `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="4e757-489">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="4e757-490">添加了 `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="4e757-490">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="4e757-491">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4e757-491">Data Lake Store</span></span>

* <span data-ttu-id="4e757-492">在 `dls account update` 中添加了用户管理的 Key Vault 密钥轮换的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-492">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="4e757-493">更新了底层 Data Lake Store 文件系统 SDK 版本，解决了一个性能问题</span><span class="sxs-lookup"><span data-stu-id="4e757-493">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="4e757-494">添加了命令 `dls enable-key-vault`。</span><span class="sxs-lookup"><span data-stu-id="4e757-494">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="4e757-495">此命令尝试使用用户提供的 Key Vault 加密 Data Lake Store 帐户中的数据</span><span class="sxs-lookup"><span data-stu-id="4e757-495">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="4e757-496">交互</span><span class="sxs-lookup"><span data-stu-id="4e757-496">Interactive</span></span>

* <span data-ttu-id="4e757-497">使用缓存的命令改进启动时间</span><span class="sxs-lookup"><span data-stu-id="4e757-497">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="4e757-498">增大了测试覆盖率</span><span class="sxs-lookup"><span data-stu-id="4e757-498">Increased test coverage</span></span>
* <span data-ttu-id="4e757-499">增强了“?”手势，使之也可注入到下一条命令</span><span class="sxs-lookup"><span data-stu-id="4e757-499">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="4e757-500">修复了配置文件 2017-03-09-profile-preview 的交互错误 (#3587)</span><span class="sxs-lookup"><span data-stu-id="4e757-500">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="4e757-501">允许使用 `--version` 作为交互模式的参数 (#3645)</span><span class="sxs-lookup"><span data-stu-id="4e757-501">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="4e757-502">阻止交互模式在验证填写内容中引发错误 (#3570)</span><span class="sxs-lookup"><span data-stu-id="4e757-502">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="4e757-503">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="4e757-503">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="4e757-504">添加了 `--progress` 标志</span><span class="sxs-lookup"><span data-stu-id="4e757-504">Added `--progress` flag</span></span>
* <span data-ttu-id="4e757-505">从填写内容中删除了 `--debug` 和 `--verbose`</span><span class="sxs-lookup"><span data-stu-id="4e757-505">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="4e757-506">从填写内容中删除了 `interactive` (#3324)</span><span class="sxs-lookup"><span data-stu-id="4e757-506">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="4e757-507">IoT</span><span class="sxs-lookup"><span data-stu-id="4e757-507">IoT</span></span>

* <span data-ttu-id="4e757-508">修复了策略创建操作不再清除现有策略的问题。</span><span class="sxs-lookup"><span data-stu-id="4e757-508">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="4e757-509">(#3934)</span><span class="sxs-lookup"><span data-stu-id="4e757-509">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="4e757-510">密钥保管库</span><span class="sxs-lookup"><span data-stu-id="4e757-510">Key vault</span></span>

* <span data-ttu-id="4e757-511">添加了 Key Vault 恢复功能的命令：</span><span class="sxs-lookup"><span data-stu-id="4e757-511">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="4e757-512">`keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="4e757-512">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="4e757-513">`keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="4e757-513">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="4e757-514">`keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="4e757-514">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="4e757-515">`keyvault key` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="4e757-515">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="4e757-516">添加了服务主体的 Key Vault 集成 (#3133)</span><span class="sxs-lookup"><span data-stu-id="4e757-516">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="4e757-517">已将 Key Vault 数据平面更新到 0.3.2。</span><span class="sxs-lookup"><span data-stu-id="4e757-517">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="4e757-518">(#3307)</span><span class="sxs-lookup"><span data-stu-id="4e757-518">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="4e757-519">实验室</span><span class="sxs-lookup"><span data-stu-id="4e757-519">Lab</span></span>

* <span data-ttu-id="4e757-520">添加了通过 `az lab vm claim` 在实验室中声明任何 VM 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-520">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="4e757-521">为 `az lab vm list` 和 `az lab vm show` 添加了表输出格式化程序</span><span class="sxs-lookup"><span data-stu-id="4e757-521">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="4e757-522">监视</span><span class="sxs-lookup"><span data-stu-id="4e757-522">Monitor</span></span>

* <span data-ttu-id="4e757-523">修复了与 `monitor autoscale-settings get-parameters-template` 命令结合使用的模板文件 (#3349)</span><span class="sxs-lookup"><span data-stu-id="4e757-523">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="4e757-524">已将 `monitor alert-rule-incidents list` 重命名为 `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="4e757-524">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="4e757-525">已将 `monitor alert-rule-incidents show` 重命名为 `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="4e757-525">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="4e757-526">已将 `monitor metric-defintions list` 重命名为 `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="4e757-526">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="4e757-527">已将 `monitor alert-rules` 重命名为 `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="4e757-527">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="4e757-528">更改了 `monitor alert create`：</span><span class="sxs-lookup"><span data-stu-id="4e757-528">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="4e757-529">`condition` 和 `action` 子命令不再接受 JSON</span><span class="sxs-lookup"><span data-stu-id="4e757-529">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="4e757-530">添加了大量的参数来简化规则创建过程</span><span class="sxs-lookup"><span data-stu-id="4e757-530">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="4e757-531">`location` 不再是必需的</span><span class="sxs-lookup"><span data-stu-id="4e757-531">`location` no longer required</span></span>
  * <span data-ttu-id="4e757-532">添加了目标的名称和 ID 支持</span><span class="sxs-lookup"><span data-stu-id="4e757-532">Add name and ID support for target</span></span>
  * <span data-ttu-id="4e757-533">删除了 `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="4e757-533">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="4e757-534">`is-enabled` 重命名为 `enabled`，不再是必需的</span><span class="sxs-lookup"><span data-stu-id="4e757-534">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="4e757-535">`description` 默认值现在基于提供的条件</span><span class="sxs-lookup"><span data-stu-id="4e757-535">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="4e757-536">添加了示例用于帮助澄清新格式</span><span class="sxs-lookup"><span data-stu-id="4e757-536">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="4e757-537">支持在 `monitor metric` 命令中使用名称或 ID</span><span class="sxs-lookup"><span data-stu-id="4e757-537">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="4e757-538">为 `monitor alert rule update` 添加了方便的参数和示例</span><span class="sxs-lookup"><span data-stu-id="4e757-538">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="4e757-539">网络</span><span class="sxs-lookup"><span data-stu-id="4e757-539">Network</span></span>

* <span data-ttu-id="4e757-540">添加了 `list-private-access-services` 命令</span><span class="sxs-lookup"><span data-stu-id="4e757-540">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="4e757-541">为 `vnet subnet create` 和 `vnet subnet update` 添加了 `--private-access-services` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-541">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="4e757-542">修复了 `application-gateway redirect-config create` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-542">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="4e757-543">修复了无法结合 `--no-wait` 使用 `application-gateway redirect-config update` 的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-543">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="4e757-544">修复了结合 `application-gateway address-pool create` 和 `application-gateway address-pool update` 使用 `--servers` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="4e757-544">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="4e757-545">添加了 `application-gateway redirect-config` 命令</span><span class="sxs-lookup"><span data-stu-id="4e757-545">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="4e757-546">添加了 `application-gateway ssl-policy` 的命令：`list-options`、`predefined list`、`predefined show`</span><span class="sxs-lookup"><span data-stu-id="4e757-546">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="4e757-547">添加了 `application-gateway ssl-policy set` 的参数：`--name`、`--cipher-suites`、`--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="4e757-547">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="4e757-548">添加了 `application-gateway http-settings create` 和 `application-gateway http-settings update` 的参数：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`</span><span class="sxs-lookup"><span data-stu-id="4e757-548">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="4e757-549">添加了 `application-gateway url-path-map create` 和 `application-gateway url-path-map update` 的参数：`--default-redirect-config`、`--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="4e757-549">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="4e757-550">为 `application-gateway url-path-map rule create` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-550">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="4e757-551">在 `application-gateway url-path-map rule delete` 中添加了对 `--no-wait` 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-551">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="4e757-552">添加了 `application-gateway probe create` 和 `application-gateway probe update` 的参数：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="4e757-552">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="4e757-553">为 `application-gateway rule create` 和 `application-gateway rule update` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-553">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="4e757-554">在 `nic create` 和 `nic update` 中添加了对 `--accelerated-networking` 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-554">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="4e757-555">从 `nic create` 中删除了 `--internal-dns-name-suffix` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-555">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="4e757-556">在 `nic update` 和 `nic create` 中添加了对 `--dns-servers` 的支持：添加了对 --dns-servers 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-556">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="4e757-557">修复了 `local-gateway create` 忽略 `--local-address-prefixes` 的 bug</span><span class="sxs-lookup"><span data-stu-id="4e757-557">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="4e757-558">在 `vnet update` 中添加了对 `--dns-servers` 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-558">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="4e757-559">修复了使用 `express-route peering create` 创建不包含路由筛选的对等互连时的 bug</span><span class="sxs-lookup"><span data-stu-id="4e757-559">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="4e757-560">修复了无法结合 `--provider` 和 `--bandwidth` 参数使用 `express-route update` 的 bug</span><span class="sxs-lookup"><span data-stu-id="4e757-560">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="4e757-561">修复了 `network watcher show-topology` 默认逻辑的 bug</span><span class="sxs-lookup"><span data-stu-id="4e757-561">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="4e757-562">改进了 `network list-usages` 的输出格式</span><span class="sxs-lookup"><span data-stu-id="4e757-562">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="4e757-563">如果只存在一个，则对 `application-gateway http-listener create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="4e757-563">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="4e757-564">如果只存在一个，则对 `application-gateway rule create` 使用默认地址池、HTTP 设置和 HTTP 侦听器</span><span class="sxs-lookup"><span data-stu-id="4e757-564">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="4e757-565">如果只存在一个，则对 `lb rule create` 使用默认前端 IP 和后端池</span><span class="sxs-lookup"><span data-stu-id="4e757-565">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="4e757-566">如果只存在一个，则对 `lb inbound-nat-rule create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="4e757-566">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="4e757-567">配置文件</span><span class="sxs-lookup"><span data-stu-id="4e757-567">Profile</span></span>

* <span data-ttu-id="4e757-568">支持使用托管标识在 VM 内部登录</span><span class="sxs-lookup"><span data-stu-id="4e757-568">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="4e757-569">支持采用 SDK 身份验证文件格式的 `account show` 输出</span><span class="sxs-lookup"><span data-stu-id="4e757-569">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="4e757-570">使用 '--expanded-view' 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="4e757-570">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="4e757-571">添加了 `get-access-token` 命令来提供原始 AAD 令牌</span><span class="sxs-lookup"><span data-stu-id="4e757-571">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="4e757-572">支持使用不包含关联订阅的用户帐户登录</span><span class="sxs-lookup"><span data-stu-id="4e757-572">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="4e757-573">RDBMS</span><span class="sxs-lookup"><span data-stu-id="4e757-573">RDBMS</span></span>

* <span data-ttu-id="4e757-574">支持跨订阅列出服务器 (#3417)</span><span class="sxs-lookup"><span data-stu-id="4e757-574">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="4e757-575">修复了由于缺少 `% server_type` 而不处理 `%s` 的问题 (#3393)</span><span class="sxs-lookup"><span data-stu-id="4e757-575">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="4e757-576">修复了文档源映射并添加了 CI 任务用于验证 (#3361)</span><span class="sxs-lookup"><span data-stu-id="4e757-576">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="4e757-577">修复了 MySQL 和 PostgreSQL 帮助 (#3369)</span><span class="sxs-lookup"><span data-stu-id="4e757-577">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="4e757-578">资源</span><span class="sxs-lookup"><span data-stu-id="4e757-578">Resource</span></span>

* <span data-ttu-id="4e757-579">改进了有关 `group deployment create` 缺少参数的提示</span><span class="sxs-lookup"><span data-stu-id="4e757-579">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="4e757-580">改进了 `--parameters KEY=VALUE` 语法分析</span><span class="sxs-lookup"><span data-stu-id="4e757-580">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="4e757-581">修复了不再能够使用 `@<file>` 语法识别 `group deployment create` 参数文件的问题</span><span class="sxs-lookup"><span data-stu-id="4e757-581">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="4e757-582">支持 `resource` 和 `managedapp` 命令的 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-582">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="4e757-583">修复了一些分析和错误消息 (#3584)</span><span class="sxs-lookup"><span data-stu-id="4e757-583">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="4e757-584">修复了 `lock` 命令的 `--resource-type` 分析，接受 `<resource-namespace>` 和 `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="4e757-584">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="4e757-585">添加了模板链接模板的参数检查 (#3629)</span><span class="sxs-lookup"><span data-stu-id="4e757-585">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="4e757-586">添加了使用 `KEY=VALUE` 语法指定部署参数的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-586">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="4e757-587">角色</span><span class="sxs-lookup"><span data-stu-id="4e757-587">Role</span></span>

* <span data-ttu-id="4e757-588">支持采用 SDK 身份验证文件格式的 `create-for-rbac` 输出</span><span class="sxs-lookup"><span data-stu-id="4e757-588">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="4e757-589">删除服务主体时清理角色分配和相关的 AAD 应用程序 (#3610)</span><span class="sxs-lookup"><span data-stu-id="4e757-589">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="4e757-590">在 `app create` 参数 `--start-date` 和 `--end-date` 说明中包含时间格式</span><span class="sxs-lookup"><span data-stu-id="4e757-590">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="4e757-591">使用 `--expanded-view` 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="4e757-591">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="4e757-592">在 `create-for-rbac` 和 `reset-credentials` 命令中添加了 Key Vault 集成</span><span class="sxs-lookup"><span data-stu-id="4e757-592">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="4e757-593">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="4e757-593">Service Fabric</span></span>
* <span data-ttu-id="4e757-594">修复了上传时截断应用程序中的大型文件的问题 (#3666)</span><span class="sxs-lookup"><span data-stu-id="4e757-594">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="4e757-595">添加了 Service Fabric 命令的测试 (#3424)</span><span class="sxs-lookup"><span data-stu-id="4e757-595">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="4e757-596">添加了大量的 Service Fabric 命令 (#3234)</span><span class="sxs-lookup"><span data-stu-id="4e757-596">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="4e757-597">SQL</span><span class="sxs-lookup"><span data-stu-id="4e757-597">SQL</span></span>

* <span data-ttu-id="4e757-598">删除了无效的 `sql server create` `--identity` 参数</span><span class="sxs-lookup"><span data-stu-id="4e757-598">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="4e757-599">从 `sql server create` 和 `sql server update` 命令输出中删除了密码值</span><span class="sxs-lookup"><span data-stu-id="4e757-599">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="4e757-600">添加了命令 `sql db list-editions` 和 `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="4e757-600">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="4e757-601">存储</span><span class="sxs-lookup"><span data-stu-id="4e757-601">Storage</span></span>

* <span data-ttu-id="4e757-602">从 `storage blob list`、`storage container list` 和 `storage share list` 命令中删除了 `--marker` 选项 (#3745)</span><span class="sxs-lookup"><span data-stu-id="4e757-602">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="4e757-603">启用了创建仅限 https 的存储帐户</span><span class="sxs-lookup"><span data-stu-id="4e757-603">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="4e757-604">更新了存储指标、日志记录和 CORS 命令 (#3495)</span><span class="sxs-lookup"><span data-stu-id="4e757-604">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="4e757-605">重新编写了 CORS add 命令的异常消息 (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="4e757-605">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="4e757-606">已在下载批处理命令试运行模式下将生成器转换为列表 (#3592)</span><span class="sxs-lookup"><span data-stu-id="4e757-606">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="4e757-607">修复了 Blob 下载批处理试运行问题 (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="4e757-607">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="4e757-608">VM</span><span class="sxs-lookup"><span data-stu-id="4e757-608">VM</span></span>

* <span data-ttu-id="4e757-609">支持配置 NSG</span><span class="sxs-lookup"><span data-stu-id="4e757-609">Support configuring nsg</span></span>
* <span data-ttu-id="4e757-610">修复了无法正确配置 DNS 服务器的 bug</span><span class="sxs-lookup"><span data-stu-id="4e757-610">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="4e757-611">支持托管服务标识</span><span class="sxs-lookup"><span data-stu-id="4e757-611">Support managed service identities</span></span>
* <span data-ttu-id="4e757-612">修复了包含现有负载均衡器的 `cmss create` 需要 `--backend-pool-name` 的问题。</span><span class="sxs-lookup"><span data-stu-id="4e757-612">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="4e757-613">要求使用 `vm image create` LUN 创建的数据磁盘以 0 开头</span><span class="sxs-lookup"><span data-stu-id="4e757-613">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="4e757-614">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="4e757-614">May 10, 2017</span></span>

<span data-ttu-id="4e757-615">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="4e757-615">Version 2.0.6</span></span>

* <span data-ttu-id="4e757-616">Documentdb 已重命名为 Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="4e757-616">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="4e757-617">添加 rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="4e757-617">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="4e757-618">包括 Data Lake Analytics 和 Data Lake Store 模块。</span><span class="sxs-lookup"><span data-stu-id="4e757-618">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="4e757-619">包括认知服务模块。</span><span class="sxs-lookup"><span data-stu-id="4e757-619">Include Cognitive Services module.</span></span>
* <span data-ttu-id="4e757-620">包括 Service Fabric 模块。</span><span class="sxs-lookup"><span data-stu-id="4e757-620">Include Service Fabric module.</span></span>
* <span data-ttu-id="4e757-621">包括交互式模块（重命名 az-shell）。</span><span class="sxs-lookup"><span data-stu-id="4e757-621">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="4e757-622">添加对 CDN 命令的支持。</span><span class="sxs-lookup"><span data-stu-id="4e757-622">Add support for CDN commands.</span></span>
* <span data-ttu-id="4e757-623">删除容器模块。</span><span class="sxs-lookup"><span data-stu-id="4e757-623">Remove Container module.</span></span>
* <span data-ttu-id="4e757-624">添加“az -v”作为“az --version”的快捷方式 ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="4e757-624">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="4e757-625">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="4e757-625">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="4e757-626">核心</span><span class="sxs-lookup"><span data-stu-id="4e757-626">Core</span></span>

* <span data-ttu-id="4e757-627">核心：捕获未注册提供程序引发的异常并自动注册</span><span class="sxs-lookup"><span data-stu-id="4e757-627">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="4e757-628">性能：将 ADAL 令牌缓存保留在内存中，直至进程退出 ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="4e757-628">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="4e757-629">修复从十六进制指纹 -o tsv 返回的字节 ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="4e757-629">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="4e757-630">改进的 Key Vault 证书下载和 AAD SP 集成 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="4e757-630">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="4e757-631">将 Python 位置添加到“az —version”([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="4e757-631">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="4e757-632">登录：无订阅时支持登录 ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="4e757-632">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="4e757-633">核心：修复重复使用服务主体登录时出现的故障 ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="4e757-633">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="4e757-634">核心：允许通过 env var 配置 accessTokens.json 的文件路径 ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="4e757-634">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="4e757-635">核心：允许配置的默认值应用于可选参数 ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="4e757-635">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="4e757-636">核心：提高了性能</span><span class="sxs-lookup"><span data-stu-id="4e757-636">core: Improved performance</span></span>
* <span data-ttu-id="4e757-637">核心：自定义 CA 证书 - 支持设置 REQUESTS_CA_BUNDLE 环境变量</span><span class="sxs-lookup"><span data-stu-id="4e757-637">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="4e757-638">核心：云配置 - 如果未设置“management”终结点，则使用“resource manager”终结点</span><span class="sxs-lookup"><span data-stu-id="4e757-638">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="4e757-639">ACS</span><span class="sxs-lookup"><span data-stu-id="4e757-639">ACS</span></span>

* <span data-ttu-id="4e757-640">将主计数和代理计数修复为整数而不是字符串</span><span class="sxs-lookup"><span data-stu-id="4e757-640">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="4e757-641">公开“az acs create --no-wait”和“az acs wait”用于异步创建</span><span class="sxs-lookup"><span data-stu-id="4e757-641">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="4e757-642">公开“az acs create --validate”用于试运行验证</span><span class="sxs-lookup"><span data-stu-id="4e757-642">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="4e757-643">在 PUT 调用 scale 命令前删除 Windows 配置文件 ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="4e757-643">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="4e757-644">应用服务</span><span class="sxs-lookup"><span data-stu-id="4e757-644">AppService</span></span>

* <span data-ttu-id="4e757-645">Function App：添加完整的 Function App 支持，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="4e757-645">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="4e757-646">将 Team Services (vsts) 作为持续交付选项添加到“appservice web source-control config”</span><span class="sxs-lookup"><span data-stu-id="4e757-646">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="4e757-647">创建“az webapp”以替换“az appservice web”（为了向后兼容，“az appservice web”将保留 2 个版本）</span><span class="sxs-lookup"><span data-stu-id="4e757-647">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="4e757-648">公开参数以针对 webapp create 配置部署和“运行时堆栈”</span><span class="sxs-lookup"><span data-stu-id="4e757-648">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="4e757-649">公开“webapp list-runtimes”</span><span class="sxs-lookup"><span data-stu-id="4e757-649">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="4e757-650">支持配置连接字符串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="4e757-650">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="4e757-651">支持与预览版交换槽</span><span class="sxs-lookup"><span data-stu-id="4e757-651">support slot swap with preview</span></span>
* <span data-ttu-id="4e757-652">修改 appservice 命令的错误 ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="4e757-652">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="4e757-653">将应用服务计划的资源组用于证书操作 ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="4e757-653">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="4e757-654">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="4e757-654">CosmosDB</span></span>

* <span data-ttu-id="4e757-655">将 DocumentDB 模块重命名为 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="4e757-655">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="4e757-656">增加对 DocumentDB 数据平面 API 的支持：数据库和集合管理</span><span class="sxs-lookup"><span data-stu-id="4e757-656">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="4e757-657">增加对数据库帐户启用自动故障转移的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-657">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="4e757-658">增加对新一致性策略 ConsistentPrefix 的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-658">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="4e757-659">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="4e757-659">Data Lake Analytics</span></span>

* <span data-ttu-id="4e757-660">Bug 修复：在筛选作业结果和状态列表时会引发错误。</span><span class="sxs-lookup"><span data-stu-id="4e757-660">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="4e757-661">增加对新目录项类型的支持：包。</span><span class="sxs-lookup"><span data-stu-id="4e757-661">Add support for new catalog item type: package.</span></span> <span data-ttu-id="4e757-662">访问方法：`az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="4e757-662">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="4e757-663">可从数据库内列出下列目录项（无需架构规范）：</span><span class="sxs-lookup"><span data-stu-id="4e757-663">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="4e757-664">表</span><span class="sxs-lookup"><span data-stu-id="4e757-664">Table</span></span>
  * <span data-ttu-id="4e757-665">表值函数</span><span class="sxs-lookup"><span data-stu-id="4e757-665">Table valued function</span></span>
  * <span data-ttu-id="4e757-666">查看</span><span class="sxs-lookup"><span data-stu-id="4e757-666">View</span></span>
  * <span data-ttu-id="4e757-667">表统计信息。</span><span class="sxs-lookup"><span data-stu-id="4e757-667">Table Statistics.</span></span> <span data-ttu-id="4e757-668">也可以使用架构列出，但无需指定表名。</span><span class="sxs-lookup"><span data-stu-id="4e757-668">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="4e757-669">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4e757-669">Data Lake Store</span></span>

* <span data-ttu-id="4e757-670">更新基础文件系统 SDK 版本，可更好地支持处理服务器端限制方案。</span><span class="sxs-lookup"><span data-stu-id="4e757-670">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="4e757-671">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="4e757-671">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="4e757-672">访问显示帮助丢失。</span><span class="sxs-lookup"><span data-stu-id="4e757-672">missed help for access show.</span></span> <span data-ttu-id="4e757-673">正在添加。</span><span class="sxs-lookup"><span data-stu-id="4e757-673">adding it.</span></span> <span data-ttu-id="4e757-674">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="4e757-674">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="4e757-675">查找</span><span class="sxs-lookup"><span data-stu-id="4e757-675">Find</span></span>

* <span data-ttu-id="4e757-676">改进搜索结果，允许搜索索引的版本控制</span><span class="sxs-lookup"><span data-stu-id="4e757-676">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="4e757-677">KeyVault</span><span class="sxs-lookup"><span data-stu-id="4e757-677">KeyVault</span></span>

* <span data-ttu-id="4e757-678">BC：`az keyvault certificate download` 将 -e 从字符串或二进制更改为 PEM 或 DER，从而更好地表示选项</span><span class="sxs-lookup"><span data-stu-id="4e757-678">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="4e757-679">BC：从 `keyvault certificate create` 删除 --expires 和 --not-before，因为此服务不支持这些参数。</span><span class="sxs-lookup"><span data-stu-id="4e757-679">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="4e757-680">将 --validity 参数添加到 `keyvault certificate create`，有选择地替代 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="4e757-680">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="4e757-681">解决 `keyvault certificate get-default-policy` 中的问题：“expires”和“not_before”已公开，但“validity_in_months”未公开。</span><span class="sxs-lookup"><span data-stu-id="4e757-681">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="4e757-682">KeyVault 解决了 pem 和 pfx 的导入问题 ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="4e757-682">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="4e757-683">实验室</span><span class="sxs-lookup"><span data-stu-id="4e757-683">Lab</span></span>

* <span data-ttu-id="4e757-684">针对实验室环境添加 create、show、delete 和 list 命令。</span><span class="sxs-lookup"><span data-stu-id="4e757-684">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="4e757-685">添加 show 和 list 命令，查看实验室中的 ARM 模板。</span><span class="sxs-lookup"><span data-stu-id="4e757-685">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="4e757-686">在 `az lab vm list` 中添加 --environment 标志，按实验室环境筛选 VM。</span><span class="sxs-lookup"><span data-stu-id="4e757-686">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="4e757-687">添加 convenience 命令 `az lab formula export-artifacts`，导出实验室公式中的项目基架。</span><span class="sxs-lookup"><span data-stu-id="4e757-687">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="4e757-688">添加命令，管理实验室中的机密。</span><span class="sxs-lookup"><span data-stu-id="4e757-688">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="4e757-689">监视</span><span class="sxs-lookup"><span data-stu-id="4e757-689">Monitor</span></span>

* <span data-ttu-id="4e757-690">Bug 修复：为 `az alert-rules create` 的 `--actions` 建模，以使用 JSON 字符串 ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="4e757-690">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="4e757-691">Bug 修复 - diagnostic settings create 不接受来自 show 命令的日志/指标 ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="4e757-691">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="4e757-692">网络</span><span class="sxs-lookup"><span data-stu-id="4e757-692">Network</span></span>

* <span data-ttu-id="4e757-693">添加 `network watcher test-connectivity` 命令。</span><span class="sxs-lookup"><span data-stu-id="4e757-693">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="4e757-694">添加对 `network watcher packet-capture create` 的 `--filters` 参数的支持。</span><span class="sxs-lookup"><span data-stu-id="4e757-694">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="4e757-695">添加对应用程序网关连接排出的支持。</span><span class="sxs-lookup"><span data-stu-id="4e757-695">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="4e757-696">添加对应用程序网关 WAF 规则集配置的支持。</span><span class="sxs-lookup"><span data-stu-id="4e757-696">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="4e757-697">添加对 ExpressRoute 路由筛选器和规则的支持。</span><span class="sxs-lookup"><span data-stu-id="4e757-697">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="4e757-698">添加对 TrafficManager 地理路由的支持。</span><span class="sxs-lookup"><span data-stu-id="4e757-698">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="4e757-699">添加对基于 VPN 连接策略的流量选择器的支持。</span><span class="sxs-lookup"><span data-stu-id="4e757-699">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="4e757-700">添加对 VPN 连接 IPSec 策略的支持。</span><span class="sxs-lookup"><span data-stu-id="4e757-700">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="4e757-701">修复使用 `--no-wait` 或 `--validate` 参数时 `vpn-connection create` 出现的 bug。</span><span class="sxs-lookup"><span data-stu-id="4e757-701">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="4e757-702">添加对主动-主动 VNet 网关的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-702">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="4e757-703">从 `network vpn-connection list/show` 命令的输出中删除 null 值。</span><span class="sxs-lookup"><span data-stu-id="4e757-703">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="4e757-704">BC：修复 `vpn-connection create` 输出中的 bug</span><span class="sxs-lookup"><span data-stu-id="4e757-704">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="4e757-705">Bug 修复：“vpn-connection create”的“--key-length”参数未正确分析。</span><span class="sxs-lookup"><span data-stu-id="4e757-705">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="4e757-706">修复 `dns zone import` 中的 Bug：记录未正确导入。</span><span class="sxs-lookup"><span data-stu-id="4e757-706">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="4e757-707">Bug 修复：`traffic-manager endpoint update` 不起作用。</span><span class="sxs-lookup"><span data-stu-id="4e757-707">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="4e757-708">添加“network watcher”预览命令。</span><span class="sxs-lookup"><span data-stu-id="4e757-708">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="4e757-709">配置文件</span><span class="sxs-lookup"><span data-stu-id="4e757-709">Profile</span></span>

* <span data-ttu-id="4e757-710">支持在未找到订阅时登录 ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="4e757-710">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="4e757-711">支持在 az account set --subscription 中使用短参数名 ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="4e757-711">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="4e757-712">Redis</span><span class="sxs-lookup"><span data-stu-id="4e757-712">Redis</span></span>

* <span data-ttu-id="4e757-713">添加 update 命令，也增加了对 redis 缓存进行缩放的功能</span><span class="sxs-lookup"><span data-stu-id="4e757-713">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="4e757-714">弃用“update-settings”命令。</span><span class="sxs-lookup"><span data-stu-id="4e757-714">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="4e757-715">资源</span><span class="sxs-lookup"><span data-stu-id="4e757-715">Resource</span></span>

* <span data-ttu-id="4e757-716">添加 managedapp 和 managedapp 定义命令 ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="4e757-716">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="4e757-717">支持“provider operation”命令([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="4e757-717">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="4e757-718">支持 generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="4e757-718">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="4e757-719">修复资源分析和 API 版本查找。</span><span class="sxs-lookup"><span data-stu-id="4e757-719">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="4e757-720">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="4e757-720">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="4e757-721">为 az lock update 添加文档。</span><span class="sxs-lookup"><span data-stu-id="4e757-721">Add docs for az lock update.</span></span> <span data-ttu-id="4e757-722">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="4e757-722">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="4e757-723">尝试为不存在的组列出资源时出错。</span><span class="sxs-lookup"><span data-stu-id="4e757-723">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="4e757-724">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="4e757-724">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="4e757-725">[计算] 修复 VMSS 和 VM 可用性集更新的相关问题。</span><span class="sxs-lookup"><span data-stu-id="4e757-725">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="4e757-726">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="4e757-726">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="4e757-727">parent-resource-path 为 None 时修复 lock create 和 delete ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="4e757-727">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="4e757-728">角色</span><span class="sxs-lookup"><span data-stu-id="4e757-728">Role</span></span>

* <span data-ttu-id="4e757-729">create-for-rbac：确保 SP 的结束日期不超过证书的到期日期 ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="4e757-729">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="4e757-730">RBAC：添加对“ad group”的完整支持 ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="4e757-730">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="4e757-731">role：解决角色定义更新的相关问题 ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="4e757-731">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="4e757-732">create-for-rbac：确保已选取用户提供的密码</span><span class="sxs-lookup"><span data-stu-id="4e757-732">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="4e757-733">SQL</span><span class="sxs-lookup"><span data-stu-id="4e757-733">SQL</span></span>

* <span data-ttu-id="4e757-734">添加了 az sql server list-usages 和 az sql db list-usages 命令。</span><span class="sxs-lookup"><span data-stu-id="4e757-734">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="4e757-735">SQL - 能够直接连接到资源提供程序 ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="4e757-735">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="4e757-736">存储</span><span class="sxs-lookup"><span data-stu-id="4e757-736">Storage</span></span>

* <span data-ttu-id="4e757-737">位置默认为 `storage account create` 的资源组位置。</span><span class="sxs-lookup"><span data-stu-id="4e757-737">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="4e757-738">添加对增量 blob 复制的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-738">Add support for incremental blob copy</span></span>
* <span data-ttu-id="4e757-739">添加对大型块 blob 上传的支持</span><span class="sxs-lookup"><span data-stu-id="4e757-739">Add support for large block blob upload</span></span>
* <span data-ttu-id="4e757-740">如果要上传的文件大于 200GB，则将块大小更改为 100MB</span><span class="sxs-lookup"><span data-stu-id="4e757-740">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="4e757-741">VM</span><span class="sxs-lookup"><span data-stu-id="4e757-741">VM</span></span>

* <span data-ttu-id="4e757-742">avail-set：将 UD 和 FD 域计数设为可选</span><span class="sxs-lookup"><span data-stu-id="4e757-742">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="4e757-743">注意：最高等级云中的 VM 命令。请避免与托管磁盘相关的功能，包括以下项：</span><span class="sxs-lookup"><span data-stu-id="4e757-743">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="4e757-744">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="4e757-744">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="4e757-745">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="4e757-745">az vm/vmss disk</span></span>
  3. <span data-ttu-id="4e757-746">在“az vm/vmss create”内，使用“—use-unmanaged-disk”避免托管磁盘 其他命令应有效</span><span class="sxs-lookup"><span data-stu-id="4e757-746">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="4e757-747">vm/vmss：改进生成 SSH 密钥对时的警告文本</span><span class="sxs-lookup"><span data-stu-id="4e757-747">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="4e757-748">vm/vmss：支持通过需要计划信息的市场映像创建 ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="4e757-748">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="4e757-749">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="4e757-749">April 3, 2017</span></span>

<span data-ttu-id="4e757-750">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="4e757-750">Version 2.0.2</span></span>

<span data-ttu-id="4e757-751">此版本中已发布 ACR、批处理、KeyVault 和 SQL 组件。</span><span class="sxs-lookup"><span data-stu-id="4e757-751">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="4e757-752">核心</span><span class="sxs-lookup"><span data-stu-id="4e757-752">Core</span></span>

* <span data-ttu-id="4e757-753">在默认列表中添加了 acr、实验室、监视和查找模块。</span><span class="sxs-lookup"><span data-stu-id="4e757-753">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="4e757-754">登录：跳过错误的租户 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="4e757-754">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="4e757-755">登录：将默认订阅设置为处于“已启用”状态的订阅 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="4e757-755">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="4e757-756">添加了 wait 命令，并添加了对其他命令的 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="4e757-756">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="4e757-757">核心：支持结合证书使用服务主体登录 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="4e757-757">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="4e757-758">添加了有关缺少模板参数的提示。</span><span class="sxs-lookup"><span data-stu-id="4e757-758">Add prompting for missing template parameters.</span></span> <span data-ttu-id="4e757-759">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="4e757-759">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="4e757-760">支持为资源组、默认 Web、 默认 VM 等常见参数设置默认值</span><span class="sxs-lookup"><span data-stu-id="4e757-760">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="4e757-761">支持登录到特定的租户</span><span class="sxs-lookup"><span data-stu-id="4e757-761">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="4e757-762">ACS</span><span class="sxs-lookup"><span data-stu-id="4e757-762">ACS</span></span>

* <span data-ttu-id="4e757-763">[ACS] 添加了配置默认 ACS 群集的支持 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="4e757-763">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="4e757-764">添加了 SSH 密钥密码提示的支持。</span><span class="sxs-lookup"><span data-stu-id="4e757-764">Add support for ssh key password prompting.</span></span> <span data-ttu-id="4e757-765">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="4e757-765">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="4e757-766">添加了对 Windows 群集的支持。</span><span class="sxs-lookup"><span data-stu-id="4e757-766">Add support for windows clusters.</span></span> <span data-ttu-id="4e757-767">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="4e757-767">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="4e757-768">从“所有者”角色切换到“参与者”角色。</span><span class="sxs-lookup"><span data-stu-id="4e757-768">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="4e757-769">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="4e757-769">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="4e757-770">应用服务</span><span class="sxs-lookup"><span data-stu-id="4e757-770">AppService</span></span>

* <span data-ttu-id="4e757-771">应用服务：支持获取用于 DNS A 记录的外部 IP 地址 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="4e757-771">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="4e757-772">应用服务：支持绑定通配符证书 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="4e757-772">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="4e757-773">应用服务：支持列出发布配置文件 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="4e757-773">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="4e757-774">应用服务 - 配置后触发源代码管理同步 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="4e757-774">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="4e757-775">DataLake</span><span class="sxs-lookup"><span data-stu-id="4e757-775">DataLake</span></span>

* <span data-ttu-id="4e757-776">Data Lake Analytics 模块的初始版本。</span><span class="sxs-lookup"><span data-stu-id="4e757-776">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="4e757-777">Data Lake Store 模块的初始版本。</span><span class="sxs-lookup"><span data-stu-id="4e757-777">Initial release of Data Lake Store module.</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="4e757-778">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="4e757-778">DocuemntDB</span></span>

* <span data-ttu-id="4e757-779">DocumentDB：添加了列出连接字符串的支持 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="4e757-779">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="4e757-780">VM</span><span class="sxs-lookup"><span data-stu-id="4e757-780">VM</span></span>

* <span data-ttu-id="4e757-781">[计算] 添加了用于创建虚拟机规模集的应用网关支持 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="4e757-781">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="4e757-782">[VM/VMSS] 改进了磁盘缓存支持 ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="4e757-782">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="4e757-783">VM/VMSS：合并了门户使用的凭据验证逻辑 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="4e757-783">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="4e757-784">添加了 wait 命令和 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="4e757-784">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="4e757-785">虚拟机规模集：支持使用 * 列出不同 VM 上的实例视图 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="4e757-785">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="4e757-786">添加了适用于 VM 和虚拟机规模集的 --secrets ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="4e757-786">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="4e757-787">允许使用专用 VHD 创建 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="4e757-787">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="4e757-788">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="4e757-788">February 27, 2017</span></span>

<span data-ttu-id="4e757-789">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="4e757-789">Version 2.0.0</span></span>

<span data-ttu-id="4e757-790">此版 Azure CLI 2.0 是第一个“正式版”。</span><span class="sxs-lookup"><span data-stu-id="4e757-790">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="4e757-791">正式版适用于以下命令模块：</span><span class="sxs-lookup"><span data-stu-id="4e757-791">General availability applies to these command modules:</span></span>
- <span data-ttu-id="4e757-792">容器服务 (ACS)</span><span class="sxs-lookup"><span data-stu-id="4e757-792">Container Service (acs)</span></span>
- <span data-ttu-id="4e757-793">计算（包括 Resource Manager、VM、虚拟机规模集、托管磁盘）</span><span class="sxs-lookup"><span data-stu-id="4e757-793">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="4e757-794">网络</span><span class="sxs-lookup"><span data-stu-id="4e757-794">Networking</span></span>
- <span data-ttu-id="4e757-795">存储</span><span class="sxs-lookup"><span data-stu-id="4e757-795">Storage</span></span>

<span data-ttu-id="4e757-796">这些命令模块可在生产环境中使用，并受标准 Microsoft SLA 的支持。</span><span class="sxs-lookup"><span data-stu-id="4e757-796">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="4e757-797">可以直接向 Microsoft 支持部门或者通过 [github 问题列表](https://github.com/azure/azure-cli/issues/)提出问题。</span><span class="sxs-lookup"><span data-stu-id="4e757-797">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="4e757-798">可以[在 StackOverflow 上使用 azure-cli 标记](http://stackoverflow.com/questions/tagged/azure-cli)或者通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队来提出问题。可以通过命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="4e757-798">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="4e757-799">这些模块中的命令非常稳定，其语法在此 Azure CLI 版本的后续发行版中预期不会变化。</span><span class="sxs-lookup"><span data-stu-id="4e757-799">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="4e757-800">若要检查 CLI 版本，请使用 `az --version`。</span><span class="sxs-lookup"><span data-stu-id="4e757-800">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="4e757-801">输出中将列出 CLI 本身的版本（在此发行版中为 2.0.0）、各个命令模块的版本，以及所用 Python 和 GCC 的版本。</span><span class="sxs-lookup"><span data-stu-id="4e757-801">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="4e757-802">某些命令模块带有“bn”或“rcn”后缀。</span><span class="sxs-lookup"><span data-stu-id="4e757-802">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="4e757-803">这些命令模块仍以预览版提供，将来会发布正式版。</span><span class="sxs-lookup"><span data-stu-id="4e757-803">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="4e757-804">此外，我们还提供 CLI 夜间预览版。</span><span class="sxs-lookup"><span data-stu-id="4e757-804">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="4e757-805">有关信息，请参阅有关[获取夜间预览版](https://github.com/Azure/azure-cli#nightly-builds)的说明，以及有关[开发人员设置与贡献代码](https://github.com/Azure/azure-cli#developer-setup)的说明。</span><span class="sxs-lookup"><span data-stu-id="4e757-805">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="4e757-806">可通过以下方式报告夜间预览版的问题：</span><span class="sxs-lookup"><span data-stu-id="4e757-806">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="4e757-807">在 [github 问题列表](https://github.com/azure/azure-cli/issues/)中报告问题</span><span class="sxs-lookup"><span data-stu-id="4e757-807">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="4e757-808">通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队。</span><span class="sxs-lookup"><span data-stu-id="4e757-808">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="4e757-809">请通过命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="4e757-809">Provide feedback from the command line with the `az feedback` command.</span></span>

