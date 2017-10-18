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
ms.openlocfilehash: 2ea9daa558200204750f19b5d22685587ff097ef
ms.sourcegitcommit: 376bc0601aba890630dadd55908c1a65ddf40f5a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/11/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="6be8a-104">Azure CLI 2.0 发行说明</span><span class="sxs-lookup"><span data-stu-id="6be8a-104">Azure CLI 2.0 release notes</span></span>

## <a name="october-9-2017"></a><span data-ttu-id="6be8a-105">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="6be8a-105">October 9, 2017</span></span>

<span data-ttu-id="6be8a-106">版本 2.0.19</span><span class="sxs-lookup"><span data-stu-id="6be8a-106">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="6be8a-107">核心</span><span class="sxs-lookup"><span data-stu-id="6be8a-107">Core</span></span>

* <span data-ttu-id="6be8a-108">在 Azure Stack 中添加了一个尾随斜杠用于处理 ADFS 机构 URL</span><span class="sxs-lookup"><span data-stu-id="6be8a-108">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="6be8a-109">应用服务</span><span class="sxs-lookup"><span data-stu-id="6be8a-109">Appservice</span></span>

* <span data-ttu-id="6be8a-110">添加了新命令 `webapp update` 用于执行常规更新</span><span class="sxs-lookup"><span data-stu-id="6be8a-110">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="6be8a-111">批处理</span><span class="sxs-lookup"><span data-stu-id="6be8a-111">Batch</span></span>

* <span data-ttu-id="6be8a-112">已更新为 Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="6be8a-112">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="6be8a-113">更新了 VirtualMachineConfiguration 的 `--image`，用于支持除 publish:offer:sku:version 以外的 ARM 映像引用</span><span class="sxs-lookup"><span data-stu-id="6be8a-113">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="6be8a-114">添加了对 Batch 扩展命令新 CLI 扩展模型的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-114">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="6be8a-115">从组件模型中删除了 Batch 支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-115">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="6be8a-116">Batchai</span><span class="sxs-lookup"><span data-stu-id="6be8a-116">Batchai</span></span>

* <span data-ttu-id="6be8a-117">Batch AI 模块初始版本</span><span class="sxs-lookup"><span data-stu-id="6be8a-117">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="6be8a-118">KeyVault</span><span class="sxs-lookup"><span data-stu-id="6be8a-118">Keyvault</span></span>

* <span data-ttu-id="6be8a-119">修复了在 Azure Stack 中使用 ADFS 时发生的 Key Vault 身份验证问题。</span><span class="sxs-lookup"><span data-stu-id="6be8a-119">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="6be8a-120">(#4448)</span><span class="sxs-lookup"><span data-stu-id="6be8a-120">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="6be8a-121">网络</span><span class="sxs-lookup"><span data-stu-id="6be8a-121">Network</span></span>

* <span data-ttu-id="6be8a-122">已将 `application-gateway address-pool create` 的 `--server` 参数更改为可选，以允许空地址池</span><span class="sxs-lookup"><span data-stu-id="6be8a-122">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="6be8a-123">更新了 `traffic-manager` 以支持最新功能</span><span class="sxs-lookup"><span data-stu-id="6be8a-123">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="6be8a-124">资源</span><span class="sxs-lookup"><span data-stu-id="6be8a-124">Resource</span></span>

* <span data-ttu-id="6be8a-125">在 `group` 中添加了对资源组名称使用 `--resource-group/-g` 选项的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-125">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="6be8a-126">为 `account lock` 添加了命令用于处理订阅级锁</span><span class="sxs-lookup"><span data-stu-id="6be8a-126">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="6be8a-127">为 `group lock` 添加了命令用于处理组级锁</span><span class="sxs-lookup"><span data-stu-id="6be8a-127">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="6be8a-128">为 `resource lock` 添加了命令用于处理资源级锁</span><span class="sxs-lookup"><span data-stu-id="6be8a-128">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="6be8a-129">Sql</span><span class="sxs-lookup"><span data-stu-id="6be8a-129">Sql</span></span>

* <span data-ttu-id="6be8a-130">添加了 SQL 透明数据加密 (TDE) 和自带密钥 TDE 的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-130">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="6be8a-131">添加了 `db list-deleted` 命令和 `db restore --deleted-time` 参数，以便能够找到和还原已删除的数据库</span><span class="sxs-lookup"><span data-stu-id="6be8a-131">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="6be8a-132">添加了 `db op list` 和 `db op cancel`，以便能够列出和取消正在对数据库执行的操作</span><span class="sxs-lookup"><span data-stu-id="6be8a-132">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="6be8a-133">存储</span><span class="sxs-lookup"><span data-stu-id="6be8a-133">Storage</span></span>

* <span data-ttu-id="6be8a-134">添加了对文件共享快照的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-134">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="6be8a-135">Vm</span><span class="sxs-lookup"><span data-stu-id="6be8a-135">Vm</span></span>

* <span data-ttu-id="6be8a-136">修复了 `vm show` 中的一个 bug：在缺少专用 IP 地址的情况下使用 `-d` 会导致崩溃</span><span class="sxs-lookup"><span data-stu-id="6be8a-136">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="6be8a-137">[预览] 添加了滚动升级到 `vmss create` 的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-137">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="6be8a-138">添加了使用 `vm encryption enable` 更新加密设置的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-138">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="6be8a-139">为 `vm create` 添加了 `--os-disk-size-gb` 参数</span><span class="sxs-lookup"><span data-stu-id="6be8a-139">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="6be8a-140">为 Windows 中的 `vmss create` 添加了 `--license-type` 参数</span><span class="sxs-lookup"><span data-stu-id="6be8a-140">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="6be8a-141">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="6be8a-141">September 22, 2017</span></span>

<span data-ttu-id="6be8a-142">版本 2.0.18</span><span class="sxs-lookup"><span data-stu-id="6be8a-142">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="6be8a-143">资源</span><span class="sxs-lookup"><span data-stu-id="6be8a-143">Resource</span></span>

* <span data-ttu-id="6be8a-144">添加了对显示内置策略定义的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-144">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="6be8a-145">添加了用于创建策略定义的支持模式参数</span><span class="sxs-lookup"><span data-stu-id="6be8a-145">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="6be8a-146">为 `managedapp definition create` 添加了对 UI 定义和模板的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-146">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="6be8a-147">[重大更改] 将 `managedapp` 资源类型从 `appliances` 更改到 `applications`，从 `applianceDefinitions` 更改到 `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="6be8a-147">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="6be8a-148">网络</span><span class="sxs-lookup"><span data-stu-id="6be8a-148">Network</span></span>

* <span data-ttu-id="6be8a-149">为 `network lb` 和 `network public-ip` 子命令添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-149">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="6be8a-150">为 `express-route` 添加了对 IPv6 Microsoft 对等互连的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-150">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="6be8a-151">添加了 `asg` 应用程序安全组命令</span><span class="sxs-lookup"><span data-stu-id="6be8a-151">Added `asg` application security group commands</span></span>
* <span data-ttu-id="6be8a-152">为 `nic [create|ip-config create|ip-config update]` 添加了 `--application-security-groups` 参数</span><span class="sxs-lookup"><span data-stu-id="6be8a-152">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="6be8a-153">为 `nsg rule [create|update]` 添加了 `--source-asgs` 和 `--destination-asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="6be8a-153">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="6be8a-154">为 `vnet [create|update]` 添加了 `--ddos-protection` 和 `--vm-protection` 参数</span><span class="sxs-lookup"><span data-stu-id="6be8a-154">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="6be8a-155">添加了 `network [vnet-gateway|vpn-client|show-url]` 命令</span><span class="sxs-lookup"><span data-stu-id="6be8a-155">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="6be8a-156">存储</span><span class="sxs-lookup"><span data-stu-id="6be8a-156">Storage</span></span>

* <span data-ttu-id="6be8a-157">已修复了 `storage account network-rule` 命令在更新 SDK 后可能会失败的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-157">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="6be8a-158">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="6be8a-158">Eventgrid</span></span>

* <span data-ttu-id="6be8a-159">更新了 Azure 事件网格 Python SDK 以使用较新的 API 版本“2017-09-15-preview”</span><span class="sxs-lookup"><span data-stu-id="6be8a-159">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="6be8a-160">SQL</span><span class="sxs-lookup"><span data-stu-id="6be8a-160">SQL</span></span>

* <span data-ttu-id="6be8a-161">将 `sql server list` 的参数 `--resource-group` 更改为可选。</span><span class="sxs-lookup"><span data-stu-id="6be8a-161">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="6be8a-162">如果未指定，将返回订阅中的所有 SQL 服务器</span><span class="sxs-lookup"><span data-stu-id="6be8a-162">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="6be8a-163">为 `db [create|copy|restore|update|replica create|create|update]` 和 `dw [create|update]` 添加了 `--no-wait` 参数</span><span class="sxs-lookup"><span data-stu-id="6be8a-163">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="6be8a-164">KeyVault</span><span class="sxs-lookup"><span data-stu-id="6be8a-164">Keyvault</span></span>

* <span data-ttu-id="6be8a-165">添加了对从代理后执行 Keyvault 命令的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-165">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="6be8a-166">VM</span><span class="sxs-lookup"><span data-stu-id="6be8a-166">VM</span></span>

* <span data-ttu-id="6be8a-167">为 `[vm|vmss|disk] create` 添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-167">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="6be8a-168">已修复了将 `--app-gateway ID` 与 `vmss create` 一起使用会导致故障的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-168">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="6be8a-169">为 `vm create` 添加了 `--asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="6be8a-169">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="6be8a-170">添加了对使用 `vm run-command` 在 VM 上运行命令的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-170">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="6be8a-171">[预览] 添加了对使用 `vmss encryption` 进行 VMSS 磁盘加密的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-171">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="6be8a-172">添加了对使用 `vm perform-maintenance` 在 VM 上执行维护的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-172">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="6be8a-173">ACS</span><span class="sxs-lookup"><span data-stu-id="6be8a-173">ACS</span></span>

* <span data-ttu-id="6be8a-174">[预览] 为适用于 ACS 预览区域的 `acs create` 添加了 `--orchestrator-release` 参数</span><span class="sxs-lookup"><span data-stu-id="6be8a-174">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="6be8a-175">应用服务</span><span class="sxs-lookup"><span data-stu-id="6be8a-175">Appservice</span></span>

* <span data-ttu-id="6be8a-176">添加了使用 `webapp auth [update|show]` 更新和显示身份验证设置的功能</span><span class="sxs-lookup"><span data-stu-id="6be8a-176">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="6be8a-177">备份</span><span class="sxs-lookup"><span data-stu-id="6be8a-177">Backup</span></span>

* <span data-ttu-id="6be8a-178">预览版</span><span class="sxs-lookup"><span data-stu-id="6be8a-178">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="6be8a-179">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="6be8a-179">September 11, 2017</span></span>

<span data-ttu-id="6be8a-180">版本 2.0.17</span><span class="sxs-lookup"><span data-stu-id="6be8a-180">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="6be8a-181">核心</span><span class="sxs-lookup"><span data-stu-id="6be8a-181">Core</span></span>

* <span data-ttu-id="6be8a-182">启用了命令模块在遥测中设置其自己的相关 ID</span><span class="sxs-lookup"><span data-stu-id="6be8a-182">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="6be8a-183">修复了在遥测设置为诊断模式时的 JSON 转储问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-183">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="6be8a-184">Acs</span><span class="sxs-lookup"><span data-stu-id="6be8a-184">Acs</span></span>

* <span data-ttu-id="6be8a-185">添加了 `acs list-locations` 命令</span><span class="sxs-lookup"><span data-stu-id="6be8a-185">Added `acs list-locations` command</span></span>
* <span data-ttu-id="6be8a-186">使 `ssh-key-file` 附带预期的默认值</span><span class="sxs-lookup"><span data-stu-id="6be8a-186">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="6be8a-187">应用服务</span><span class="sxs-lookup"><span data-stu-id="6be8a-187">Appservice</span></span>

* <span data-ttu-id="6be8a-188">添加了在未包含活动服务计划的资源组中创建 Web 应用的功能</span><span class="sxs-lookup"><span data-stu-id="6be8a-188">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="6be8a-189">CDN</span><span class="sxs-lookup"><span data-stu-id="6be8a-189">CDN</span></span>

* <span data-ttu-id="6be8a-190">修复了 `cdn custom-domain create` 的“CustomDomain 不可迭代” bug。</span><span class="sxs-lookup"><span data-stu-id="6be8a-190">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="6be8a-191">分机</span><span class="sxs-lookup"><span data-stu-id="6be8a-191">Extension</span></span>

* <span data-ttu-id="6be8a-192">初始版本。</span><span class="sxs-lookup"><span data-stu-id="6be8a-192">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="6be8a-193">KeyVault</span><span class="sxs-lookup"><span data-stu-id="6be8a-193">Keyvault</span></span>

* <span data-ttu-id="6be8a-194">修复了 `keyvault set-policy` 的权限区分大小写的问题。</span><span class="sxs-lookup"><span data-stu-id="6be8a-194">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="6be8a-195">网络</span><span class="sxs-lookup"><span data-stu-id="6be8a-195">Network</span></span>

* <span data-ttu-id="6be8a-196">已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="6be8a-196">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="6be8a-197">已为 `vnet subnet create/update` 将 `--private-access-services` 参数重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="6be8a-197">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="6be8a-198">在 `nsg rule create/update` 中添加了对多个 IP 范围和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-198">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="6be8a-199">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-199">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="6be8a-200">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-200">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="6be8a-201">资源</span><span class="sxs-lookup"><span data-stu-id="6be8a-201">Resource</span></span>

* <span data-ttu-id="6be8a-202">允许在 `policy definition create` 和 `policy definition update` 中传入资源策略参数定义</span><span class="sxs-lookup"><span data-stu-id="6be8a-202">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="6be8a-203">允许为 `policy assignment create` 传入参数值</span><span class="sxs-lookup"><span data-stu-id="6be8a-203">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="6be8a-204">允许为所有参数传入 JSON 或文件</span><span class="sxs-lookup"><span data-stu-id="6be8a-204">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="6be8a-205">更新了 API 版本</span><span class="sxs-lookup"><span data-stu-id="6be8a-205">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="6be8a-206">SQL</span><span class="sxs-lookup"><span data-stu-id="6be8a-206">SQL</span></span>

* <span data-ttu-id="6be8a-207">添加了 `sql server vnet-rule` 命令</span><span class="sxs-lookup"><span data-stu-id="6be8a-207">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="6be8a-208">VM</span><span class="sxs-lookup"><span data-stu-id="6be8a-208">VM</span></span>

* <span data-ttu-id="6be8a-209">已修复：除非提供 `--scope`，否则不分配访问权限</span><span class="sxs-lookup"><span data-stu-id="6be8a-209">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="6be8a-210">已修复：使用与门户相同的扩展命名</span><span class="sxs-lookup"><span data-stu-id="6be8a-210">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="6be8a-211">已从 `[vm|vmss] create` 输出中删除了 `subscription`</span><span class="sxs-lookup"><span data-stu-id="6be8a-211">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="6be8a-212">已修复：`[vm|vmss] create` SKU 无法应用于带映像的数据磁盘</span><span class="sxs-lookup"><span data-stu-id="6be8a-212">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="6be8a-213">已修复：`vm format-secret --secrets` 不接受新行分隔的 ID</span><span class="sxs-lookup"><span data-stu-id="6be8a-213">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="6be8a-214">2017 年 8 月31 日</span><span class="sxs-lookup"><span data-stu-id="6be8a-214">August 31, 2017</span></span>

<span data-ttu-id="6be8a-215">版本 2.0.16</span><span class="sxs-lookup"><span data-stu-id="6be8a-215">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="6be8a-216">KeyVault</span><span class="sxs-lookup"><span data-stu-id="6be8a-216">Keyvault</span></span>

* <span data-ttu-id="6be8a-217">修复了在尝试使用 `secret download` 自动解析机密编码时的 bug</span><span class="sxs-lookup"><span data-stu-id="6be8a-217">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="6be8a-218">Sf</span><span class="sxs-lookup"><span data-stu-id="6be8a-218">Sf</span></span>

* <span data-ttu-id="6be8a-219">弃用所有支持 Service Fabric CLI (sfctl) 的命令</span><span class="sxs-lookup"><span data-stu-id="6be8a-219">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="6be8a-220">存储</span><span class="sxs-lookup"><span data-stu-id="6be8a-220">Storage</span></span>

* <span data-ttu-id="6be8a-221">修复了无法在不支持 NetworkACLs 功能的区域中创建存储帐户的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-221">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="6be8a-222">在 Blob 和文件上载过程中确定内容类型和内容编码（如果既未指定内容类型，也未指定内容编码）</span><span class="sxs-lookup"><span data-stu-id="6be8a-222">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="6be8a-223">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="6be8a-223">August 28, 2017</span></span>

<span data-ttu-id="6be8a-224">版本 2.0.15</span><span class="sxs-lookup"><span data-stu-id="6be8a-224">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="6be8a-225">CLI</span><span class="sxs-lookup"><span data-stu-id="6be8a-225">CLI</span></span>

* <span data-ttu-id="6be8a-226">在 `--version` 中添加了法律说明。</span><span class="sxs-lookup"><span data-stu-id="6be8a-226">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="6be8a-227">ACS</span><span class="sxs-lookup"><span data-stu-id="6be8a-227">ACS</span></span>

* <span data-ttu-id="6be8a-228">更正了预览区域。</span><span class="sxs-lookup"><span data-stu-id="6be8a-228">Corrected preview regions.</span></span>
* <span data-ttu-id="6be8a-229">正确设置了默认 `dns_name_prefix` 的格式。</span><span class="sxs-lookup"><span data-stu-id="6be8a-229">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="6be8a-230">优化了 acs 命令输出。</span><span class="sxs-lookup"><span data-stu-id="6be8a-230">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="6be8a-231">应用服务</span><span class="sxs-lookup"><span data-stu-id="6be8a-231">Appservice</span></span>

* <span data-ttu-id="6be8a-232">[重大更改] 修复了 `az webapp config appsettings [delete|set]` 输出中的不一致问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-232">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="6be8a-233">为 `az webapp config container set --docker-custom-image-name` 的 `-i` 添加了新别名</span><span class="sxs-lookup"><span data-stu-id="6be8a-233">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="6be8a-234">公开了 `az webapp log show`</span><span class="sxs-lookup"><span data-stu-id="6be8a-234">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="6be8a-235">公开了 `az webapp delete` 中的新参数，用于保留应用服务计划、指标或 dns 注册</span><span class="sxs-lookup"><span data-stu-id="6be8a-235">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="6be8a-236">已修复：正确检测槽位设置</span><span class="sxs-lookup"><span data-stu-id="6be8a-236">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="6be8a-237">IoT</span><span class="sxs-lookup"><span data-stu-id="6be8a-237">IoT</span></span>

* <span data-ttu-id="6be8a-238">修复了 #3934：策略创建操作不再清除现有的策略</span><span class="sxs-lookup"><span data-stu-id="6be8a-238">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="6be8a-239">网络</span><span class="sxs-lookup"><span data-stu-id="6be8a-239">Network</span></span>

* <span data-ttu-id="6be8a-240">[重大更改] 已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="6be8a-240">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="6be8a-241">[重大更改] 已将 `vnet subnet [create|update]` 的选项 `--private-access-services` 重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="6be8a-241">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="6be8a-242">在 `nsg rule [create|update]` 中添加了对多个 IP 和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-242">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="6be8a-243">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-243">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="6be8a-244">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-244">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="6be8a-245">配置文件</span><span class="sxs-lookup"><span data-stu-id="6be8a-245">Profile</span></span>

* <span data-ttu-id="6be8a-246">公开了 `--msi` 和 `--msi-port`，以便使用虚拟机的标识登录</span><span class="sxs-lookup"><span data-stu-id="6be8a-246">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="6be8a-247">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="6be8a-247">Service Fabric</span></span>

* <span data-ttu-id="6be8a-248">预览版</span><span class="sxs-lookup"><span data-stu-id="6be8a-248">Preview release</span></span>
* <span data-ttu-id="6be8a-249">简化了命令的注册表用户/密码规则</span><span class="sxs-lookup"><span data-stu-id="6be8a-249">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="6be8a-250">修复了即使在参数中传入了密码，也提示用户输入密码的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-250">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="6be8a-251">添加了对空 `registry_cred` 的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-251">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="6be8a-252">存储</span><span class="sxs-lookup"><span data-stu-id="6be8a-252">Storage</span></span>

* <span data-ttu-id="6be8a-253">启用了设置 Blob 层</span><span class="sxs-lookup"><span data-stu-id="6be8a-253">Enabled setting blob tier</span></span>
* <span data-ttu-id="6be8a-254">为 `storage account [create|update]` 添加了 `--bypass` 和 `--default-action` 参数用于支持服务隧道</span><span class="sxs-lookup"><span data-stu-id="6be8a-254">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="6be8a-255">添加了用于在 `storage account network-rule` 中添加 VNET 规则和基于 IP 的规则的命令</span><span class="sxs-lookup"><span data-stu-id="6be8a-255">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>  
* <span data-ttu-id="6be8a-256">启用了使用客户管理的密钥进行服务加密的功能</span><span class="sxs-lookup"><span data-stu-id="6be8a-256">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="6be8a-257">[重大更改] 已将 `az storage account create and az storage account update` 命令的选项 `--encryption` 重命名为 `--encryption-services`</span><span class="sxs-lookup"><span data-stu-id="6be8a-257">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="6be8a-258">修复了 #4220：`az storage account update encryption` - 语法不匹配</span><span class="sxs-lookup"><span data-stu-id="6be8a-258">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="6be8a-259">VM</span><span class="sxs-lookup"><span data-stu-id="6be8a-259">VM</span></span>

* <span data-ttu-id="6be8a-260">修复了使用 `--instance-id *` 时，针对 `vmss get-instance-view` 显示多余且错误的信息的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-260">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="6be8a-261">在 `vmss create` 中添加了对 `--lb-sku` 的支持：</span><span class="sxs-lookup"><span data-stu-id="6be8a-261">Added support for `--lb-sku` to `vmss create`:</span></span> 
* <span data-ttu-id="6be8a-262">从 `[vm|vmss] create` 的管理员名称方块列表中删除了人员名称</span><span class="sxs-lookup"><span data-stu-id="6be8a-262">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span> 
* <span data-ttu-id="6be8a-263">修复了当无法从映像中提取计划信息时，`[vm|vmss] create` 引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-263">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="6be8a-264">修复了创建包含内部 LB 的 vmms 规模集时发生崩溃的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-264">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="6be8a-265">修复了 `--no-wait` 参数无法配合 `vm availability-set create` 工作的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-265">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="6be8a-266">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="6be8a-266">August 15, 2017</span></span>

<span data-ttu-id="6be8a-267">版本 2.0.14</span><span class="sxs-lookup"><span data-stu-id="6be8a-267">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="6be8a-268">ACS</span><span class="sxs-lookup"><span data-stu-id="6be8a-268">ACS</span></span>

* <span data-ttu-id="6be8a-269">更正了 kubernetes 的 sshMaster0 端口号</span><span class="sxs-lookup"><span data-stu-id="6be8a-269">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="6be8a-270">应用服务</span><span class="sxs-lookup"><span data-stu-id="6be8a-270">Appservice</span></span>

* <span data-ttu-id="6be8a-271">修复了创建基于新 Git 的 Linux Web 应用时发生异常的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-271">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="6be8a-272">事件网格</span><span class="sxs-lookup"><span data-stu-id="6be8a-272">Event Grid</span></span>

* <span data-ttu-id="6be8a-273">添加了 SDK 依赖项</span><span class="sxs-lookup"><span data-stu-id="6be8a-273">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="6be8a-274">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="6be8a-274">August 11, 2017</span></span>

<span data-ttu-id="6be8a-275">版本 2.0.13</span><span class="sxs-lookup"><span data-stu-id="6be8a-275">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="6be8a-276">ACS</span><span class="sxs-lookup"><span data-stu-id="6be8a-276">ACS</span></span>

* <span data-ttu-id="6be8a-277">添加了更多预览区域</span><span class="sxs-lookup"><span data-stu-id="6be8a-277">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="6be8a-278">批处理</span><span class="sxs-lookup"><span data-stu-id="6be8a-278">Batch</span></span>

* <span data-ttu-id="6be8a-279">已更新到 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="6be8a-279">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="6be8a-280">添加了新命令用于显示作业的任务计数</span><span class="sxs-lookup"><span data-stu-id="6be8a-280">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="6be8a-281">修复了处理资源文件 SAS URL 时的 bug</span><span class="sxs-lookup"><span data-stu-id="6be8a-281">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="6be8a-282">Batch 帐户终结点现在支持可选的 “https://” 前缀</span><span class="sxs-lookup"><span data-stu-id="6be8a-282">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="6be8a-283">支持将包含 100 多个任务的列表添加到作业</span><span class="sxs-lookup"><span data-stu-id="6be8a-283">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="6be8a-284">添加了加载扩展命令模块的调试日志记录</span><span class="sxs-lookup"><span data-stu-id="6be8a-284">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="6be8a-285">组件</span><span class="sxs-lookup"><span data-stu-id="6be8a-285">Component</span></span>

* <span data-ttu-id="6be8a-286">为“az component”命令添加了弃用警告</span><span class="sxs-lookup"><span data-stu-id="6be8a-286">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="6be8a-287">容器</span><span class="sxs-lookup"><span data-stu-id="6be8a-287">Container</span></span>

* <span data-ttu-id="6be8a-288">`create`：修复了某个环境变量中不允许等于号的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-288">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="6be8a-289">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="6be8a-289">Data Lake Store</span></span>

* <span data-ttu-id="6be8a-290">启用了进度控件</span><span class="sxs-lookup"><span data-stu-id="6be8a-290">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="6be8a-291">事件网格</span><span class="sxs-lookup"><span data-stu-id="6be8a-291">Event Grid</span></span>

* <span data-ttu-id="6be8a-292">初始版本</span><span class="sxs-lookup"><span data-stu-id="6be8a-292">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="6be8a-293">网络</span><span class="sxs-lookup"><span data-stu-id="6be8a-293">Network</span></span>

* <span data-ttu-id="6be8a-294">`lb`：修复了某些子资源名称在省略时无法正确解析的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-294">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="6be8a-295">`application-gateway {subresource} delete`：修复了不遵循 `--no-wait` 的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-295">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="6be8a-296">`application-gateway http-settings update`：修复了无法关闭 `--connection-draining-timeout` 的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-296">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="6be8a-297">修复了 `az network vpn-connection ipsec-policy add` 包含意外关键字参数 `sa_data_size_kilobyes` 的错误</span><span class="sxs-lookup"><span data-stu-id="6be8a-297">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="6be8a-298">配置文件</span><span class="sxs-lookup"><span data-stu-id="6be8a-298">Profile</span></span>

* <span data-ttu-id="6be8a-299">`account list`：添加了 `--refresh` 用于从服务器同步最新订阅</span><span class="sxs-lookup"><span data-stu-id="6be8a-299">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="6be8a-300">存储</span><span class="sxs-lookup"><span data-stu-id="6be8a-300">Storage</span></span>

* <span data-ttu-id="6be8a-301">启用了使用系统分配的标识更新存储帐户的功能</span><span class="sxs-lookup"><span data-stu-id="6be8a-301">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="6be8a-302">VM</span><span class="sxs-lookup"><span data-stu-id="6be8a-302">VM</span></span>

* <span data-ttu-id="6be8a-303">`availability-set`：公开了转换时的容错域计数</span><span class="sxs-lookup"><span data-stu-id="6be8a-303">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="6be8a-304">公开了 `list-skus` 命令</span><span class="sxs-lookup"><span data-stu-id="6be8a-304">Exposed `list-skus` command</span></span>
* <span data-ttu-id="6be8a-305">支持在不创建角色分配的情况下分配标识</span><span class="sxs-lookup"><span data-stu-id="6be8a-305">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="6be8a-306">附加数据磁盘时应用存储 SKU</span><span class="sxs-lookup"><span data-stu-id="6be8a-306">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="6be8a-307">删除了使用托管磁盘时的默认 OS 磁盘名称和存储 SKU</span><span class="sxs-lookup"><span data-stu-id="6be8a-307">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="6be8a-308">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="6be8a-308">July 28, 2017</span></span>

<span data-ttu-id="6be8a-309">版本 2.0.12</span><span class="sxs-lookup"><span data-stu-id="6be8a-309">Version 2.0.12</span></span>

* <span data-ttu-id="6be8a-310">添加了容器命令</span><span class="sxs-lookup"><span data-stu-id="6be8a-310">Added container commands</span></span>
* <span data-ttu-id="6be8a-311">添加了计费和消耗模块</span><span class="sxs-lookup"><span data-stu-id="6be8a-311">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="6be8a-312">核心</span><span class="sxs-lookup"><span data-stu-id="6be8a-312">Core</span></span>

* <span data-ttu-id="6be8a-313">输出包含证书的服务主体的 SDK 身份验证信息</span><span class="sxs-lookup"><span data-stu-id="6be8a-313">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="6be8a-314">修复了部署进度异常</span><span class="sxs-lookup"><span data-stu-id="6be8a-314">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="6be8a-315">使用当前云中的 arm 终结点创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="6be8a-315">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="6be8a-316">改进了 clouds.config 文件的并发处理 (#3636)</span><span class="sxs-lookup"><span data-stu-id="6be8a-316">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="6be8a-317">刷新每个命令执行进程的客户端请求 ID</span><span class="sxs-lookup"><span data-stu-id="6be8a-317">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="6be8a-318">使用适当的 SDK 配置文件创建订阅客户端 (#3635)</span><span class="sxs-lookup"><span data-stu-id="6be8a-318">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="6be8a-319">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="6be8a-319">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="6be8a-320">添加了通过 jmespath 查询选择表输出字段的支持 (#3581)</span><span class="sxs-lookup"><span data-stu-id="6be8a-320">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="6be8a-321">改进了分析参数的静默和包含手势的追加历史记录 (#3434)</span><span class="sxs-lookup"><span data-stu-id="6be8a-321">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="6be8a-322">使用适当的 SDK 配置文件创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="6be8a-322">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="6be8a-323">将所有现有记录文件移到最新的文件夹</span><span class="sxs-lookup"><span data-stu-id="6be8a-323">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="6be8a-324">修复了 VM/VMSS 创建操作的幂等性 (#3586)</span><span class="sxs-lookup"><span data-stu-id="6be8a-324">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="6be8a-325">命令路径不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="6be8a-325">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="6be8a-326">某些布尔类型的参数不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="6be8a-326">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="6be8a-327">支持登录到 Azure Stack 等本地服务器上的 ADFS</span><span class="sxs-lookup"><span data-stu-id="6be8a-327">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="6be8a-328">修复了并发写入 clouds.config 的问题 (#3255)</span><span class="sxs-lookup"><span data-stu-id="6be8a-328">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="6be8a-329">ACR</span><span class="sxs-lookup"><span data-stu-id="6be8a-329">ACR</span></span>

* <span data-ttu-id="6be8a-330">针对托管注册表添加了 `show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="6be8a-330">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="6be8a-331">支持托管注册表的 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="6be8a-331">Support SKU update for managed registries</span></span>
* <span data-ttu-id="6be8a-332">添加了包含托管 SKU 的托管注册表</span><span class="sxs-lookup"><span data-stu-id="6be8a-332">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="6be8a-333">通过 ACR Webhook 命令模块添加了托管注册表的 Webhook</span><span class="sxs-lookup"><span data-stu-id="6be8a-333">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="6be8a-334">添加了使用 acr login 命令进行 AAD 身份验证的功能</span><span class="sxs-lookup"><span data-stu-id="6be8a-334">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="6be8a-335">添加了 Docker 存储库、清单和标记的 delete 命令</span><span class="sxs-lookup"><span data-stu-id="6be8a-335">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="6be8a-336">ACS</span><span class="sxs-lookup"><span data-stu-id="6be8a-336">ACS</span></span>

* <span data-ttu-id="6be8a-337">API 版本 2017-07-01 的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-337">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="6be8a-338">应用服务</span><span class="sxs-lookup"><span data-stu-id="6be8a-338">Appservice</span></span>

* <span data-ttu-id="6be8a-339">修复了列出 Linux Web 应用时不返回任何内容的 bug</span><span class="sxs-lookup"><span data-stu-id="6be8a-339">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="6be8a-340">支持从 ACR 检索凭据</span><span class="sxs-lookup"><span data-stu-id="6be8a-340">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="6be8a-341">删除 `appservice web` 下的所有命令</span><span class="sxs-lookup"><span data-stu-id="6be8a-341">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="6be8a-342">将命令输出中的 Docker 注册表密码掩码 (#3656)</span><span class="sxs-lookup"><span data-stu-id="6be8a-342">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="6be8a-343">确保在 macOS 上使用默认浏览器且不出错 (#3623)</span><span class="sxs-lookup"><span data-stu-id="6be8a-343">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="6be8a-344">改进了 `webapp log tail` 和 `webapp log download` 的帮助 (#3624)</span><span class="sxs-lookup"><span data-stu-id="6be8a-344">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="6be8a-345">公开了 `traffic-routing` 命令用于配置静态路由 (#3566)</span><span class="sxs-lookup"><span data-stu-id="6be8a-345">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="6be8a-346">添加了用于配置源代码管理的可靠性修复 (#3245)</span><span class="sxs-lookup"><span data-stu-id="6be8a-346">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="6be8a-347">从 `webapp config update` 中删除了 Windows Web 应用不支持的 `--node-version` 参数。</span><span class="sxs-lookup"><span data-stu-id="6be8a-347">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="6be8a-348">需改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`。</span><span class="sxs-lookup"><span data-stu-id="6be8a-348">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="6be8a-349">批处理</span><span class="sxs-lookup"><span data-stu-id="6be8a-349">Batch</span></span>

* <span data-ttu-id="6be8a-350">已更新到 Batch SDK 3.0.0，支持池中的低优先级 VM</span><span class="sxs-lookup"><span data-stu-id="6be8a-350">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="6be8a-351">已将 `pool create` 选项 `--target-dedicated` 重命名为 `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="6be8a-351">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="6be8a-352">添加了 `pool create` 选项 `--target-low-priority-nodes` 和 `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="6be8a-352">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="6be8a-353">CDN</span><span class="sxs-lookup"><span data-stu-id="6be8a-353">CDN</span></span>

* <span data-ttu-id="6be8a-354">当 `--profile-name` 指定的配置文件不存在时，针对 `cdn endpoint list` 提供更完善的错误消息。</span><span class="sxs-lookup"><span data-stu-id="6be8a-354">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="6be8a-355">云</span><span class="sxs-lookup"><span data-stu-id="6be8a-355">Cloud</span></span>

* <span data-ttu-id="6be8a-356">已将云元数据终结点的 API 版本更改为 YYYY-MM-DD 格式</span><span class="sxs-lookup"><span data-stu-id="6be8a-356">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="6be8a-357">不需要库终结点</span><span class="sxs-lookup"><span data-stu-id="6be8a-357">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="6be8a-358">支持只将云注册到 ARM 资源管理器终结点</span><span class="sxs-lookup"><span data-stu-id="6be8a-358">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="6be8a-359">提供 `cloud set` 的选项用于在选择当前云时选择配置文件</span><span class="sxs-lookup"><span data-stu-id="6be8a-359">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="6be8a-360">公开了 `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="6be8a-360">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="6be8a-361">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6be8a-361">CosmosDB</span></span>

* <span data-ttu-id="6be8a-362">修复了允许使用自定义分区键创建集合的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-362">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="6be8a-363">添加了对集合默认 TTL 的支持。</span><span class="sxs-lookup"><span data-stu-id="6be8a-363">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="6be8a-364">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="6be8a-364">Data Lake Analytics</span></span>

* <span data-ttu-id="6be8a-365">在 `dla account compute-policy` 标题下添加了用于计算策略管理的命令</span><span class="sxs-lookup"><span data-stu-id="6be8a-365">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="6be8a-366">添加了 `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="6be8a-366">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="6be8a-367">添加了 `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="6be8a-367">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="6be8a-368">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="6be8a-368">Data Lake Store</span></span>

* <span data-ttu-id="6be8a-369">在 `dls account update` 中添加了用户管理的 Key Vault 密钥轮换的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-369">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="6be8a-370">更新了底层 Data Lake Store 文件系统 SDK 版本，解决了一个性能问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-370">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="6be8a-371">添加了命令 `dls enable-key-vault`。</span><span class="sxs-lookup"><span data-stu-id="6be8a-371">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="6be8a-372">此命令尝试使用用户提供的 Key Vault 加密 Data Lake Store 帐户中的数据</span><span class="sxs-lookup"><span data-stu-id="6be8a-372">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="6be8a-373">交互</span><span class="sxs-lookup"><span data-stu-id="6be8a-373">Interactive</span></span>

* <span data-ttu-id="6be8a-374">使用缓存的命令改进启动时间</span><span class="sxs-lookup"><span data-stu-id="6be8a-374">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="6be8a-375">增大了测试覆盖率</span><span class="sxs-lookup"><span data-stu-id="6be8a-375">Increased test coverage</span></span>
* <span data-ttu-id="6be8a-376">增强了“?”手势，使之也可注入到下一条命令</span><span class="sxs-lookup"><span data-stu-id="6be8a-376">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="6be8a-377">修复了配置文件 2017-03-09-profile-preview 的交互错误 (#3587)</span><span class="sxs-lookup"><span data-stu-id="6be8a-377">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="6be8a-378">允许使用 `--version` 作为交互模式的参数 (#3645)</span><span class="sxs-lookup"><span data-stu-id="6be8a-378">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="6be8a-379">阻止交互模式在验证填写内容中引发错误 (#3570)</span><span class="sxs-lookup"><span data-stu-id="6be8a-379">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="6be8a-380">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="6be8a-380">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="6be8a-381">添加了 `--progress` 标志</span><span class="sxs-lookup"><span data-stu-id="6be8a-381">Added `--progress` flag</span></span>
* <span data-ttu-id="6be8a-382">从填写内容中删除了 `--debug` 和 `--verbose`</span><span class="sxs-lookup"><span data-stu-id="6be8a-382">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="6be8a-383">从填写内容中删除了 `interactive` (#3324)</span><span class="sxs-lookup"><span data-stu-id="6be8a-383">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="6be8a-384">IoT</span><span class="sxs-lookup"><span data-stu-id="6be8a-384">IoT</span></span>

* <span data-ttu-id="6be8a-385">修复了策略创建操作不再清除现有策略的问题。</span><span class="sxs-lookup"><span data-stu-id="6be8a-385">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="6be8a-386">(#3934)</span><span class="sxs-lookup"><span data-stu-id="6be8a-386">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="6be8a-387">Key Vault</span><span class="sxs-lookup"><span data-stu-id="6be8a-387">Key vault</span></span>

* <span data-ttu-id="6be8a-388">添加了 Key Vault 恢复功能的命令：</span><span class="sxs-lookup"><span data-stu-id="6be8a-388">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="6be8a-389">`keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="6be8a-389">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="6be8a-390">`keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="6be8a-390">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="6be8a-391">`keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="6be8a-391">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="6be8a-392">`keyvault key` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="6be8a-392">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="6be8a-393">添加了服务主体的 Key Vault 集成 (#3133)</span><span class="sxs-lookup"><span data-stu-id="6be8a-393">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="6be8a-394">已将 Key Vault 数据平面更新到 0.3.2。</span><span class="sxs-lookup"><span data-stu-id="6be8a-394">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="6be8a-395">(#3307)</span><span class="sxs-lookup"><span data-stu-id="6be8a-395">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="6be8a-396">实验室</span><span class="sxs-lookup"><span data-stu-id="6be8a-396">Lab</span></span>

* <span data-ttu-id="6be8a-397">添加了通过 `az lab vm claim` 在实验室中声明任何 VM 的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-397">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="6be8a-398">为 `az lab vm list` 和 `az lab vm show` 添加了表输出格式化程序</span><span class="sxs-lookup"><span data-stu-id="6be8a-398">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="6be8a-399">监视</span><span class="sxs-lookup"><span data-stu-id="6be8a-399">Monitor</span></span>

* <span data-ttu-id="6be8a-400">修复了与 `monitor autoscale-settings get-parameters-template` 命令结合使用的模板文件 (#3349)</span><span class="sxs-lookup"><span data-stu-id="6be8a-400">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="6be8a-401">已将 `monitor alert-rule-incidents list` 重命名为 `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="6be8a-401">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="6be8a-402">已将 `monitor alert-rule-incidents show` 重命名为 `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="6be8a-402">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="6be8a-403">已将 `monitor metric-defintions list` 重命名为 `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="6be8a-403">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="6be8a-404">已将 `monitor alert-rules` 重命名为 `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="6be8a-404">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="6be8a-405">更改了 `monitor alert create`：</span><span class="sxs-lookup"><span data-stu-id="6be8a-405">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="6be8a-406">`condition` 和 `action` 子命令不再接受 JSON</span><span class="sxs-lookup"><span data-stu-id="6be8a-406">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="6be8a-407">添加了大量的参数来简化规则创建过程</span><span class="sxs-lookup"><span data-stu-id="6be8a-407">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="6be8a-408">`location` 不再是必需的</span><span class="sxs-lookup"><span data-stu-id="6be8a-408">`location` no longer required</span></span>
  * <span data-ttu-id="6be8a-409">添加了目标的名称和 ID 支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-409">Add name and ID support for target</span></span>
  * <span data-ttu-id="6be8a-410">删除了 `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="6be8a-410">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="6be8a-411">`is-enabled` 重命名为 `enabled`，不再是必需的</span><span class="sxs-lookup"><span data-stu-id="6be8a-411">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="6be8a-412">`description` 默认值现在基于提供的条件</span><span class="sxs-lookup"><span data-stu-id="6be8a-412">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="6be8a-413">添加了示例用于帮助澄清新格式</span><span class="sxs-lookup"><span data-stu-id="6be8a-413">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="6be8a-414">支持在 `monitor metric` 命令中使用名称或 ID</span><span class="sxs-lookup"><span data-stu-id="6be8a-414">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="6be8a-415">为 `monitor alert rule update` 添加了方便的参数和示例</span><span class="sxs-lookup"><span data-stu-id="6be8a-415">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="6be8a-416">网络</span><span class="sxs-lookup"><span data-stu-id="6be8a-416">Network</span></span>

* <span data-ttu-id="6be8a-417">添加了 `list-private-access-services` 命令</span><span class="sxs-lookup"><span data-stu-id="6be8a-417">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="6be8a-418">为 `vnet subnet create` 和 `vnet subnet update` 添加了 `--private-access-services` 参数</span><span class="sxs-lookup"><span data-stu-id="6be8a-418">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="6be8a-419">修复了 `application-gateway redirect-config create` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-419">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="6be8a-420">修复了无法结合 `--no-wait` 使用 `application-gateway redirect-config update` 的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-420">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="6be8a-421">修复了结合 `application-gateway address-pool create` 和 `application-gateway address-pool update` 使用 `--servers` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="6be8a-421">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="6be8a-422">添加了 `application-gateway redirect-config` 命令</span><span class="sxs-lookup"><span data-stu-id="6be8a-422">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="6be8a-423">添加了 `application-gateway ssl-policy` 的命令：`list-options`、`predefined list`、`predefined show`</span><span class="sxs-lookup"><span data-stu-id="6be8a-423">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="6be8a-424">添加了 `application-gateway ssl-policy set` 的参数：`--name`、`--cipher-suites`、`--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="6be8a-424">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="6be8a-425">添加了 `application-gateway http-settings create` 和 `application-gateway http-settings update` 的参数：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`</span><span class="sxs-lookup"><span data-stu-id="6be8a-425">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="6be8a-426">添加了 `application-gateway url-path-map create` 和 `application-gateway url-path-map update` 的参数：`--default-redirect-config`、`--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="6be8a-426">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="6be8a-427">为 `application-gateway url-path-map rule create` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="6be8a-427">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="6be8a-428">在 `application-gateway url-path-map rule delete` 中添加了对 `--no-wait` 的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-428">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="6be8a-429">添加了 `application-gateway probe create` 和 `application-gateway probe update` 的参数：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="6be8a-429">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="6be8a-430">为 `application-gateway rule create` 和 `application-gateway rule update` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="6be8a-430">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="6be8a-431">在 `nic create` 和 `nic update` 中添加了对 `--accelerated-networking` 的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-431">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="6be8a-432">从 `nic create` 中删除了 `--internal-dns-name-suffix` 参数</span><span class="sxs-lookup"><span data-stu-id="6be8a-432">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="6be8a-433">在 `nic update` 和 `nic create` 中添加了对 `--dns-servers` 的支持：添加了对 --dns-servers 的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-433">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="6be8a-434">修复了 `local-gateway create` 忽略 `--local-address-prefixes` 的 bug</span><span class="sxs-lookup"><span data-stu-id="6be8a-434">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="6be8a-435">在 `vnet update` 中添加了对 `--dns-servers` 的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-435">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="6be8a-436">修复了使用 `express-route peering create` 创建不包含路由筛选的对等互连时的 bug</span><span class="sxs-lookup"><span data-stu-id="6be8a-436">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="6be8a-437">修复了无法结合 `--provider` 和 `--bandwidth` 参数使用 `express-route update` 的 bug</span><span class="sxs-lookup"><span data-stu-id="6be8a-437">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="6be8a-438">修复了 `network watcher show-topology` 默认逻辑的 bug</span><span class="sxs-lookup"><span data-stu-id="6be8a-438">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="6be8a-439">改进了 `network list-usages` 的输出格式</span><span class="sxs-lookup"><span data-stu-id="6be8a-439">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="6be8a-440">如果只存在一个，则对 `application-gateway http-listener create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="6be8a-440">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="6be8a-441">如果只存在一个，则对 `application-gateway rule create` 使用默认地址池、HTTP 设置和 HTTP 侦听器</span><span class="sxs-lookup"><span data-stu-id="6be8a-441">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="6be8a-442">如果只存在一个，则对 `lb rule create` 使用默认前端 IP 和后端池</span><span class="sxs-lookup"><span data-stu-id="6be8a-442">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="6be8a-443">如果只存在一个，则对 `lb inbound-nat-rule create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="6be8a-443">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="6be8a-444">配置文件</span><span class="sxs-lookup"><span data-stu-id="6be8a-444">Profile</span></span>

* <span data-ttu-id="6be8a-445">支持使用托管标识在 VM 内部登录</span><span class="sxs-lookup"><span data-stu-id="6be8a-445">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="6be8a-446">支持采用 SDK 身份验证文件格式的 `account show` 输出</span><span class="sxs-lookup"><span data-stu-id="6be8a-446">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="6be8a-447">使用 '--expanded-view' 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="6be8a-447">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="6be8a-448">添加了 `get-access-token` 命令来提供原始 AAD 令牌</span><span class="sxs-lookup"><span data-stu-id="6be8a-448">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="6be8a-449">支持使用不包含关联订阅的用户帐户登录</span><span class="sxs-lookup"><span data-stu-id="6be8a-449">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="6be8a-450">RDBMS</span><span class="sxs-lookup"><span data-stu-id="6be8a-450">RDBMS</span></span>

* <span data-ttu-id="6be8a-451">支持跨订阅列出服务器 (#3417)</span><span class="sxs-lookup"><span data-stu-id="6be8a-451">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="6be8a-452">修复了由于缺少 `% server_type` 而不处理 `%s` 的问题 (#3393)</span><span class="sxs-lookup"><span data-stu-id="6be8a-452">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="6be8a-453">修复了文档源映射并添加了 CI 任务用于验证 (#3361)</span><span class="sxs-lookup"><span data-stu-id="6be8a-453">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="6be8a-454">修复了 MySQL 和 PostgreSQL 帮助 (#3369)</span><span class="sxs-lookup"><span data-stu-id="6be8a-454">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="6be8a-455">资源</span><span class="sxs-lookup"><span data-stu-id="6be8a-455">Resource</span></span>

* <span data-ttu-id="6be8a-456">改进了有关 `group deployment create` 缺少参数的提示</span><span class="sxs-lookup"><span data-stu-id="6be8a-456">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="6be8a-457">改进了 `--parameters KEY=VALUE` 语法分析</span><span class="sxs-lookup"><span data-stu-id="6be8a-457">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="6be8a-458">修复了不再能够使用 `@<file>` 语法识别 `group deployment create` 参数文件的问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-458">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="6be8a-459">支持 `resource` 和 `managedapp` 命令的 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="6be8a-459">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="6be8a-460">修复了一些分析和错误消息 (#3584)</span><span class="sxs-lookup"><span data-stu-id="6be8a-460">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="6be8a-461">修复了 `lock` 命令的 `--resource-type` 分析，接受 `<resource-namespace>` 和 `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="6be8a-461">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="6be8a-462">添加了模板链接模板的参数检查 (#3629)</span><span class="sxs-lookup"><span data-stu-id="6be8a-462">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="6be8a-463">添加了使用 `KEY=VALUE` 语法指定部署参数的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-463">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="6be8a-464">角色</span><span class="sxs-lookup"><span data-stu-id="6be8a-464">Role</span></span>

* <span data-ttu-id="6be8a-465">支持采用 SDK 身份验证文件格式的 `create-for-rbac` 输出</span><span class="sxs-lookup"><span data-stu-id="6be8a-465">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="6be8a-466">删除服务主体时清理角色分配和相关的 AAD 应用程序 (#3610)</span><span class="sxs-lookup"><span data-stu-id="6be8a-466">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="6be8a-467">在 `app create` 参数 `--start-date` 和 `--end-date` 说明中包含时间格式</span><span class="sxs-lookup"><span data-stu-id="6be8a-467">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="6be8a-468">使用 `--expanded-view` 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="6be8a-468">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="6be8a-469">在 `create-for-rbac` 和 `reset-credentials` 命令中添加了 Key Vault 集成</span><span class="sxs-lookup"><span data-stu-id="6be8a-469">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="6be8a-470">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="6be8a-470">Service Fabric</span></span>
* <span data-ttu-id="6be8a-471">修复了上传时截断应用程序中的大型文件的问题 (#3666)</span><span class="sxs-lookup"><span data-stu-id="6be8a-471">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="6be8a-472">添加了 Service Fabric 命令的测试 (#3424)</span><span class="sxs-lookup"><span data-stu-id="6be8a-472">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="6be8a-473">添加了大量的 Service Fabric 命令 (#3234)</span><span class="sxs-lookup"><span data-stu-id="6be8a-473">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="6be8a-474">SQL</span><span class="sxs-lookup"><span data-stu-id="6be8a-474">SQL</span></span>

* <span data-ttu-id="6be8a-475">删除了无效的 `sql server create` `--identity` 参数</span><span class="sxs-lookup"><span data-stu-id="6be8a-475">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="6be8a-476">从 `sql server create` 和 `sql server update` 命令输出中删除了密码值</span><span class="sxs-lookup"><span data-stu-id="6be8a-476">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="6be8a-477">添加了命令 `sql db list-editions` 和 `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="6be8a-477">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="6be8a-478">存储</span><span class="sxs-lookup"><span data-stu-id="6be8a-478">Storage</span></span>

* <span data-ttu-id="6be8a-479">从 `storage blob list`、`storage container list` 和 `storage share list` 命令中删除了 `--marker` 选项 (#3745)</span><span class="sxs-lookup"><span data-stu-id="6be8a-479">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="6be8a-480">启用了创建仅限 https 的存储帐户</span><span class="sxs-lookup"><span data-stu-id="6be8a-480">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="6be8a-481">更新了存储指标、日志记录和 CORS 命令 (#3495)</span><span class="sxs-lookup"><span data-stu-id="6be8a-481">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="6be8a-482">重新编写了 CORS add 命令的异常消息 (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="6be8a-482">Rephrased exception message from CORS add (#3638) (#3362)</span></span>  
* <span data-ttu-id="6be8a-483">已在下载批处理命令试运行模式下将生成器转换为列表 (#3592)</span><span class="sxs-lookup"><span data-stu-id="6be8a-483">Converted generator to a list in download batch command dry run mode (#3592)</span></span> 
* <span data-ttu-id="6be8a-484">修复了 Blob 下载批处理试运行问题 (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="6be8a-484">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="6be8a-485">VM</span><span class="sxs-lookup"><span data-stu-id="6be8a-485">VM</span></span>

* <span data-ttu-id="6be8a-486">支持配置 NSG</span><span class="sxs-lookup"><span data-stu-id="6be8a-486">Support configuring nsg</span></span>
* <span data-ttu-id="6be8a-487">修复了无法正确配置 DNS 服务器的 bug</span><span class="sxs-lookup"><span data-stu-id="6be8a-487">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="6be8a-488">支持托管服务标识</span><span class="sxs-lookup"><span data-stu-id="6be8a-488">Support managed service identities</span></span>
* <span data-ttu-id="6be8a-489">修复了包含现有负载均衡器的 `cmss create` 需要 `--backend-pool-name` 的问题。</span><span class="sxs-lookup"><span data-stu-id="6be8a-489">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="6be8a-490">要求使用 `vm image create` LUN 创建的数据磁盘以 0 开头</span><span class="sxs-lookup"><span data-stu-id="6be8a-490">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="6be8a-491">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="6be8a-491">May 10, 2017</span></span>

<span data-ttu-id="6be8a-492">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="6be8a-492">Version 2.0.6</span></span>

* <span data-ttu-id="6be8a-493">Documentdb 已重命名为 Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="6be8a-493">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="6be8a-494">添加 rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="6be8a-494">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="6be8a-495">包括 Data Lake Analytics 和 Data Lake Store 模块。</span><span class="sxs-lookup"><span data-stu-id="6be8a-495">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="6be8a-496">包括认知服务模块。</span><span class="sxs-lookup"><span data-stu-id="6be8a-496">Include Cognitive Services module.</span></span>
* <span data-ttu-id="6be8a-497">包括 Service Fabric 模块。</span><span class="sxs-lookup"><span data-stu-id="6be8a-497">Include Service Fabric module.</span></span>
* <span data-ttu-id="6be8a-498">包括交互式模块（重命名 az-shell）。</span><span class="sxs-lookup"><span data-stu-id="6be8a-498">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="6be8a-499">添加对 CDN 命令的支持。</span><span class="sxs-lookup"><span data-stu-id="6be8a-499">Add support for CDN commands.</span></span>
* <span data-ttu-id="6be8a-500">删除容器模块。</span><span class="sxs-lookup"><span data-stu-id="6be8a-500">Remove Container module.</span></span>
* <span data-ttu-id="6be8a-501">添加“az -v”作为“az --version”的快捷方式 ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="6be8a-501">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="6be8a-502">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="6be8a-502">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="6be8a-503">核心</span><span class="sxs-lookup"><span data-stu-id="6be8a-503">Core</span></span>

* <span data-ttu-id="6be8a-504">核心：捕获未注册提供程序引发的异常并自动注册</span><span class="sxs-lookup"><span data-stu-id="6be8a-504">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="6be8a-505">性能：将 ADAL 令牌缓存保留在内存中，直至进程退出 ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="6be8a-505">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="6be8a-506">修复从十六进制指纹 -o tsv 返回的字节 ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="6be8a-506">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="6be8a-507">改进的 Key Vault 证书下载和 AAD SP 集成 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="6be8a-507">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="6be8a-508">将 Python 位置添加到“az —version”([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="6be8a-508">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="6be8a-509">登录：无订阅时支持登录 ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="6be8a-509">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="6be8a-510">核心：修复重复使用服务主体登录时出现的故障 ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="6be8a-510">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="6be8a-511">核心：允许通过 env var 配置 accessTokens.json 的文件路径 ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="6be8a-511">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="6be8a-512">核心：允许配置的默认值应用于可选参数 ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="6be8a-512">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="6be8a-513">核心：提高了性能</span><span class="sxs-lookup"><span data-stu-id="6be8a-513">core: Improved performance</span></span>
* <span data-ttu-id="6be8a-514">核心：自定义 CA 证书 - 支持设置 REQUESTS_CA_BUNDLE 环境变量</span><span class="sxs-lookup"><span data-stu-id="6be8a-514">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="6be8a-515">核心：云配置 - 如果未设置“management”终结点，则使用“resource manager”终结点</span><span class="sxs-lookup"><span data-stu-id="6be8a-515">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="6be8a-516">ACS</span><span class="sxs-lookup"><span data-stu-id="6be8a-516">ACS</span></span>

* <span data-ttu-id="6be8a-517">将主计数和代理计数修复为整数而不是字符串</span><span class="sxs-lookup"><span data-stu-id="6be8a-517">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="6be8a-518">公开“az acs create --no-wait”和“az acs wait”用于异步创建</span><span class="sxs-lookup"><span data-stu-id="6be8a-518">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="6be8a-519">公开“az acs create --validate”用于试运行验证</span><span class="sxs-lookup"><span data-stu-id="6be8a-519">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="6be8a-520">在 PUT 调用 scale 命令前删除 Windows 配置文件 ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="6be8a-520">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="6be8a-521">应用服务</span><span class="sxs-lookup"><span data-stu-id="6be8a-521">AppService</span></span>

* <span data-ttu-id="6be8a-522">Function App：添加完整的 Function App 支持，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="6be8a-522">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="6be8a-523">将 Team Services (vsts) 作为持续交付选项添加到“appservice web source-control config”</span><span class="sxs-lookup"><span data-stu-id="6be8a-523">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="6be8a-524">创建“az webapp”以替换“az appservice web”（为了向后兼容，“az appservice web”将保留 2 个版本）</span><span class="sxs-lookup"><span data-stu-id="6be8a-524">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="6be8a-525">公开参数以针对 webapp create 配置部署和“运行时堆栈”</span><span class="sxs-lookup"><span data-stu-id="6be8a-525">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="6be8a-526">公开“webapp list-runtimes”</span><span class="sxs-lookup"><span data-stu-id="6be8a-526">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="6be8a-527">支持配置连接字符串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="6be8a-527">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="6be8a-528">支持与预览版交换槽</span><span class="sxs-lookup"><span data-stu-id="6be8a-528">support slot swap with preview</span></span>
* <span data-ttu-id="6be8a-529">修改 appservice 命令的错误 ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="6be8a-529">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="6be8a-530">将应用服务计划的资源组用于证书操作 ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="6be8a-530">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="6be8a-531">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6be8a-531">CosmosDB</span></span>

* <span data-ttu-id="6be8a-532">将 DocumentDB 模块重命名为 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="6be8a-532">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="6be8a-533">增加对 DocumentDB 数据平面 API 的支持：数据库和集合管理</span><span class="sxs-lookup"><span data-stu-id="6be8a-533">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="6be8a-534">增加对数据库帐户启用自动故障转移的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-534">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="6be8a-535">增加对新一致性策略 ConsistentPrefix 的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-535">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="6be8a-536">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="6be8a-536">Data Lake Analytics</span></span>

* <span data-ttu-id="6be8a-537">Bug 修复：在筛选作业结果和状态列表时会引发错误。</span><span class="sxs-lookup"><span data-stu-id="6be8a-537">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="6be8a-538">增加对新目录项类型的支持：包。</span><span class="sxs-lookup"><span data-stu-id="6be8a-538">Add support for new catalog item type: package.</span></span> <span data-ttu-id="6be8a-539">访问方法：`az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="6be8a-539">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="6be8a-540">可从数据库内列出下列目录项（无需架构规范）：</span><span class="sxs-lookup"><span data-stu-id="6be8a-540">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="6be8a-541">表</span><span class="sxs-lookup"><span data-stu-id="6be8a-541">Table</span></span>
  * <span data-ttu-id="6be8a-542">表值函数</span><span class="sxs-lookup"><span data-stu-id="6be8a-542">Table valued function</span></span>
  * <span data-ttu-id="6be8a-543">查看</span><span class="sxs-lookup"><span data-stu-id="6be8a-543">View</span></span>
  * <span data-ttu-id="6be8a-544">表统计信息。</span><span class="sxs-lookup"><span data-stu-id="6be8a-544">Table Statistics.</span></span> <span data-ttu-id="6be8a-545">也可以使用架构列出，但无需指定表名。</span><span class="sxs-lookup"><span data-stu-id="6be8a-545">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="6be8a-546">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="6be8a-546">Data Lake Store</span></span>

* <span data-ttu-id="6be8a-547">更新基础文件系统 SDK 版本，可更好地支持处理服务器端限制方案。</span><span class="sxs-lookup"><span data-stu-id="6be8a-547">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="6be8a-548">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="6be8a-548">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="6be8a-549">访问显示帮助丢失。</span><span class="sxs-lookup"><span data-stu-id="6be8a-549">missed help for access show.</span></span> <span data-ttu-id="6be8a-550">正在添加。</span><span class="sxs-lookup"><span data-stu-id="6be8a-550">adding it.</span></span> <span data-ttu-id="6be8a-551">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="6be8a-551">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="6be8a-552">查找</span><span class="sxs-lookup"><span data-stu-id="6be8a-552">Find</span></span>

* <span data-ttu-id="6be8a-553">改进搜索结果，允许搜索索引的版本控制</span><span class="sxs-lookup"><span data-stu-id="6be8a-553">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="6be8a-554">KeyVault</span><span class="sxs-lookup"><span data-stu-id="6be8a-554">KeyVault</span></span>

* <span data-ttu-id="6be8a-555">BC：`az keyvault certificate download` 将 -e 从字符串或二进制更改为 PEM 或 DER，从而更好地表示选项</span><span class="sxs-lookup"><span data-stu-id="6be8a-555">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="6be8a-556">BC：从 `keyvault certificate create` 删除 --expires 和 --not-before，因为此服务不支持这些参数。</span><span class="sxs-lookup"><span data-stu-id="6be8a-556">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="6be8a-557">将 --validity 参数添加到 `keyvault certificate create`，有选择地替代 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="6be8a-557">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="6be8a-558">解决 `keyvault certificate get-default-policy` 中的问题：“expires”和“not_before”已公开，但“validity_in_months”未公开。</span><span class="sxs-lookup"><span data-stu-id="6be8a-558">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="6be8a-559">KeyVault 解决了 pem 和 pfx 的导入问题 ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="6be8a-559">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="6be8a-560">实验室</span><span class="sxs-lookup"><span data-stu-id="6be8a-560">Lab</span></span>

* <span data-ttu-id="6be8a-561">针对实验室环境添加 create、show、delete 和 list 命令。</span><span class="sxs-lookup"><span data-stu-id="6be8a-561">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="6be8a-562">添加 show 和 list 命令，查看实验室中的 ARM 模板。</span><span class="sxs-lookup"><span data-stu-id="6be8a-562">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="6be8a-563">在 `az lab vm list` 中添加 --environment 标志，按实验室环境筛选 VM。</span><span class="sxs-lookup"><span data-stu-id="6be8a-563">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="6be8a-564">添加 convenience 命令 `az lab formula export-artifacts`，导出实验室公式中的项目基架。</span><span class="sxs-lookup"><span data-stu-id="6be8a-564">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="6be8a-565">添加命令，管理实验室中的机密。</span><span class="sxs-lookup"><span data-stu-id="6be8a-565">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="6be8a-566">监视</span><span class="sxs-lookup"><span data-stu-id="6be8a-566">Monitor</span></span>

* <span data-ttu-id="6be8a-567">Bug 修复：为 `az alert-rules create` 的 `--actions` 建模，以使用 JSON 字符串 ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="6be8a-567">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="6be8a-568">Bug 修复 - diagnostic settings create 不接受来自 show 命令的日志/指标 ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="6be8a-568">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="6be8a-569">网络</span><span class="sxs-lookup"><span data-stu-id="6be8a-569">Network</span></span>

* <span data-ttu-id="6be8a-570">添加 `network watcher test-connectivity` 命令。</span><span class="sxs-lookup"><span data-stu-id="6be8a-570">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="6be8a-571">添加对 `network watcher packet-capture create` 的 `--filters` 参数的支持。</span><span class="sxs-lookup"><span data-stu-id="6be8a-571">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="6be8a-572">添加对应用程序网关连接排出的支持。</span><span class="sxs-lookup"><span data-stu-id="6be8a-572">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="6be8a-573">添加对应用程序网关 WAF 规则集配置的支持。</span><span class="sxs-lookup"><span data-stu-id="6be8a-573">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="6be8a-574">添加对 ExpressRoute 路由筛选器和规则的支持。</span><span class="sxs-lookup"><span data-stu-id="6be8a-574">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="6be8a-575">添加对 TrafficManager 地理路由的支持。</span><span class="sxs-lookup"><span data-stu-id="6be8a-575">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="6be8a-576">添加对基于 VPN 连接策略的流量选择器的支持。</span><span class="sxs-lookup"><span data-stu-id="6be8a-576">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="6be8a-577">添加对 VPN 连接 IPSec 策略的支持。</span><span class="sxs-lookup"><span data-stu-id="6be8a-577">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="6be8a-578">修复使用 `--no-wait` 或 `--validate` 参数时 `vpn-connection create` 出现的 bug。</span><span class="sxs-lookup"><span data-stu-id="6be8a-578">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="6be8a-579">添加对主动-主动 VNet 网关的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-579">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="6be8a-580">从 `network vpn-connection list/show` 命令的输出中删除 null 值。</span><span class="sxs-lookup"><span data-stu-id="6be8a-580">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="6be8a-581">BC：修复 `vpn-connection create` 输出中的 bug</span><span class="sxs-lookup"><span data-stu-id="6be8a-581">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="6be8a-582">Bug 修复：“vpn-connection create”的“--key-length”参数未正确分析。</span><span class="sxs-lookup"><span data-stu-id="6be8a-582">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="6be8a-583">修复 `dns zone import` 中的 Bug：记录未正确导入。</span><span class="sxs-lookup"><span data-stu-id="6be8a-583">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="6be8a-584">Bug 修复：`traffic-manager endpoint update` 不起作用。</span><span class="sxs-lookup"><span data-stu-id="6be8a-584">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="6be8a-585">添加“network watcher”预览命令。</span><span class="sxs-lookup"><span data-stu-id="6be8a-585">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="6be8a-586">配置文件</span><span class="sxs-lookup"><span data-stu-id="6be8a-586">Profile</span></span>

* <span data-ttu-id="6be8a-587">支持在未找到订阅时登录 ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="6be8a-587">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="6be8a-588">支持在 az account set --subscription 中使用短参数名 ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="6be8a-588">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="6be8a-589">Redis</span><span class="sxs-lookup"><span data-stu-id="6be8a-589">Redis</span></span>

* <span data-ttu-id="6be8a-590">添加 update 命令，也增加了对 redis 缓存进行缩放的功能</span><span class="sxs-lookup"><span data-stu-id="6be8a-590">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="6be8a-591">弃用“update-settings”命令。</span><span class="sxs-lookup"><span data-stu-id="6be8a-591">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="6be8a-592">资源</span><span class="sxs-lookup"><span data-stu-id="6be8a-592">Resource</span></span>

* <span data-ttu-id="6be8a-593">添加 managedapp 和 managedapp 定义命令 ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="6be8a-593">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="6be8a-594">支持“provider operation”命令([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="6be8a-594">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="6be8a-595">支持 generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="6be8a-595">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="6be8a-596">修复资源分析和 API 版本查找。</span><span class="sxs-lookup"><span data-stu-id="6be8a-596">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="6be8a-597">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="6be8a-597">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="6be8a-598">为 az lock update 添加文档。</span><span class="sxs-lookup"><span data-stu-id="6be8a-598">Add docs for az lock update.</span></span> <span data-ttu-id="6be8a-599">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="6be8a-599">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="6be8a-600">尝试为不存在的组列出资源时出错。</span><span class="sxs-lookup"><span data-stu-id="6be8a-600">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="6be8a-601">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="6be8a-601">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="6be8a-602">[计算] 修复 VMSS 和 VM 可用性集更新的相关问题。</span><span class="sxs-lookup"><span data-stu-id="6be8a-602">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="6be8a-603">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="6be8a-603">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="6be8a-604">parent-resource-path 为 None 时修复 lock create 和 delete ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="6be8a-604">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="6be8a-605">角色</span><span class="sxs-lookup"><span data-stu-id="6be8a-605">Role</span></span>

* <span data-ttu-id="6be8a-606">create-for-rbac：确保 SP 的结束日期不超过证书的到期日期 ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="6be8a-606">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="6be8a-607">RBAC：添加对“ad group”的完整支持 ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="6be8a-607">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="6be8a-608">role：解决角色定义更新的相关问题 ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="6be8a-608">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="6be8a-609">create-for-rbac：确保已选取用户提供的密码</span><span class="sxs-lookup"><span data-stu-id="6be8a-609">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="6be8a-610">SQL</span><span class="sxs-lookup"><span data-stu-id="6be8a-610">SQL</span></span>

* <span data-ttu-id="6be8a-611">添加了 az sql server list-usages 和 az sql db list-usages 命令。</span><span class="sxs-lookup"><span data-stu-id="6be8a-611">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="6be8a-612">SQL - 能够直接连接到资源提供程序 ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="6be8a-612">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="6be8a-613">存储</span><span class="sxs-lookup"><span data-stu-id="6be8a-613">Storage</span></span>

* <span data-ttu-id="6be8a-614">位置默认为 `storage account create` 的资源组位置。</span><span class="sxs-lookup"><span data-stu-id="6be8a-614">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="6be8a-615">添加对增量 blob 复制的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-615">Add support for incremental blob copy</span></span>
* <span data-ttu-id="6be8a-616">添加对大型块 blob 上传的支持</span><span class="sxs-lookup"><span data-stu-id="6be8a-616">Add support for large block blob upload</span></span>
* <span data-ttu-id="6be8a-617">如果要上传的文件大于 200GB，则将块大小更改为 100MB</span><span class="sxs-lookup"><span data-stu-id="6be8a-617">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="6be8a-618">VM</span><span class="sxs-lookup"><span data-stu-id="6be8a-618">VM</span></span>

* <span data-ttu-id="6be8a-619">avail-set：将 UD 和 FD 域计数设为可选</span><span class="sxs-lookup"><span data-stu-id="6be8a-619">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="6be8a-620">注意：最高等级云中的 VM 命令。请避免与托管磁盘相关的功能，包括以下项：</span><span class="sxs-lookup"><span data-stu-id="6be8a-620">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="6be8a-621">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="6be8a-621">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="6be8a-622">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="6be8a-622">az vm/vmss disk</span></span>
  3. <span data-ttu-id="6be8a-623">在“az vm/vmss create”内，使用“—use-unmanaged-disk”避免托管磁盘 其他命令应有效</span><span class="sxs-lookup"><span data-stu-id="6be8a-623">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="6be8a-624">vm/vmss：改进生成 SSH 密钥对时的警告文本</span><span class="sxs-lookup"><span data-stu-id="6be8a-624">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="6be8a-625">vm/vmss：支持通过需要计划信息的市场映像创建 ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="6be8a-625">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="6be8a-626">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="6be8a-626">April 3, 2017</span></span>

<span data-ttu-id="6be8a-627">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="6be8a-627">Version 2.0.2</span></span>

<span data-ttu-id="6be8a-628">此版本中已发布 ACR、批处理、KeyVault 和 SQL 组件。</span><span class="sxs-lookup"><span data-stu-id="6be8a-628">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="6be8a-629">核心</span><span class="sxs-lookup"><span data-stu-id="6be8a-629">Core</span></span>

* <span data-ttu-id="6be8a-630">在默认列表中添加了 acr、实验室、监视和查找模块。</span><span class="sxs-lookup"><span data-stu-id="6be8a-630">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="6be8a-631">登录：跳过错误的租户 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="6be8a-631">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="6be8a-632">登录：将默认订阅设置为处于“已启用”状态的订阅 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="6be8a-632">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="6be8a-633">添加了 wait 命令，并添加了对其他命令的 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="6be8a-633">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="6be8a-634">核心：支持结合证书使用服务主体登录 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="6be8a-634">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="6be8a-635">添加了有关缺少模板参数的提示。</span><span class="sxs-lookup"><span data-stu-id="6be8a-635">Add prompting for missing template parameters.</span></span> <span data-ttu-id="6be8a-636">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="6be8a-636">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="6be8a-637">支持为资源组、默认 Web、 默认 VM 等常见参数设置默认值</span><span class="sxs-lookup"><span data-stu-id="6be8a-637">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="6be8a-638">支持登录到特定的租户</span><span class="sxs-lookup"><span data-stu-id="6be8a-638">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="6be8a-639">ACS</span><span class="sxs-lookup"><span data-stu-id="6be8a-639">ACS</span></span>

* <span data-ttu-id="6be8a-640">[ACS] 添加了配置默认 ACS 群集的支持 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="6be8a-640">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="6be8a-641">添加了 SSH 密钥密码提示的支持。</span><span class="sxs-lookup"><span data-stu-id="6be8a-641">Add support for ssh key password prompting.</span></span> <span data-ttu-id="6be8a-642">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="6be8a-642">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="6be8a-643">添加了对 Windows 群集的支持。</span><span class="sxs-lookup"><span data-stu-id="6be8a-643">Add support for windows clusters.</span></span> <span data-ttu-id="6be8a-644">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="6be8a-644">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="6be8a-645">从“所有者”角色切换到“参与者”角色。</span><span class="sxs-lookup"><span data-stu-id="6be8a-645">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="6be8a-646">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="6be8a-646">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="6be8a-647">应用服务</span><span class="sxs-lookup"><span data-stu-id="6be8a-647">AppService</span></span>

* <span data-ttu-id="6be8a-648">应用服务：支持获取用于 DNS A 记录的外部 IP 地址 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="6be8a-648">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="6be8a-649">应用服务：支持绑定通配符证书 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="6be8a-649">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="6be8a-650">应用服务：支持列出发布配置文件 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="6be8a-650">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="6be8a-651">应用服务 - 配置后触发源代码管理同步 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="6be8a-651">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="6be8a-652">DataLake</span><span class="sxs-lookup"><span data-stu-id="6be8a-652">DataLake</span></span>

* <span data-ttu-id="6be8a-653">Data Lake Analytics 模块的初始版本。</span><span class="sxs-lookup"><span data-stu-id="6be8a-653">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="6be8a-654">Data Lake Store 模块的初始版本。</span><span class="sxs-lookup"><span data-stu-id="6be8a-654">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="6be8a-655">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="6be8a-655">DocuemntDB</span></span>

* <span data-ttu-id="6be8a-656">DocumentDB：添加了列出连接字符串的支持 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="6be8a-656">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="6be8a-657">VM</span><span class="sxs-lookup"><span data-stu-id="6be8a-657">VM</span></span>

* <span data-ttu-id="6be8a-658">[计算] 添加了用于创建虚拟机规模集的应用网关支持 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="6be8a-658">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="6be8a-659">[VM/VMSS] 改进了磁盘缓存支持 ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="6be8a-659">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="6be8a-660">VM/VMSS：合并了门户使用的凭据验证逻辑 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="6be8a-660">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="6be8a-661">添加了 wait 命令和 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="6be8a-661">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="6be8a-662">虚拟机规模集：支持使用 * 列出不同 VM 上的实例视图 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="6be8a-662">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="6be8a-663">添加了适用于 VM 和虚拟机规模集的 --secrets ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="6be8a-663">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="6be8a-664">允许使用专用 VHD 创建 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="6be8a-664">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="6be8a-665">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="6be8a-665">February 27, 2017</span></span>

<span data-ttu-id="6be8a-666">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="6be8a-666">Version 2.0.0</span></span>

<span data-ttu-id="6be8a-667">此版 Azure CLI 2.0 是第一个“正式版”。</span><span class="sxs-lookup"><span data-stu-id="6be8a-667">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="6be8a-668">正式版适用于以下命令模块：</span><span class="sxs-lookup"><span data-stu-id="6be8a-668">General availability applies to these command modules:</span></span>
- <span data-ttu-id="6be8a-669">容器服务 (ACS)</span><span class="sxs-lookup"><span data-stu-id="6be8a-669">Container Service (acs)</span></span>
- <span data-ttu-id="6be8a-670">计算（包括 Resource Manager、VM、虚拟机规模集、托管磁盘）</span><span class="sxs-lookup"><span data-stu-id="6be8a-670">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="6be8a-671">网络</span><span class="sxs-lookup"><span data-stu-id="6be8a-671">Networking</span></span>
- <span data-ttu-id="6be8a-672">存储</span><span class="sxs-lookup"><span data-stu-id="6be8a-672">Storage</span></span>

<span data-ttu-id="6be8a-673">这些命令模块可在生产环境中使用，并受标准 Microsoft SLA 的支持。</span><span class="sxs-lookup"><span data-stu-id="6be8a-673">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="6be8a-674">可以直接向 Microsoft 支持部门或者通过 [github 问题列表](https://github.com/azure/azure-cli/issues/)提出问题。</span><span class="sxs-lookup"><span data-stu-id="6be8a-674">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="6be8a-675">可以[在 StackOverflow 上使用 azure-cli 标记](http://stackoverflow.com/questions/tagged/azure-cli)或者通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队来提出问题。可以通过命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="6be8a-675">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="6be8a-676">这些模块中的命令非常稳定，其语法在此 Azure CLI 版本的后续发行版中预期不会变化。</span><span class="sxs-lookup"><span data-stu-id="6be8a-676">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="6be8a-677">若要检查 CLI 版本，请使用 `az --version`。</span><span class="sxs-lookup"><span data-stu-id="6be8a-677">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="6be8a-678">输出中将列出 CLI 本身的版本（在此发行版中为 2.0.0）、各个命令模块的版本，以及所用 Python 和 GCC 的版本。</span><span class="sxs-lookup"><span data-stu-id="6be8a-678">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="6be8a-679">某些命令模块带有“bn”或“rcn”后缀。</span><span class="sxs-lookup"><span data-stu-id="6be8a-679">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="6be8a-680">这些命令模块仍以预览版提供，将来会发布正式版。</span><span class="sxs-lookup"><span data-stu-id="6be8a-680">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="6be8a-681">此外，我们还提供 CLI 夜间预览版。</span><span class="sxs-lookup"><span data-stu-id="6be8a-681">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="6be8a-682">有关信息，请参阅有关[获取夜间预览版](https://github.com/Azure/azure-cli#nightly-builds)的说明，以及有关[开发人员设置与贡献代码](https://github.com/Azure/azure-cli#developer-setup)的说明。</span><span class="sxs-lookup"><span data-stu-id="6be8a-682">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="6be8a-683">可通过以下方式报告夜间预览版的问题：</span><span class="sxs-lookup"><span data-stu-id="6be8a-683">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="6be8a-684">在 [github 问题列表](https://github.com/azure/azure-cli/issues/)中报告问题</span><span class="sxs-lookup"><span data-stu-id="6be8a-684">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="6be8a-685">通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队。</span><span class="sxs-lookup"><span data-stu-id="6be8a-685">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="6be8a-686">请通过命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="6be8a-686">Provide feedback from the command line with the `az feedback` command.</span></span>

