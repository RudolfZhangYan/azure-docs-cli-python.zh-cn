---
title: Azure CLI 2.0 发行说明
description: 了解 Azure CLI 2.0 的最新更新
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 07/03/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 8d4f0879a18d2cf99ea7a284155bec86413406f8
ms.sourcegitcommit: da34d0eecf19c676826bd32ab254a92bd0976124
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/19/2018
ms.locfileid: "39138230"
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="fc76f-103">Azure CLI 2.0 发行说明</span><span class="sxs-lookup"><span data-stu-id="fc76f-103">Azure CLI 2.0 release notes</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="fc76f-104">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-104">July 18, 2018</span></span>

<span data-ttu-id="fc76f-105">版本 2.0.42</span><span class="sxs-lookup"><span data-stu-id="fc76f-105">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="fc76f-106">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-106">Core</span></span>

* <span data-ttu-id="fc76f-107">在 WSL bash 窗口中添加了对基于浏览器的登录的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-107">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="fc76f-108">为所有通用更新命令添加了 `--force-string` 标志</span><span class="sxs-lookup"><span data-stu-id="fc76f-108">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="fc76f-109">[重大更改]更改了“show”命令以记录错误消息，并在缺少资源时退出代码为 3</span><span class="sxs-lookup"><span data-stu-id="fc76f-109">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="fc76f-110">ACR</span><span class="sxs-lookup"><span data-stu-id="fc76f-110">ACR</span></span>

* <span data-ttu-id="fc76f-111">[重大更改]在“acr build”命令中将“--no-push”更新为纯标志</span><span class="sxs-lookup"><span data-stu-id="fc76f-111">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="fc76f-112">在 `acr repository` 组下添加了 `show` 和 `update` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-112">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="fc76f-113">为 `show-manifests` 和 `show-tags`添加了 `--detail` 标记以显示更详细的信息</span><span class="sxs-lookup"><span data-stu-id="fc76f-113">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="fc76f-114">添加了 `--image` 参数以支持通过图像获取构建详细信息或日志</span><span class="sxs-lookup"><span data-stu-id="fc76f-114">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-115">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-115">ACS</span></span>

* <span data-ttu-id="fc76f-116">如果 `--max-pods` 小于 5，则将 `az aks create` 更改为错误输出</span><span class="sxs-lookup"><span data-stu-id="fc76f-116">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-117">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-117">AppService</span></span>

* <span data-ttu-id="fc76f-118">添加了对 PremiumV2 sku 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-118">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="fc76f-119">Batch</span><span class="sxs-lookup"><span data-stu-id="fc76f-119">Batch</span></span>

* <span data-ttu-id="fc76f-120">修复了在 Cloud Shell 模式下使用令牌凭据时的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-120">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="fc76f-121">将 JSON 输入更改为不区分大小写</span><span class="sxs-lookup"><span data-stu-id="fc76f-121">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="fc76f-122">Batch AI</span><span class="sxs-lookup"><span data-stu-id="fc76f-122">Batch AI</span></span>

* <span data-ttu-id="fc76f-123">修复了 `az batchai job exec` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-123">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="fc76f-124">容器</span><span class="sxs-lookup"><span data-stu-id="fc76f-124">Container</span></span>

* <span data-ttu-id="fc76f-125">删除了非 dockerhub 注册表的用户名和密码要求</span><span class="sxs-lookup"><span data-stu-id="fc76f-125">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="fc76f-126">修复了从 yaml 文件创建容器组时的错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-126">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-127">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-127">Network</span></span>

* <span data-ttu-id="fc76f-128">为 `network nic [create|update|delete]` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-128">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="fc76f-129">添加了 `network nic wait`</span><span class="sxs-lookup"><span data-stu-id="fc76f-129">Added `network nic wait`</span></span>
* <span data-ttu-id="fc76f-130">对 `network vnet [subnet|peering] list` 弃用了 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-130">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="fc76f-131">添加了 `--include-default` 标志以在 `network nsg rule list` 的输出中包含默认安全规则</span><span class="sxs-lookup"><span data-stu-id="fc76f-131">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="fc76f-132">资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-132">Resource</span></span>

* <span data-ttu-id="fc76f-133">为 `group deployment delete` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-133">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="fc76f-134">为 `deployment delete` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-134">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="fc76f-135">添加了 `deployment wait` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-135">Added `deployment wait` command</span></span>
* <span data-ttu-id="fc76f-136">修复了订阅级别 `az deployment` 命令对于配置文件 2017-03-09-profile 错误显示的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-136">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="fc76f-137">SQL</span><span class="sxs-lookup"><span data-stu-id="fc76f-137">SQL</span></span>

* <span data-ttu-id="fc76f-138">修复了为 `sql db copy` 和 `sql db replica create` 命令指定弹性池名称时“提供的资源组名称与 URL 中的名称不匹配”错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-138">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="fc76f-139">允许通过执行 `az configure --defaults sql-server=<name>` 配置默认 SQL Server</span><span class="sxs-lookup"><span data-stu-id="fc76f-139">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="fc76f-140">为 `sql server`、`sql server firewall-rule`、`sql list-usages` 和 `sql show-usage` 命令实现了表格式化程序</span><span class="sxs-lookup"><span data-stu-id="fc76f-140">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-141">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-141">Storage</span></span>

* <span data-ttu-id="fc76f-142">将 `pageRanges` 属性添加到了将为页 blob 填充的 `storage blob show` 输出</span><span class="sxs-lookup"><span data-stu-id="fc76f-142">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-143">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-143">VM</span></span>

* <span data-ttu-id="fc76f-144">[重大更改] 将 `vmss create` 更改为使用 `Standard_DS1_v2` 作为默认实例大小</span><span class="sxs-lookup"><span data-stu-id="fc76f-144">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="fc76f-145">向 `vm extension [set|delete]` 和 `vmss extension [set|delete]` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-145">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="fc76f-146">添加了 `vm extension wait`</span><span class="sxs-lookup"><span data-stu-id="fc76f-146">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="fc76f-147">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-147">July 3, 2018</span></span>

<span data-ttu-id="fc76f-148">版本 2.0.41</span><span class="sxs-lookup"><span data-stu-id="fc76f-148">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="fc76f-149">AKS</span><span class="sxs-lookup"><span data-stu-id="fc76f-149">AKS</span></span>

* <span data-ttu-id="fc76f-150">更改了监视以使用订阅 ID</span><span class="sxs-lookup"><span data-stu-id="fc76f-150">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="fc76f-151">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-151">July 3, 2018</span></span>

<span data-ttu-id="fc76f-152">版本 2.0.40</span><span class="sxs-lookup"><span data-stu-id="fc76f-152">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="fc76f-153">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-153">Core</span></span>

* <span data-ttu-id="fc76f-154">添加了用于交互式登录的新授权代码流</span><span class="sxs-lookup"><span data-stu-id="fc76f-154">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="fc76f-155">ACR</span><span class="sxs-lookup"><span data-stu-id="fc76f-155">ACR</span></span>

* <span data-ttu-id="fc76f-156">添加了轮询生成状态</span><span class="sxs-lookup"><span data-stu-id="fc76f-156">Added polling build status</span></span>
* <span data-ttu-id="fc76f-157">添加了对不区分大小写的枚举值的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-157">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="fc76f-158">为 `show-manifests` 添加了 `--top` 和 `--orderby` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-158">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-159">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-159">ACS</span></span>

* <span data-ttu-id="fc76f-160">[重大更改] 默认情况下启用 Kubernetes 基于角色的访问控制</span><span class="sxs-lookup"><span data-stu-id="fc76f-160">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="fc76f-161">添加了 `--disable-rbac` 参数并弃用了 `--enable-rbac`，因为它现在是默认值</span><span class="sxs-lookup"><span data-stu-id="fc76f-161">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="fc76f-162">更新了 `aks browse` 命令的选项。</span><span class="sxs-lookup"><span data-stu-id="fc76f-162">Updated options for `aks browse` command.</span></span> <span data-ttu-id="fc76f-163">增加了 `--listen-port` 支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-163">Added `--listen-port` support</span></span>
* <span data-ttu-id="fc76f-164">为 `aks install-connector` 命令更新了默认 helm chart 包。</span><span class="sxs-lookup"><span data-stu-id="fc76f-164">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="fc76f-165">使用 virtual-kubelet-for-aks-latest.tgz</span><span class="sxs-lookup"><span data-stu-id="fc76f-165">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="fc76f-166">添加了 `aks enable-addons` 和 `aks disable-addons` 命令以更新现有群集</span><span class="sxs-lookup"><span data-stu-id="fc76f-166">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-167">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-167">AppService</span></span>

* <span data-ttu-id="fc76f-168">添加了对通过 `webapp identity remove` 禁用标识的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-168">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="fc76f-169">删除了标识功能的 `preview` 标记</span><span class="sxs-lookup"><span data-stu-id="fc76f-169">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="fc76f-170">备份</span><span class="sxs-lookup"><span data-stu-id="fc76f-170">Backup</span></span>

* <span data-ttu-id="fc76f-171">更新了模块定义</span><span class="sxs-lookup"><span data-stu-id="fc76f-171">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="fc76f-172">BatchAI</span><span class="sxs-lookup"><span data-stu-id="fc76f-172">BatchAI</span></span>

* <span data-ttu-id="fc76f-173">修复了 `batchai cluster node list` 和 `batchai job node list` 命令的表输出</span><span class="sxs-lookup"><span data-stu-id="fc76f-173">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="fc76f-174">云</span><span class="sxs-lookup"><span data-stu-id="fc76f-174">Cloud</span></span>

* <span data-ttu-id="fc76f-175">为云配置添加了 `acr login` 服务器后缀</span><span class="sxs-lookup"><span data-stu-id="fc76f-175">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="fc76f-176">容器</span><span class="sxs-lookup"><span data-stu-id="fc76f-176">Container</span></span>

* <span data-ttu-id="fc76f-177">更改了 `container create` 以将其默认为长时间运行的操作</span><span class="sxs-lookup"><span data-stu-id="fc76f-177">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="fc76f-178">添加了 Log Analytics 参数 `--log-analytics-workspace` 和 `--log-analytics-workspace-key`</span><span class="sxs-lookup"><span data-stu-id="fc76f-178">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="fc76f-179">添加了 `--protocol` 参数来指定要使用哪个网络协议</span><span class="sxs-lookup"><span data-stu-id="fc76f-179">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="fc76f-180">分机</span><span class="sxs-lookup"><span data-stu-id="fc76f-180">Extension</span></span>

* <span data-ttu-id="fc76f-181">更改了 `extension list-available` 以仅显示与 CLI 版本兼容的扩展</span><span class="sxs-lookup"><span data-stu-id="fc76f-181">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-182">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-182">Network</span></span>

* <span data-ttu-id="fc76f-183">修复了记录类型区分大小写的问题 ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span><span class="sxs-lookup"><span data-stu-id="fc76f-183">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="fc76f-184">Rdbms</span><span class="sxs-lookup"><span data-stu-id="fc76f-184">Rdbms</span></span>

* <span data-ttu-id="fc76f-185">添加了 `[postgres|myql] server vnet-rule` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-185">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="fc76f-186">资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-186">Resource</span></span>

* <span data-ttu-id="fc76f-187">添加了新操作组 `deployment`</span><span class="sxs-lookup"><span data-stu-id="fc76f-187">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-188">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-188">VM</span></span>

* <span data-ttu-id="fc76f-189">添加了对删除系统分配标识的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-189">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="fc76f-190">2018 年 6 月 25日</span><span class="sxs-lookup"><span data-stu-id="fc76f-190">June 25, 2018</span></span>

<span data-ttu-id="fc76f-191">版本 2.0.39</span><span class="sxs-lookup"><span data-stu-id="fc76f-191">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="fc76f-192">CLI</span><span class="sxs-lookup"><span data-stu-id="fc76f-192">CLI</span></span>

* <span data-ttu-id="fc76f-193">更新了 MSI 安装程序中的文件修整以修复扩展安装问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-193">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="fc76f-194">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-194">June 19, 2018</span></span>

<span data-ttu-id="fc76f-195">版本 2.0.38</span><span class="sxs-lookup"><span data-stu-id="fc76f-195">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="fc76f-196">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-196">Core</span></span>

* <span data-ttu-id="fc76f-197">为大多数命令增加了对 `--subscription` 的全局支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-197">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="fc76f-198">ACR</span><span class="sxs-lookup"><span data-stu-id="fc76f-198">ACR</span></span>

* <span data-ttu-id="fc76f-199">增加了 `azure-storage-blob` 作为依赖项</span><span class="sxs-lookup"><span data-stu-id="fc76f-199">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="fc76f-200">更改了 `acr build-task create` 的默认 CPU 配置，允许使用 2 核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-200">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-201">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-201">ACS</span></span>

* <span data-ttu-id="fc76f-202">更新了 `aks use-dev-spaces` 命令的选项。</span><span class="sxs-lookup"><span data-stu-id="fc76f-202">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="fc76f-203">增加了 `--update` 支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-203">Added `--update` support</span></span>
* <span data-ttu-id="fc76f-204">更改了 `aks get-credentials --admin`，不替换 `$HOME/.kube/config` 中的用户上下文</span><span class="sxs-lookup"><span data-stu-id="fc76f-204">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="fc76f-205">公开了托管群集上的只读 `nodeResourceGroup` 属性</span><span class="sxs-lookup"><span data-stu-id="fc76f-205">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="fc76f-206">修复了 `acs browse` 命令错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-206">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="fc76f-207">将 `--connector-name` 设置为 `aks install-connector`、`aks upgrade-connector` 和 `aks remove-connector` 的可选项</span><span class="sxs-lookup"><span data-stu-id="fc76f-207">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="fc76f-208">为 `aks install-connector` 增加了新的 Azure 容器实例区域</span><span class="sxs-lookup"><span data-stu-id="fc76f-208">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="fc76f-209">为 helm 版本名称增加了规范化位置，并为 `aks install-connector` 增加了节点名称</span><span class="sxs-lookup"><span data-stu-id="fc76f-209">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-210">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-210">AppService</span></span>

* <span data-ttu-id="fc76f-211">增加了对更新版 urllib 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-211">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="fc76f-212">为 `functionapp create` 增加了支持，可以使用外部资源组的应用服务计划</span><span class="sxs-lookup"><span data-stu-id="fc76f-212">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="fc76f-213">Batch</span><span class="sxs-lookup"><span data-stu-id="fc76f-213">Batch</span></span>

* <span data-ttu-id="fc76f-214">删除了 `azure-batch-extensions` 依赖项</span><span class="sxs-lookup"><span data-stu-id="fc76f-214">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="fc76f-215">Batch AI</span><span class="sxs-lookup"><span data-stu-id="fc76f-215">Batch AI</span></span>

* <span data-ttu-id="fc76f-216">添加了对工作区的支持。</span><span class="sxs-lookup"><span data-stu-id="fc76f-216">Added support for workspaces.</span></span> <span data-ttu-id="fc76f-217">可以通过工作区将群集、文件服务器和试验按组分组，去除了对可以创建的资源数的限制</span><span class="sxs-lookup"><span data-stu-id="fc76f-217">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="fc76f-218">增加了对试验的支持。</span><span class="sxs-lookup"><span data-stu-id="fc76f-218">Added support for experiments.</span></span> <span data-ttu-id="fc76f-219">可以通过试验将作业按集合分组，去除了对已创建作业的数目限制</span><span class="sxs-lookup"><span data-stu-id="fc76f-219">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="fc76f-220">增加了为 Docker 容器中运行的作业配置 `/dev/shm` 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-220">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="fc76f-221">增加了 `batchai cluster node exec` 和 `batchai job node exec` 命令。</span><span class="sxs-lookup"><span data-stu-id="fc76f-221">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="fc76f-222">这些命令允许在节点上直接执行任何命令，提供用于端口转发的功能。</span><span class="sxs-lookup"><span data-stu-id="fc76f-222">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="fc76f-223">为 `batchai` 命令增加了对 `--ids` 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-223">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="fc76f-224">[重大更改] 所有群集和文件服务器必须在工作区创建</span><span class="sxs-lookup"><span data-stu-id="fc76f-224">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="fc76f-225">[重大更改] 作业必须在试验中创建</span><span class="sxs-lookup"><span data-stu-id="fc76f-225">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="fc76f-226">[重大更改] 从 `cluster create` 和 `job create` 命令中删除了 `--nfs-resource-group`。</span><span class="sxs-lookup"><span data-stu-id="fc76f-226">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="fc76f-227">若要装载属于其他工作区/资源组的 NFS，请通过 `--nfs` 选项提供文件服务器的 ARM ID</span><span class="sxs-lookup"><span data-stu-id="fc76f-227">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="fc76f-228">[重大更改] 从 `job create` 命令中删除了 `--cluster-resource-group`。</span><span class="sxs-lookup"><span data-stu-id="fc76f-228">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="fc76f-229">若要在属于其他工作区/资源组的群集上提交作业，请通过 `--cluster` 选项提供群集的 ARM ID</span><span class="sxs-lookup"><span data-stu-id="fc76f-229">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="fc76f-230">[重大更改] 从作业、群集和文件服务器中删除了 `location` 特性。</span><span class="sxs-lookup"><span data-stu-id="fc76f-230">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="fc76f-231">位置现在是工作区的特性。</span><span class="sxs-lookup"><span data-stu-id="fc76f-231">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="fc76f-232">[重大更改] 从 `job create`、`cluster create` 和 `file-server create` 命令中删除了 `--location`</span><span class="sxs-lookup"><span data-stu-id="fc76f-232">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="fc76f-233">[重大更改] 更改了短选项的名称，使接口更一致：</span><span class="sxs-lookup"><span data-stu-id="fc76f-233">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
 - <span data-ttu-id="fc76f-234">[`--config`, `-c`] 已重命名为 [`--config-file`, `-f`]</span><span class="sxs-lookup"><span data-stu-id="fc76f-234">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
 - <span data-ttu-id="fc76f-235">[`--cluster`, `-r`] 已重命名为 [`--cluster`, `-c`]</span><span class="sxs-lookup"><span data-stu-id="fc76f-235">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
 - <span data-ttu-id="fc76f-236">[`--cluster`, `-n`] 已重命名为 [`--cluster`, `-c`]</span><span class="sxs-lookup"><span data-stu-id="fc76f-236">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
 - <span data-ttu-id="fc76f-237">[`--job`, `-n`] 已重命名为 [`--job`, `-j`]</span><span class="sxs-lookup"><span data-stu-id="fc76f-237">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="fc76f-238">地图</span><span class="sxs-lookup"><span data-stu-id="fc76f-238">Maps</span></span>

* <span data-ttu-id="fc76f-239">[重大更改] 更改了 `maps account create`，要求通过交互式提示或 `--accept-tos` 标志接受《服务条款》</span><span class="sxs-lookup"><span data-stu-id="fc76f-239">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-240">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-240">Network</span></span>

* <span data-ttu-id="fc76f-241">为 `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571) 增加了对 `https` 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-241">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="fc76f-242">修复了 `--endpoint-status` 区分大小写的问题。</span><span class="sxs-lookup"><span data-stu-id="fc76f-242">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="fc76f-243">#6502</span><span class="sxs-lookup"><span data-stu-id="fc76f-243">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="fc76f-244">预留</span><span class="sxs-lookup"><span data-stu-id="fc76f-244">Reservations</span></span>

* <span data-ttu-id="fc76f-245">[重大更改] 为 `reservations catalog show` 增加了必需参数 `ReservedResourceType`</span><span class="sxs-lookup"><span data-stu-id="fc76f-245">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="fc76f-246">为 `reservations catalog show` 增加了参数 `Location`</span><span class="sxs-lookup"><span data-stu-id="fc76f-246">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="fc76f-247">[重大更改] 从 `ReservationProperties` 中删除了 `kind`</span><span class="sxs-lookup"><span data-stu-id="fc76f-247">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="fc76f-248">[重大更改] 已在 `Catalog` 中将 `capabilities` 重命名为 `sku_properties`</span><span class="sxs-lookup"><span data-stu-id="fc76f-248">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="fc76f-249">[重大更改] 从 `Catalog` 中删除了 `size` 和 `tier` 属性</span><span class="sxs-lookup"><span data-stu-id="fc76f-249">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="fc76f-250">为 `reservations reservation update` 增加了参数 `InstanceFlexibility`</span><span class="sxs-lookup"><span data-stu-id="fc76f-250">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="fc76f-251">角色</span><span class="sxs-lookup"><span data-stu-id="fc76f-251">Role</span></span>

* <span data-ttu-id="fc76f-252">改进了错误处理</span><span class="sxs-lookup"><span data-stu-id="fc76f-252">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="fc76f-253">SQL</span><span class="sxs-lookup"><span data-stu-id="fc76f-253">SQL</span></span>

* <span data-ttu-id="fc76f-254">修复了针对不可供订阅使用的位置运行 `az sql db list-editions` 时出现的令人困惑的错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-254">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-255">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-255">Storage</span></span>

* <span data-ttu-id="fc76f-256">更改了 `storage blob download` 的表输出，使之更为可读</span><span class="sxs-lookup"><span data-stu-id="fc76f-256">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-257">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-257">VM</span></span>

* <span data-ttu-id="fc76f-258">针对 `vm create` 中的加速网络支持，改进了 refine vm size check</span><span class="sxs-lookup"><span data-stu-id="fc76f-258">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="fc76f-259">增加了针对 `vmss create` 的警告：默认的 VM 大小将从 `Standard_D1_v2` 切换为 `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="fc76f-259">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="fc76f-260">为 `[vm|vmss] extension set` 增加了 `--force-update`，即使在配置未变的情况下也可以更新扩展</span><span class="sxs-lookup"><span data-stu-id="fc76f-260">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="fc76f-261">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-261">June 13, 2018</span></span>

<span data-ttu-id="fc76f-262">版本 2.0.37</span><span class="sxs-lookup"><span data-stu-id="fc76f-262">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="fc76f-263">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-263">Core</span></span>

* <span data-ttu-id="fc76f-264">改进了交互式遥测</span><span class="sxs-lookup"><span data-stu-id="fc76f-264">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="fc76f-265">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-265">June 13, 2018</span></span>

<span data-ttu-id="fc76f-266">版本 2.0.36</span><span class="sxs-lookup"><span data-stu-id="fc76f-266">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="fc76f-267">AKS</span><span class="sxs-lookup"><span data-stu-id="fc76f-267">AKS</span></span>

* <span data-ttu-id="fc76f-268">为 `aks create` 添加了高级网络选项</span><span class="sxs-lookup"><span data-stu-id="fc76f-268">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="fc76f-269">为 `aks create` 添加了参数以启用监视和 HTTP 路由</span><span class="sxs-lookup"><span data-stu-id="fc76f-269">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="fc76f-270">为 `aks create` 添加了 `--no-ssh-key` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-270">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="fc76f-271">为 `aks create` 添加了 `--enable-rbac` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-271">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="fc76f-272">[PREVIEW] 为 `aks create` 添加了对 Azure Active Directory 身份验证的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-272">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-273">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-273">AppService</span></span>

* <span data-ttu-id="fc76f-274">修复了不兼容 urllib 版本的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-274">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="fc76f-275">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-275">June 5, 2018</span></span>

<span data-ttu-id="fc76f-276">版本 2.0.35</span><span class="sxs-lookup"><span data-stu-id="fc76f-276">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="fc76f-277">交互</span><span class="sxs-lookup"><span data-stu-id="fc76f-277">Interactive</span></span>

* <span data-ttu-id="fc76f-278">添加了对交互模式的依赖项的限制</span><span class="sxs-lookup"><span data-stu-id="fc76f-278">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="fc76f-279">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-279">June 5, 2018</span></span>

<span data-ttu-id="fc76f-280">版本 2.0.34</span><span class="sxs-lookup"><span data-stu-id="fc76f-280">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="fc76f-281">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-281">Core</span></span>

* <span data-ttu-id="fc76f-282">增加了对跨租户资源引用的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-282">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="fc76f-283">增强了遥测数据上传可靠性</span><span class="sxs-lookup"><span data-stu-id="fc76f-283">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="fc76f-284">ACR</span><span class="sxs-lookup"><span data-stu-id="fc76f-284">ACR</span></span>

* <span data-ttu-id="fc76f-285">增加了对 VSTS 充当远程源位置的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-285">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="fc76f-286">添加了 `acr import` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-286">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="fc76f-287">AKS</span><span class="sxs-lookup"><span data-stu-id="fc76f-287">AKS</span></span>

* <span data-ttu-id="fc76f-288">更改了 `aks get-credentials`，可以使用更安全的文件系统权限来创建 kube 配置文件</span><span class="sxs-lookup"><span data-stu-id="fc76f-288">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="fc76f-289">Batch</span><span class="sxs-lookup"><span data-stu-id="fc76f-289">Batch</span></span>

* <span data-ttu-id="fc76f-290">修复了池列表表格式设置中的 Bug [[问题 #4378](https://github.com/Azure/azure-cli/issues/4378)]</span><span class="sxs-lookup"><span data-stu-id="fc76f-290">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="fc76f-291">IOT</span><span class="sxs-lookup"><span data-stu-id="fc76f-291">IOT</span></span>

* <span data-ttu-id="fc76f-292">增加了对创建基本层 IoT 中心的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-292">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-293">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-293">Network</span></span>

* <span data-ttu-id="fc76f-294">改进了 `network vnet peering`</span><span class="sxs-lookup"><span data-stu-id="fc76f-294">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="fc76f-295">策略见解</span><span class="sxs-lookup"><span data-stu-id="fc76f-295">Policy Insights</span></span>

* <span data-ttu-id="fc76f-296">初始版本</span><span class="sxs-lookup"><span data-stu-id="fc76f-296">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="fc76f-297">ARM</span><span class="sxs-lookup"><span data-stu-id="fc76f-297">ARM</span></span>

* <span data-ttu-id="fc76f-298">增加了 `account management-group` 命令。</span><span class="sxs-lookup"><span data-stu-id="fc76f-298">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="fc76f-299">SQL</span><span class="sxs-lookup"><span data-stu-id="fc76f-299">SQL</span></span>

* <span data-ttu-id="fc76f-300">增加了新的托管实例命令：</span><span class="sxs-lookup"><span data-stu-id="fc76f-300">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="fc76f-301">增加了新的托管数据库命令：</span><span class="sxs-lookup"><span data-stu-id="fc76f-301">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="fc76f-302">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-302">Storage</span></span>

* <span data-ttu-id="fc76f-303">增加了可以从文件扩展名推断且适用于 json 和 javascript 的额外 mimetype</span><span class="sxs-lookup"><span data-stu-id="fc76f-303">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-304">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-304">VM</span></span>

* <span data-ttu-id="fc76f-305">更改了 `vm list-skus`，可以使用固定列并可添加表明要删除 `Tier` 和 `Size` 的警告</span><span class="sxs-lookup"><span data-stu-id="fc76f-305">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="fc76f-306">为 `vm create` 添加了 `--accelerated-networking` 选项</span><span class="sxs-lookup"><span data-stu-id="fc76f-306">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="fc76f-307">为 `identity create` 添加了 `--tags`</span><span class="sxs-lookup"><span data-stu-id="fc76f-307">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="fc76f-308">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-308">May 22, 2018</span></span>

<span data-ttu-id="fc76f-309">版本 2.0.33</span><span class="sxs-lookup"><span data-stu-id="fc76f-309">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="fc76f-310">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-310">Core</span></span>

* <span data-ttu-id="fc76f-311">增加了对在文件名中扩展 `@` 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-311">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-312">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-312">ACS</span></span>

* <span data-ttu-id="fc76f-313">增加了新的 Dev-Spaces 命令：`aks use-dev-spaces` 和 `aks remove-dev-spaces`</span><span class="sxs-lookup"><span data-stu-id="fc76f-313">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="fc76f-314">修复了帮助消息中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-314">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-315">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-315">AppService</span></span>

* <span data-ttu-id="fc76f-316">改进了泛型更新命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-316">Improved generic update commands</span></span>
* <span data-ttu-id="fc76f-317">增加了对 `webapp deployment source config-zip` 的异步支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-317">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="fc76f-318">容器</span><span class="sxs-lookup"><span data-stu-id="fc76f-318">Container</span></span>

* <span data-ttu-id="fc76f-319">增加了对以 yaml 格式导出容器组的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-319">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="fc76f-320">增加了对使用 yaml 文件创建/更新容器组的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-320">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="fc76f-321">分机</span><span class="sxs-lookup"><span data-stu-id="fc76f-321">Extension</span></span>

* <span data-ttu-id="fc76f-322">改进了扩展的删除方式</span><span class="sxs-lookup"><span data-stu-id="fc76f-322">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="fc76f-323">交互</span><span class="sxs-lookup"><span data-stu-id="fc76f-323">Interactive</span></span>

* <span data-ttu-id="fc76f-324">更改了日志记录，在完成时将分析器静音</span><span class="sxs-lookup"><span data-stu-id="fc76f-324">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="fc76f-325">改进了错误的帮助缓存的处理</span><span class="sxs-lookup"><span data-stu-id="fc76f-325">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="fc76f-326">KeyVault</span><span class="sxs-lookup"><span data-stu-id="fc76f-326">KeyVault</span></span>

* <span data-ttu-id="fc76f-327">修复了 keyvault 命令，使之可以在 Cloud Shell 或 VM 中与标识一起使用</span><span class="sxs-lookup"><span data-stu-id="fc76f-327">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-328">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-328">Network</span></span>

* <span data-ttu-id="fc76f-329">修复了 `network watcher show-topology` 无法与 vnet 和/或子网名称一起使用的问题 [#6326](https://github.com/Azure/azure-cli/issues/6326)</span><span class="sxs-lookup"><span data-stu-id="fc76f-329">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="fc76f-330">修复了某些 `network watcher` 命令宣称未为区域启用网络观察程序而实际上却已经启用的问题 [#6264](https://github.com/Azure/azure-cli/issues/6264)</span><span class="sxs-lookup"><span data-stu-id="fc76f-330">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="fc76f-331">SQL</span><span class="sxs-lookup"><span data-stu-id="fc76f-331">SQL</span></span>

* <span data-ttu-id="fc76f-332">[重大更改] 更改了从 `db` 和 `dw` 命令返回的响应对象：</span><span class="sxs-lookup"><span data-stu-id="fc76f-332">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="fc76f-333">已将 `serviceLevelObjective` 属性重命名为 `currentServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="fc76f-333">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="fc76f-334">删除了 `currentServiceObjectiveId` 和 `requestedServiceObjectiveId` 属性</span><span class="sxs-lookup"><span data-stu-id="fc76f-334">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="fc76f-335">已将 `maxSizeBytes` 属性更改为整数值而不是字符串</span><span class="sxs-lookup"><span data-stu-id="fc76f-335">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="fc76f-336">[重大更改] 已将下面的 `db` 和 `dw` 属性更改为只读：</span><span class="sxs-lookup"><span data-stu-id="fc76f-336">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="fc76f-337">`requestedServiceObjectiveName`。</span><span class="sxs-lookup"><span data-stu-id="fc76f-337">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="fc76f-338">若要更新，请使用 `--service-objective` 参数或设置 `sku.name` 属性</span><span class="sxs-lookup"><span data-stu-id="fc76f-338">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="fc76f-339">`edition`。</span><span class="sxs-lookup"><span data-stu-id="fc76f-339">`edition`.</span></span> <span data-ttu-id="fc76f-340">若要更新，请使用 `--edition` 参数或设置 `sku.tier` 属性</span><span class="sxs-lookup"><span data-stu-id="fc76f-340">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="fc76f-341">`elasticPoolName`。</span><span class="sxs-lookup"><span data-stu-id="fc76f-341">`elasticPoolName`.</span></span> <span data-ttu-id="fc76f-342">若要更新，请使用 `--elastic-pool` 参数或设置 `elasticPoolId` 属性</span><span class="sxs-lookup"><span data-stu-id="fc76f-342">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="fc76f-343">[重大更改] 已将下面的 `elastic-pool` 属性更改为只读：</span><span class="sxs-lookup"><span data-stu-id="fc76f-343">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="fc76f-344">`edition`。</span><span class="sxs-lookup"><span data-stu-id="fc76f-344">`edition`.</span></span> <span data-ttu-id="fc76f-345">若要更新，请使用 `--edition` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-345">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="fc76f-346">`dtu`。</span><span class="sxs-lookup"><span data-stu-id="fc76f-346">`dtu`.</span></span> <span data-ttu-id="fc76f-347">若要更新，请使用 `--capacity` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-347">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="fc76f-348">`databaseDtuMin`。</span><span class="sxs-lookup"><span data-stu-id="fc76f-348">`databaseDtuMin`.</span></span> <span data-ttu-id="fc76f-349">若要更新，请使用 `--db-min-capacity` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-349">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="fc76f-350">`databaseDtuMax`。</span><span class="sxs-lookup"><span data-stu-id="fc76f-350">`databaseDtuMax`.</span></span> <span data-ttu-id="fc76f-351">若要更新，请使用 `--db-max-capacity` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-351">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="fc76f-352">为 `db`、`dw` 和 `elastic-pool` 命令增加了 `--family` 和 `--capacity` 参数。</span><span class="sxs-lookup"><span data-stu-id="fc76f-352">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="fc76f-353">为 `db`、`dw` 和 `elastic-pool` 命令增加了表格式化程序。</span><span class="sxs-lookup"><span data-stu-id="fc76f-353">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-354">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-354">Storage</span></span>

* <span data-ttu-id="fc76f-355">增加了 `--account-name` 参数的补全选项</span><span class="sxs-lookup"><span data-stu-id="fc76f-355">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="fc76f-356">修复了 `storage entity query` 的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-356">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-357">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-357">VM</span></span>

* <span data-ttu-id="fc76f-358">[重大更改] 从 `vm create` 中删除了 `--write-accelerator`。</span><span class="sxs-lookup"><span data-stu-id="fc76f-358">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="fc76f-359">可以通过 `vm update` 或 `vm disk attach` 访问同一支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-359">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="fc76f-360">修复了 `[vm|vmss] extension` 中的扩展映像匹配问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-360">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="fc76f-361">为 `vm create` 添加了 `--boot-diagnostics-storage`，可以捕获启动日志</span><span class="sxs-lookup"><span data-stu-id="fc76f-361">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="fc76f-362">为 `[vm|vmss] update` 添加了 `--license-type`</span><span class="sxs-lookup"><span data-stu-id="fc76f-362">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="fc76f-363">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-363">May 7, 2018</span></span>

<span data-ttu-id="fc76f-364">版本 2.0.32</span><span class="sxs-lookup"><span data-stu-id="fc76f-364">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="fc76f-365">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-365">Core</span></span>

* <span data-ttu-id="fc76f-366">修复了使用证书从服务主体帐户检索机密时引发未处理异常的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-366">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="fc76f-367">增加了对位置参数的有限支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-367">Added limited support for positional arguments</span></span>
* <span data-ttu-id="fc76f-368">修复了 `--query` 无法与 `--ids` 一起使用的问题。</span><span class="sxs-lookup"><span data-stu-id="fc76f-368">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="fc76f-369">#5591</span><span class="sxs-lookup"><span data-stu-id="fc76f-369">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="fc76f-370">改进了使用 `--ids` 时通过命令执行的管道方案。</span><span class="sxs-lookup"><span data-stu-id="fc76f-370">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="fc76f-371">支持在指定查询的情况下使用 `-o tsv`，或者在不指定查询的情况下使用 `-o json`</span><span class="sxs-lookup"><span data-stu-id="fc76f-371">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="fc76f-372">增加了在用户的命令中存在拼写错误的情况下，针对错误提供命令建议的功能</span><span class="sxs-lookup"><span data-stu-id="fc76f-372">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="fc76f-373">改进了用户键入 `az ''` 时出现的错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-373">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="fc76f-374">增加了针对命令模块和扩展自定义资源类型的功能</span><span class="sxs-lookup"><span data-stu-id="fc76f-374">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="fc76f-375">ACR</span><span class="sxs-lookup"><span data-stu-id="fc76f-375">ACR</span></span>

* <span data-ttu-id="fc76f-376">增加了 ACR 生成命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-376">Added ACR Build commands</span></span>
* <span data-ttu-id="fc76f-377">改进了“找不到资源”类型的错误消息</span><span class="sxs-lookup"><span data-stu-id="fc76f-377">Improved resource not found error messages</span></span>
* <span data-ttu-id="fc76f-378">改进了资源创建性能和错误处理</span><span class="sxs-lookup"><span data-stu-id="fc76f-378">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="fc76f-379">改进了 acr 登录非标准控制台和 WSL</span><span class="sxs-lookup"><span data-stu-id="fc76f-379">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="fc76f-380">改进了存储库命令错误消息</span><span class="sxs-lookup"><span data-stu-id="fc76f-380">Improved repository commands error messages</span></span>
* <span data-ttu-id="fc76f-381">更新了表列和排序</span><span class="sxs-lookup"><span data-stu-id="fc76f-381">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-382">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-382">ACS</span></span>

* <span data-ttu-id="fc76f-383">增加了“`az aks` 是预览版服务”警告</span><span class="sxs-lookup"><span data-stu-id="fc76f-383">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="fc76f-384">修复了未指定 `--aci-resource-group` 时 `aks install-connector` 中的权限问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-384">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="fc76f-385">AMS</span><span class="sxs-lookup"><span data-stu-id="fc76f-385">AMS</span></span>

* <span data-ttu-id="fc76f-386">初始版本 - 管理 Azure 媒体服务资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-386">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-387">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-387">Appservice</span></span>

* <span data-ttu-id="fc76f-388">修复了提供 `--slot` 时 `webapp delete` 中的 Bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-388">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="fc76f-389">从 `webapp auth update` 删除了 `--runtime-version`</span><span class="sxs-lookup"><span data-stu-id="fc76f-389">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="fc76f-390">增加了对 min\_tls\_version & https2.0 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-390">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="fc76f-391">增加了对多容器的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-391">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="fc76f-392">Batch AI</span><span class="sxs-lookup"><span data-stu-id="fc76f-392">Batch AI</span></span>

* <span data-ttu-id="fc76f-393">更改了 `batchai create cluster`，以便遵循在群集的配置文件中配置的 VM 优先级</span><span class="sxs-lookup"><span data-stu-id="fc76f-393">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="fc76f-394">认知服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-394">Cognitive Services</span></span>

* <span data-ttu-id="fc76f-395">修复了在 `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603) 的示例中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-395">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="fc76f-396">消耗</span><span class="sxs-lookup"><span data-stu-id="fc76f-396">Consumption</span></span>

* <span data-ttu-id="fc76f-397">增加了预算 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-397">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="fc76f-398">容器</span><span class="sxs-lookup"><span data-stu-id="fc76f-398">Container</span></span>

* <span data-ttu-id="fc76f-399">删除了在映像名称中包括注册表服务器时对 `container create` 命令的 `--registry-server` 参数的要求</span><span class="sxs-lookup"><span data-stu-id="fc76f-399">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="fc76f-400">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="fc76f-400">Cosmos DB</span></span>

* <span data-ttu-id="fc76f-401">引入针对 Azure CLI 的 VNET 支持 - Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="fc76f-401">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="fc76f-402">DMS</span><span class="sxs-lookup"><span data-stu-id="fc76f-402">DMS</span></span>

* <span data-ttu-id="fc76f-403">初始版本 - 为 Azure SQL 迁移方案增加了对 SQL 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-403">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="fc76f-404">分机</span><span class="sxs-lookup"><span data-stu-id="fc76f-404">Extension</span></span>

* <span data-ttu-id="fc76f-405">修复了停止显示扩展元数据的 Bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-405">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="fc76f-406">交互</span><span class="sxs-lookup"><span data-stu-id="fc76f-406">Interactive</span></span>

* <span data-ttu-id="fc76f-407">允许交互式补全选项使用位置参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-407">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="fc76f-408">增强用户键入 '\' 时的输出的用户友好性</span><span class="sxs-lookup"><span data-stu-id="fc76f-408">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="fc76f-409">修复了在没有帮助的情况下参数的补全问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-409">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="fc76f-410">修复了命令组的说明问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-410">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="fc76f-411">实验室</span><span class="sxs-lookup"><span data-stu-id="fc76f-411">Lab</span></span>

* <span data-ttu-id="fc76f-412">修复了 Knack 转换的回归问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-412">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-413">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-413">Network</span></span>

* <span data-ttu-id="fc76f-414">[重大更改] 删除了以下项的 `--ids` 参数：</span><span class="sxs-lookup"><span data-stu-id="fc76f-414">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="fc76f-415">配置文件</span><span class="sxs-lookup"><span data-stu-id="fc76f-415">Profile</span></span>

* <span data-ttu-id="fc76f-416">修复了 `disk create` 源检测问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-416">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="fc76f-417">[重大更改] 删除了不再使用的 `--msi-port` 和 `--identity-port`</span><span class="sxs-lookup"><span data-stu-id="fc76f-417">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="fc76f-418">修复了 `account get-access-token` 短摘要中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-418">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="fc76f-419">Redis</span><span class="sxs-lookup"><span data-stu-id="fc76f-419">Redis</span></span>

* <span data-ttu-id="fc76f-420">弃用 `redis patch-schedule patch-schedule show` 而改用 `redis patch-schedule show`</span><span class="sxs-lookup"><span data-stu-id="fc76f-420">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="fc76f-421">弃用 `redis list-all`。</span><span class="sxs-lookup"><span data-stu-id="fc76f-421">Deprecated `redis list-all`.</span></span> <span data-ttu-id="fc76f-422">此功能已加入 `redis list` 中</span><span class="sxs-lookup"><span data-stu-id="fc76f-422">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="fc76f-423">弃用 `redis import-method` 而改用 `redis import`</span><span class="sxs-lookup"><span data-stu-id="fc76f-423">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="fc76f-424">为各种命令增加了对 `--ids` 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-424">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="fc76f-425">角色</span><span class="sxs-lookup"><span data-stu-id="fc76f-425">Role</span></span>

* <span data-ttu-id="fc76f-426">[重大更改] 删除了已弃用的 `ad sp reset-credentials`</span><span class="sxs-lookup"><span data-stu-id="fc76f-426">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-427">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-427">Storage</span></span>

* <span data-ttu-id="fc76f-428">在源 SAS 和帐户密钥未指定的情况下，允许将目标 SAS 令牌应用到源，以便进行 Blob 复制</span><span class="sxs-lookup"><span data-stu-id="fc76f-428">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="fc76f-429">公开了用于 Blob 上传和下载的 --socket-timeout 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-429">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="fc76f-430">将以路径分隔符开头的 Blob 名称视为相对路径</span><span class="sxs-lookup"><span data-stu-id="fc76f-430">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="fc76f-431">允许 `storage blob copy --source-sas` 以查询字符“?”开头</span><span class="sxs-lookup"><span data-stu-id="fc76f-431">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="fc76f-432">修复了 `storage entity query --marker` 问题，接受“键=值”列表</span><span class="sxs-lookup"><span data-stu-id="fc76f-432">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-433">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-433">VM</span></span>

* <span data-ttu-id="fc76f-434">修复了非托管 Blob URI 上的检测逻辑无效的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-434">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="fc76f-435">增加了在没有用户提供的服务主体的情况下进行磁盘加密的功能</span><span class="sxs-lookup"><span data-stu-id="fc76f-435">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="fc76f-436">[重大更改] 请勿使用 VM“ManagedIdentityExtension”来寻求 MSI 支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-436">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="fc76f-437">增加了对 `vmss` 使用逐出策略的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-437">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="fc76f-438">[重大更改] 从以下项删除了 `--ids`：</span><span class="sxs-lookup"><span data-stu-id="fc76f-438">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="fc76f-439">增加了写入加速器支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-439">Added write accelerator support</span></span>
* <span data-ttu-id="fc76f-440">添加了 `vmss perform-maintenance`</span><span class="sxs-lookup"><span data-stu-id="fc76f-440">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="fc76f-441">修复了 `vm diagnostics set` 问题，可以可靠地检测 VM 的 OS 类型</span><span class="sxs-lookup"><span data-stu-id="fc76f-441">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="fc76f-442">更改了 `vm resize`，系统会检查请求的大小是否不同于当前设置的大小，只在二者有变化时进行更新</span><span class="sxs-lookup"><span data-stu-id="fc76f-442">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="fc76f-443">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-443">April 10, 2018</span></span>

<span data-ttu-id="fc76f-444">版本 2.0.31</span><span class="sxs-lookup"><span data-stu-id="fc76f-444">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="fc76f-445">ACR</span><span class="sxs-lookup"><span data-stu-id="fc76f-445">ACR</span></span>

* <span data-ttu-id="fc76f-446">改进了 wincred 回退错误处理</span><span class="sxs-lookup"><span data-stu-id="fc76f-446">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-447">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-447">ACS</span></span>

* <span data-ttu-id="fc76f-448">更改了 aks 创建的 SPN，使其有效期达到 5 年</span><span class="sxs-lookup"><span data-stu-id="fc76f-448">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-449">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-449">Appservice</span></span>

* [重大更改]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="fc76f-451">修复了 Web 应用计划不存在导致的未捕获异常</span><span class="sxs-lookup"><span data-stu-id="fc76f-451">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="fc76f-452">BatchAI</span><span class="sxs-lookup"><span data-stu-id="fc76f-452">BatchAI</span></span>

* <span data-ttu-id="fc76f-453">添加了对 2018-03-01 API 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-453">Added support for 2018-03-01 API</span></span>

 - <span data-ttu-id="fc76f-454">作业级装载</span><span class="sxs-lookup"><span data-stu-id="fc76f-454">Job level mounting</span></span>
 - <span data-ttu-id="fc76f-455">使用机密值的环境变量</span><span class="sxs-lookup"><span data-stu-id="fc76f-455">Environment variables with secret values</span></span>
 - <span data-ttu-id="fc76f-456">性能计数器设置</span><span class="sxs-lookup"><span data-stu-id="fc76f-456">Performance counters settings</span></span>
 - <span data-ttu-id="fc76f-457">报告作业特定的路径段</span><span class="sxs-lookup"><span data-stu-id="fc76f-457">Reporting of job specific path segment</span></span>
 - <span data-ttu-id="fc76f-458">支持“列出文件”API 中的子文件夹</span><span class="sxs-lookup"><span data-stu-id="fc76f-458">Support for subfolders in list files api</span></span>
 - <span data-ttu-id="fc76f-459">使用情况和限制报告</span><span class="sxs-lookup"><span data-stu-id="fc76f-459">Usage and limits reporting</span></span>
 - <span data-ttu-id="fc76f-460">允许为 NFS 服务器指定缓存类型</span><span class="sxs-lookup"><span data-stu-id="fc76f-460">Allow to specify caching type for NFS servers</span></span>
 - <span data-ttu-id="fc76f-461">支持自定义映像</span><span class="sxs-lookup"><span data-stu-id="fc76f-461">Support for custom images</span></span>
 - <span data-ttu-id="fc76f-462">添加了 pyTorch 工具包支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-462">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="fc76f-463">添加了 `job wait` 命令，以允许等待作业完成和报告作业退出代码</span><span class="sxs-lookup"><span data-stu-id="fc76f-463">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="fc76f-464">添加了 `usage show` 命令，用于列出不同区域的当前 Batch AI 资源使用情况和限制</span><span class="sxs-lookup"><span data-stu-id="fc76f-464">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="fc76f-465">支持国家云</span><span class="sxs-lookup"><span data-stu-id="fc76f-465">National clouds are supported</span></span>
* <span data-ttu-id="fc76f-466">添加了作业命令行参数，以便除了装载配置文件以外，还能装载作业级别的文件系统</span><span class="sxs-lookup"><span data-stu-id="fc76f-466">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="fc76f-467">添加了更多选项用于自定义群集 - VM 优先级、子网、自动缩放群集的初始节点计数，以及指定自定义映像</span><span class="sxs-lookup"><span data-stu-id="fc76f-467">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="fc76f-468">添加了命令行选项用于指定 Batch AI 托管 NFS 的缓存类型</span><span class="sxs-lookup"><span data-stu-id="fc76f-468">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="fc76f-469">简化了在配置文件中指定装载文件系统的方法。</span><span class="sxs-lookup"><span data-stu-id="fc76f-469">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="fc76f-470">现在，可以省略 Azure 文件共享和 Azure Blob 容器的凭据 - CLI 将会使用通过命令行参数提供的或通过环境变量指定的存储帐户密钥来填充缺少的凭据，或者从 Azure 存储查询密钥（如果存储帐户属于当前订阅）</span><span class="sxs-lookup"><span data-stu-id="fc76f-470">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="fc76f-471">作业完成后（成功、失败、已终止或已删除），作业文件流命令现在会自动完成</span><span class="sxs-lookup"><span data-stu-id="fc76f-471">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="fc76f-472">改进了 `show` 操作的 `table` 输出</span><span class="sxs-lookup"><span data-stu-id="fc76f-472">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="fc76f-473">添加了 `--use-auto-storage` 选项用于创建群集。</span><span class="sxs-lookup"><span data-stu-id="fc76f-473">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="fc76f-474">使用此选项可以更方便地管理存储帐户，以及将 Azure 文件共享和 Azure Blob 容器装载到群集</span><span class="sxs-lookup"><span data-stu-id="fc76f-474">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="fc76f-475">为 `cluster create` 和 `file-server create` 添加了 `--generate-ssh-keys` 选项</span><span class="sxs-lookup"><span data-stu-id="fc76f-475">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="fc76f-476">添加了通过命令行提供节点设置任务的功能</span><span class="sxs-lookup"><span data-stu-id="fc76f-476">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="fc76f-477">[重大更改]移动了 `job file` 组下面的 `job stream-file` 和 `job list-files` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-477">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="fc76f-478">[重大更改]已将 `file-server create` 命令中的 `--admin-user-name` 重命名为 `--user-name`，使其与 `cluster create` 命令一致</span><span class="sxs-lookup"><span data-stu-id="fc76f-478">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="fc76f-479">计费</span><span class="sxs-lookup"><span data-stu-id="fc76f-479">Billing</span></span>

* <span data-ttu-id="fc76f-480">添加了登记帐户命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-480">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="fc76f-481">消耗</span><span class="sxs-lookup"><span data-stu-id="fc76f-481">Consumption</span></span>

* <span data-ttu-id="fc76f-482">添加了 `marketplace` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-482">Added `marketplace` commands</span></span>
* <span data-ttu-id="fc76f-483">[重大更改] 已将 `reservations summaries` 重命名为 `reservation summary`</span><span class="sxs-lookup"><span data-stu-id="fc76f-483">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="fc76f-484">[重大更改] 已将 `reservations details` 重命名为 `reservation detail`</span><span class="sxs-lookup"><span data-stu-id="fc76f-484">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="fc76f-485">[重大更改]删除了 `reservation` 命令的 `--reservation-order-id` 和 `--reservation-id` 短选项</span><span class="sxs-lookup"><span data-stu-id="fc76f-485">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="fc76f-486">[重大更改]删除了 `reservation summary` 命令的 `--grain` 短选项</span><span class="sxs-lookup"><span data-stu-id="fc76f-486">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="fc76f-487">[重大更改]删除了 `pricesheet` 命令的 `--include-meter-details` 短选项</span><span class="sxs-lookup"><span data-stu-id="fc76f-487">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="fc76f-488">容器</span><span class="sxs-lookup"><span data-stu-id="fc76f-488">Container</span></span>

* <span data-ttu-id="fc76f-489">添加了 git 存储库卷装载参数 `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` 和 `--gitrepo-mount-path`</span><span class="sxs-lookup"><span data-stu-id="fc76f-489">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="fc76f-490">修复了 [#5926](https://github.com/Azure/azure-cli/issues/5926)：指定 --container-name 时 `az container exec` 失败</span><span class="sxs-lookup"><span data-stu-id="fc76f-490">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="fc76f-491">分机</span><span class="sxs-lookup"><span data-stu-id="fc76f-491">Extension</span></span>

* <span data-ttu-id="fc76f-492">已将分配检查消息更改为调试级别</span><span class="sxs-lookup"><span data-stu-id="fc76f-492">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="fc76f-493">交互</span><span class="sxs-lookup"><span data-stu-id="fc76f-493">Interactive</span></span>

* <span data-ttu-id="fc76f-494">更改为在命令不可识别时停止完成</span><span class="sxs-lookup"><span data-stu-id="fc76f-494">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="fc76f-495">添加了创建命令子树之前和之后所用的事件挂钩</span><span class="sxs-lookup"><span data-stu-id="fc76f-495">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="fc76f-496">添加了 `--ids` 参数补全</span><span class="sxs-lookup"><span data-stu-id="fc76f-496">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-497">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-497">Network</span></span>

* <span data-ttu-id="fc76f-498">修复了 [#5936](https://github.com/Azure/azure-cli/issues/5936)：无法设置 `application-gateway create` 标记</span><span class="sxs-lookup"><span data-stu-id="fc76f-498">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="fc76f-499">添加了参数 `--auth-certs`，以附加 `application-gateway http-settings [create|update]` 的身份验证证书。</span><span class="sxs-lookup"><span data-stu-id="fc76f-499">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="fc76f-500">#4910</span><span class="sxs-lookup"><span data-stu-id="fc76f-500">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="fc76f-501">添加了 `ddos-protection` 命令用于创建 DDoS 保护计划</span><span class="sxs-lookup"><span data-stu-id="fc76f-501">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="fc76f-502">为 `vnet [create|update]` 添加了 `--ddos-protection-plan` 支持，以便将 VNet 关联到 DDoS 保护计划</span><span class="sxs-lookup"><span data-stu-id="fc76f-502">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="fc76f-503">修复了 `network route-table [create|update]` 中 `--disable-bgp-route-propagation` 标志的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-503">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="fc76f-504">删除了 `network lb [create|update]` 的虚拟参数 `--public-ip-address-type` 和 `--subnet-type`</span><span class="sxs-lookup"><span data-stu-id="fc76f-504">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="fc76f-505">为 `network dns zone [import|export]` 和 `network dns record-set txt add-record` 添加了采用 RFC 1035 转义序列的 TXT 记录支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-505">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="fc76f-506">配置文件</span><span class="sxs-lookup"><span data-stu-id="fc76f-506">Profile</span></span>

* <span data-ttu-id="fc76f-507">在 `account list` 中添加了 Azure 经典帐户支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-507">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="fc76f-508">[重大更改]删除了 `--msi` & `--msi-port` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-508">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="fc76f-509">RDBMS</span><span class="sxs-lookup"><span data-stu-id="fc76f-509">RDBMS</span></span>

* <span data-ttu-id="fc76f-510">添加了 `georestore` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-510">Added `georestore` command</span></span>
* <span data-ttu-id="fc76f-511">删除了 `create` 命令的存储大小限制</span><span class="sxs-lookup"><span data-stu-id="fc76f-511">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="fc76f-512">资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-512">Resource</span></span>

* <span data-ttu-id="fc76f-513">在 `policy definition create` 中添加了对 `--metadata` 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-513">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="fc76f-514">为 `policy definition update` 添加了对 `--metadata`、`--set`、`--add` 和 `--remove` 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-514">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="fc76f-515">SQL</span><span class="sxs-lookup"><span data-stu-id="fc76f-515">SQL</span></span>

* <span data-ttu-id="fc76f-516">添加了 `sql elastic-pool op list` 和 `sql elastic-pool op cancel`</span><span class="sxs-lookup"><span data-stu-id="fc76f-516">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-517">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-517">Storage</span></span>

* <span data-ttu-id="fc76f-518">改进了有关连接字符串格式不当的错误消息</span><span class="sxs-lookup"><span data-stu-id="fc76f-518">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-519">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-519">VM</span></span>

* <span data-ttu-id="fc76f-520">为 `vmss create` 添加了配置平台容错域计数的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-520">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="fc76f-521">已将 `vmss create` 的默认值更改为区域性、大型或禁用单一位置组的规模集的标准负载均衡器</span><span class="sxs-lookup"><span data-stu-id="fc76f-521">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [重大更改]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="fc76f-523">为 `vm create` 添加了对公共 IP SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-523">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="fc76f-524">为 `vm secret format` 添加了 `--keyvault` 和 `--resource-group` 参数，以便在命令无法解析保管库 ID 的情况下提供支持。</span><span class="sxs-lookup"><span data-stu-id="fc76f-524">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="fc76f-525">#5718</span><span class="sxs-lookup"><span data-stu-id="fc76f-525">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="fc76f-526">改进了当资源组的位置不支持区域时，`[vm|vmss create]` 发生的错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-526">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="fc76f-527">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-527">March 27, 2018</span></span>

<span data-ttu-id="fc76f-528">版本 2.0.30</span><span class="sxs-lookup"><span data-stu-id="fc76f-528">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="fc76f-529">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-529">Core</span></span>

* <span data-ttu-id="fc76f-530">为帮助中标记为预览版的扩展显示消息</span><span class="sxs-lookup"><span data-stu-id="fc76f-530">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-531">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-531">ACS</span></span>

* <span data-ttu-id="fc76f-532">为 Cloud Shell 中的 `aks install-cli` 修复 SSL 证书验证错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-532">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-533">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-533">Appservice</span></span>

* <span data-ttu-id="fc76f-534">为 `webapp update` 添加了仅限 HTTPS 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-534">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="fc76f-535">为 `az webapp identity [assign|show]` 和 `az functionapp identity [assign|show]` 添加了对插槽的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-535">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="fc76f-536">备份</span><span class="sxs-lookup"><span data-stu-id="fc76f-536">Backup</span></span>

* <span data-ttu-id="fc76f-537">添加了新命令 `az backup protection isenabled-for-vm`。</span><span class="sxs-lookup"><span data-stu-id="fc76f-537">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="fc76f-538">此命令可用于检查 VM 是否已由订阅中的任何保管库备份</span><span class="sxs-lookup"><span data-stu-id="fc76f-538">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="fc76f-539">为下列命令的 `--resource-group` 和 `--vault-name` 参数启用了 Azure 对象 ID：</span><span class="sxs-lookup"><span data-stu-id="fc76f-539">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="fc76f-540">更改了 `--name` 参数以接受 `backup ... show` 命令的输出格式</span><span class="sxs-lookup"><span data-stu-id="fc76f-540">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="fc76f-541">容器</span><span class="sxs-lookup"><span data-stu-id="fc76f-541">Container</span></span>

* <span data-ttu-id="fc76f-542">添加了 `container exec` 命令。</span><span class="sxs-lookup"><span data-stu-id="fc76f-542">Added `container exec` command.</span></span> <span data-ttu-id="fc76f-543">在正在运行的容器组的容器中执行命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-543">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="fc76f-544">允许将表输出用于创建和更新容器组</span><span class="sxs-lookup"><span data-stu-id="fc76f-544">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="fc76f-545">分机</span><span class="sxs-lookup"><span data-stu-id="fc76f-545">Extension</span></span>

* <span data-ttu-id="fc76f-546">为 `extension add` 添加了消息（如果扩展处于预览状态）</span><span class="sxs-lookup"><span data-stu-id="fc76f-546">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="fc76f-547">更改了 `extension list-available` 以通过 `--show-details` 显示完整扩展数据</span><span class="sxs-lookup"><span data-stu-id="fc76f-547">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="fc76f-548">[重大更改] 更改了 `extension list-available` 以在默认情况下显示简化的扩展数据</span><span class="sxs-lookup"><span data-stu-id="fc76f-548">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="fc76f-549">交互</span><span class="sxs-lookup"><span data-stu-id="fc76f-549">Interactive</span></span>

* <span data-ttu-id="fc76f-550">已将“完成”更改为在执行命令表加载后立即激活</span><span class="sxs-lookup"><span data-stu-id="fc76f-550">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="fc76f-551">修复了使用 `--style` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-551">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="fc76f-552">交互式词法分析器在命令表转储后实例化（如果缺失）</span><span class="sxs-lookup"><span data-stu-id="fc76f-552">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="fc76f-553">改进了完成符支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-553">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="fc76f-554">实验室</span><span class="sxs-lookup"><span data-stu-id="fc76f-554">Lab</span></span>

* <span data-ttu-id="fc76f-555">修复了 `create environment` 命令的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-555">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="fc76f-556">监视</span><span class="sxs-lookup"><span data-stu-id="fc76f-556">Monitor</span></span>

* <span data-ttu-id="fc76f-557">为 `metrics list` 添加了对 `--top`、`--orderby` 和 `--namespace` 的支持 [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="fc76f-557">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="fc76f-558">修复了 [#4529](https://github.com/Azure/azure-cli/issues/5785)：`metrics list`接受要检索的指标的空格分隔列表</span><span class="sxs-lookup"><span data-stu-id="fc76f-558">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="fc76f-559">为 `metrics list-definitions` 添加了对 `--namespace` 的支持 [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="fc76f-559">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-560">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-560">Network</span></span>

* <span data-ttu-id="fc76f-561">添加了对专用 DNS 区域的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-561">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="fc76f-562">配置文件</span><span class="sxs-lookup"><span data-stu-id="fc76f-562">Profile</span></span>

* <span data-ttu-id="fc76f-563">为 `login` 添加了针对 `--identity-port` 和 `--msi-port` 的警告</span><span class="sxs-lookup"><span data-stu-id="fc76f-563">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="fc76f-564">RDBMS</span><span class="sxs-lookup"><span data-stu-id="fc76f-564">RDBMS</span></span>

* <span data-ttu-id="fc76f-565">添加了业务模型 GA API 版本 2017-12-01</span><span class="sxs-lookup"><span data-stu-id="fc76f-565">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="fc76f-566">资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-566">Resource</span></span>

* [重大更改]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="fc76f-568">角色</span><span class="sxs-lookup"><span data-stu-id="fc76f-568">Role</span></span>

* <span data-ttu-id="fc76f-569">为 `az ad app create` 添加了对所需访问权限配置和本机客户端的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-569">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="fc76f-570">更改了 `rbac` 命令以在对象解析时返回少于 1000 个的 ID</span><span class="sxs-lookup"><span data-stu-id="fc76f-570">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="fc76f-571">添加了凭据管理命令 `ad sp credential [reset|list|delete]`</span><span class="sxs-lookup"><span data-stu-id="fc76f-571">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="fc76f-572">[重大更改] 从 `az role assignment [list|show]` 输出中删除了“properties”</span><span class="sxs-lookup"><span data-stu-id="fc76f-572">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="fc76f-573">为 `role definition` 添加了对 `dataActions` 和 `notDataActions` 权限的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-573">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-574">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-574">Storage</span></span>

* <span data-ttu-id="fc76f-575">修复了在上传大小介于 195GB 和 200GB 之间的文件时存在的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-575">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="fc76f-576">修复了 [#4049](https://github.com/Azure/azure-cli/issues/4049)：上传 append 类型的 Blob 时忽略条件参数的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-576">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-577">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-577">VM</span></span>

* <span data-ttu-id="fc76f-578">针对即将到来的、适用于包含 100 个以上实例的集合的重大更改，为 `vmss create` 添加了警告</span><span class="sxs-lookup"><span data-stu-id="fc76f-578">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="fc76f-579">为 `vm [snapshot|image]` 添加了区域弹性支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-579">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="fc76f-580">更改了磁盘实例视图以更好地报告加密状态</span><span class="sxs-lookup"><span data-stu-id="fc76f-580">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="fc76f-581">[重大更改] 更改了 `vm extension delete` 以不再返回输出</span><span class="sxs-lookup"><span data-stu-id="fc76f-581">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="fc76f-582">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-582">March 13, 2018</span></span>

<span data-ttu-id="fc76f-583">版本 2.0.29</span><span class="sxs-lookup"><span data-stu-id="fc76f-583">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="fc76f-584">ACR</span><span class="sxs-lookup"><span data-stu-id="fc76f-584">ACR</span></span>

* <span data-ttu-id="fc76f-585">为 `repository delete` 添加了对 `--image` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-585">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="fc76f-586">弃用了 `repository delete` 命令的 `--manifest` 和 `--tag` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-586">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="fc76f-587">添加了 `repository untag` 命令以在不删除数据的情况下删除标记</span><span class="sxs-lookup"><span data-stu-id="fc76f-587">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-588">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-588">ACS</span></span>

* <span data-ttu-id="fc76f-589">添加了 `aks upgrade-connector` 命令以升级现有连接器</span><span class="sxs-lookup"><span data-stu-id="fc76f-589">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="fc76f-590">更改了 `kubectl` 配置文件以使用更具可读性的块样式 YAML</span><span class="sxs-lookup"><span data-stu-id="fc76f-590">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="fc76f-591">顾问</span><span class="sxs-lookup"><span data-stu-id="fc76f-591">Advisor</span></span>

* <span data-ttu-id="fc76f-592">[重大更改] 已将 `advisor configuration get` 重命名为 `advisor configuration list`</span><span class="sxs-lookup"><span data-stu-id="fc76f-592">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="fc76f-593">[重大更改] 已将 `advisor configuration set` 重命名为 `advisor configuration update`</span><span class="sxs-lookup"><span data-stu-id="fc76f-593">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="fc76f-594">[重大更改] 删除了 `advisor recommendation generate`</span><span class="sxs-lookup"><span data-stu-id="fc76f-594">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="fc76f-595">为 `advisor recommendation list` 添加了 `--refresh` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-595">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="fc76f-596">添加了 `advisor recommendation show` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-596">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-597">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-597">Appservice</span></span>

* <span data-ttu-id="fc76f-598">弃用了 `[webapp|functionapp] assign-identity`</span><span class="sxs-lookup"><span data-stu-id="fc76f-598">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="fc76f-599">添加了托管标识命令 `webapp identity [assign|show]` 和 `functionapp identity [assign|show]`</span><span class="sxs-lookup"><span data-stu-id="fc76f-599">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="fc76f-600">Eventhubs</span><span class="sxs-lookup"><span data-stu-id="fc76f-600">Eventhubs</span></span>

* <span data-ttu-id="fc76f-601">初始版本</span><span class="sxs-lookup"><span data-stu-id="fc76f-601">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="fc76f-602">分机</span><span class="sxs-lookup"><span data-stu-id="fc76f-602">Extension</span></span>

* <span data-ttu-id="fc76f-603">添加了检查，以在使用的发行版不是程序包源文件中存储的发行版时提醒用户，因为这可能导致错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-603">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="fc76f-604">交互</span><span class="sxs-lookup"><span data-stu-id="fc76f-604">Interactive</span></span>

* <span data-ttu-id="fc76f-605">修复了 [#5625](https://github.com/Azure/azure-cli/issues/5625)：在不同会话之间永久保留历史记录</span><span class="sxs-lookup"><span data-stu-id="fc76f-605">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="fc76f-606">修复了 [#3016](https://github.com/Azure/azure-cli/issues/3016)：在作用域中时不记录历史记录</span><span class="sxs-lookup"><span data-stu-id="fc76f-606">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="fc76f-607">修复了 [#5688](https://github.com/Azure/azure-cli/issues/5688)：如果命令表加载遇到了异常，不显示“完成”</span><span class="sxs-lookup"><span data-stu-id="fc76f-607">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="fc76f-608">修复了用于长时间运行的操作的进度指示器</span><span class="sxs-lookup"><span data-stu-id="fc76f-608">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="fc76f-609">监视</span><span class="sxs-lookup"><span data-stu-id="fc76f-609">Monitor</span></span>

* <span data-ttu-id="fc76f-610">弃用了 `monitor autoscale-settings` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-610">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="fc76f-611">添加了 `monitor autoscale` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-611">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="fc76f-612">添加了 `monitor autoscale profile` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-612">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="fc76f-613">添加了 `monitor autoscale rule` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-613">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-614">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-614">Network</span></span>

* <span data-ttu-id="fc76f-615">[重大更改] 从 `route-filter rule create` 中删除了 `--tags` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-615">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="fc76f-616">删除了以下命令的某些错误默认值：</span><span class="sxs-lookup"><span data-stu-id="fc76f-616">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="fc76f-617">添加了 `network watcher connection-monitor` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-617">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="fc76f-618">为 `network watcher show-topology` 添加了 `--vnet` 和 `--subnet`</span><span class="sxs-lookup"><span data-stu-id="fc76f-618">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="fc76f-619">配置文件</span><span class="sxs-lookup"><span data-stu-id="fc76f-619">Profile</span></span>

* <span data-ttu-id="fc76f-620">弃用了 `az login` 的 `--msi` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-620">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="fc76f-621">为 `az login` 添加了 `--identity` 参数以替换 `--msi`</span><span class="sxs-lookup"><span data-stu-id="fc76f-621">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="fc76f-622">RDBMS</span><span class="sxs-lookup"><span data-stu-id="fc76f-622">RDBMS</span></span>

* <span data-ttu-id="fc76f-623">[预览] 已更改为使用 API 2017-12-01-preview</span><span class="sxs-lookup"><span data-stu-id="fc76f-623">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="fc76f-624">服务总线</span><span class="sxs-lookup"><span data-stu-id="fc76f-624">Service Bus</span></span>

* <span data-ttu-id="fc76f-625">初始版本</span><span class="sxs-lookup"><span data-stu-id="fc76f-625">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-626">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-626">Storage</span></span>

* <span data-ttu-id="fc76f-627">修复了 [#4971](https://github.com/Azure/azure-cli/issues/4971)：`storage blob copy` 现在支持其他 Azure 云</span><span class="sxs-lookup"><span data-stu-id="fc76f-627">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="fc76f-628">修复了 [#5286](https://github.com/Azure/azure-cli/issues/5286)：Batch 命令 `storage blob [delete-batch|download-batch|upload-batch]` 不再在前置条件失败时引发错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-628">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-629">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-629">VM</span></span>

* <span data-ttu-id="fc76f-630">为 `[vm|vmss] create` 添加了支持，以附加非托管数据磁盘和配置缓存</span><span class="sxs-lookup"><span data-stu-id="fc76f-630">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="fc76f-631">弃用了 `[vm|vmss] assign-identity` 和 `[vm|vmss] remove-identity`</span><span class="sxs-lookup"><span data-stu-id="fc76f-631">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="fc76f-632">添加了 `vm identity [assign|remove|show]` 和 `vmss identity [assign|remove|show]` 以替换弃用的命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-632">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="fc76f-633">已将 `vmss create` 中的默认优先级更改为 None</span><span class="sxs-lookup"><span data-stu-id="fc76f-633">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="fc76f-634">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-634">February 27, 2018</span></span>

<span data-ttu-id="fc76f-635">版本 2.0.28</span><span class="sxs-lookup"><span data-stu-id="fc76f-635">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="fc76f-636">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-636">Core</span></span>

* <span data-ttu-id="fc76f-637">已修复 [#5184](https://github.com/Azure/azure-cli/issues/5184)：Homebrew 安装问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-637">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="fc76f-638">添加了对具有自定义密钥的扩展遥测的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-638">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="fc76f-639">为 `--debug` 添加了 HTTP 日志记录</span><span class="sxs-lookup"><span data-stu-id="fc76f-639">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-640">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-640">ACS</span></span>

* <span data-ttu-id="fc76f-641">已更改为默认情况下对 `aks install-connector` 使用 `virtual-kubelet-for-aks` Helm 图</span><span class="sxs-lookup"><span data-stu-id="fc76f-641">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="fc76f-642">已修复问题：服务主体没有足够的权限来创建 ACI 容器组的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-642">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="fc76f-643">已为 `aks install-connector` 添加了 `--aci-container-group`、`--location` 和 `--image-tag`</span><span class="sxs-lookup"><span data-stu-id="fc76f-643">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="fc76f-644">从 `aks get-versions` 中删除了弃用通知</span><span class="sxs-lookup"><span data-stu-id="fc76f-644">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-645">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-645">Appservice</span></span>

* <span data-ttu-id="fc76f-646">针对新 SDK 版本 (azure-mgmt-web 0.35.0) 的更新</span><span class="sxs-lookup"><span data-stu-id="fc76f-646">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="fc76f-647">已修复 [#5538](https://github.com/Azure/azure-cli/issues/5538)：`Free` 被报告为无效 SKU</span><span class="sxs-lookup"><span data-stu-id="fc76f-647">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="fc76f-648">认知服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-648">Cognitive Services</span></span>

* <span data-ttu-id="fc76f-649">更新了创建新的认知服务帐户时的“通知”</span><span class="sxs-lookup"><span data-stu-id="fc76f-649">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="fc76f-650">消耗</span><span class="sxs-lookup"><span data-stu-id="fc76f-650">Consumption</span></span>

* <span data-ttu-id="fc76f-651">为 pricesheet API 添加了新命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-651">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="fc76f-652">更新了现有“使用情况详细信息”和“预订详细信息”格式</span><span class="sxs-lookup"><span data-stu-id="fc76f-652">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="fc76f-653">容器</span><span class="sxs-lookup"><span data-stu-id="fc76f-653">Container</span></span>

* <span data-ttu-id="fc76f-654">为 `container create` 添加了 `--secrets` 和 `--secrets-mount-path` 参数以在 ACI 中使用机密</span><span class="sxs-lookup"><span data-stu-id="fc76f-654">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-655">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-655">Network</span></span>

* <span data-ttu-id="fc76f-656">修复了 [#5559](https://github.com/Azure/azure-cli/issues/5559)：`network vnet-gateway vpn-client generate` 中缺少客户端</span><span class="sxs-lookup"><span data-stu-id="fc76f-656">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="fc76f-657">资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-657">Resource</span></span>

* <span data-ttu-id="fc76f-658">更改了 `group deployment export` 以在失败时显示部分模板和错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-658">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="fc76f-659">角色</span><span class="sxs-lookup"><span data-stu-id="fc76f-659">Role</span></span>

* <span data-ttu-id="fc76f-660">添加了 `role assignment list-changelogs` 以允许审核服务主体角色</span><span class="sxs-lookup"><span data-stu-id="fc76f-660">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="fc76f-661">SQL</span><span class="sxs-lookup"><span data-stu-id="fc76f-661">SQL</span></span>

* <span data-ttu-id="fc76f-662">添加了在创建和更新时对数据库和弹性池的区域冗余支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-662">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-663">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-663">Storage</span></span>

* <span data-ttu-id="fc76f-664">已允许为 `storage blob [upload-batch|download-batch]` 指定 destination-path/prefix</span><span class="sxs-lookup"><span data-stu-id="fc76f-664">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-665">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-665">VM</span></span>

* <span data-ttu-id="fc76f-666">添加了对在单个 VMSS 实例上附加/分离磁盘的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-666">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="fc76f-667">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-667">February 13, 2018</span></span>

<span data-ttu-id="fc76f-668">版本 2.0.27</span><span class="sxs-lookup"><span data-stu-id="fc76f-668">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="fc76f-669">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-669">Core</span></span>

* <span data-ttu-id="fc76f-670">更改了同时根据订阅 ID 和在 MSI 登录名对密钥进行身份验证</span><span class="sxs-lookup"><span data-stu-id="fc76f-670">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-671">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-671">ACS</span></span>

* <span data-ttu-id="fc76f-672">[重大更改] 为了提高准确性，已将 `aks get-versions` 重命名为 `aks get-upgrades`</span><span class="sxs-lookup"><span data-stu-id="fc76f-672">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="fc76f-673">更改了 `aks get-versions` 以显示可用于 `aks create` 的 Kubernetes 版本</span><span class="sxs-lookup"><span data-stu-id="fc76f-673">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="fc76f-674">更改了 `aks create` 默认值以允许服务器选择 Kubernetes 版本</span><span class="sxs-lookup"><span data-stu-id="fc76f-674">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="fc76f-675">更新了引用由 AKS 生成的服务主体的帮助消息</span><span class="sxs-lookup"><span data-stu-id="fc76f-675">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="fc76f-676">更改了 `aks create` 的默认节点大小，从“Standard\_D1\_v2”更改为“Standard\_DS1\_v2”</span><span class="sxs-lookup"><span data-stu-id="fc76f-676">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="fc76f-677">改进了定位 `az aks browse` 的仪表板 pod 时的可靠性</span><span class="sxs-lookup"><span data-stu-id="fc76f-677">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="fc76f-678">修复了 `aks get-credentials` 以便在加载 Kubernetes 配置文件时处理 Unicode 错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-678">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="fc76f-679">向 `az aks install-cli` 添加了一条消息，以便帮助在 `$PATH` 中获取 `kubectl`</span><span class="sxs-lookup"><span data-stu-id="fc76f-679">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-680">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-680">Appservice</span></span>

* <span data-ttu-id="fc76f-681">修复了由于空引用 `webapp [backup|restore]` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-681">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="fc76f-682">通过 `az configure --defaults appserviceplan=my-asp` 添加了对默认应用服务计划的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-682">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="fc76f-683">CDN</span><span class="sxs-lookup"><span data-stu-id="fc76f-683">CDN</span></span>

* <span data-ttu-id="fc76f-684">添加了 `cdn custom-domain [enable-https|disable-https]` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-684">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="fc76f-685">容器</span><span class="sxs-lookup"><span data-stu-id="fc76f-685">Container</span></span>

* <span data-ttu-id="fc76f-686">向 `az container logs` 添加了 `--follow` 选项，用于流式传输日志</span><span class="sxs-lookup"><span data-stu-id="fc76f-686">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="fc76f-687">添加了 `container attach` 命令，用于将本地标准输出和错误流附加到容器组中的容器</span><span class="sxs-lookup"><span data-stu-id="fc76f-687">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="fc76f-688">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="fc76f-688">CosmosDB</span></span>

* <span data-ttu-id="fc76f-689">添加了对设置功能的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-689">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="fc76f-690">分机</span><span class="sxs-lookup"><span data-stu-id="fc76f-690">Extension</span></span>

* <span data-ttu-id="fc76f-691">向 `az extension [add|update]` 命令添加了对 `--pip-proxy` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-691">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="fc76f-692">向 `az extension [add|update]` 命令添加了对 `--pip-extra-index-urls` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-692">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="fc76f-693">反馈</span><span class="sxs-lookup"><span data-stu-id="fc76f-693">Feedback</span></span>

* <span data-ttu-id="fc76f-694">将扩展信息添加到了遥测数据</span><span class="sxs-lookup"><span data-stu-id="fc76f-694">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="fc76f-695">交互</span><span class="sxs-lookup"><span data-stu-id="fc76f-695">Interactive</span></span>

* <span data-ttu-id="fc76f-696">修复了在 Cloud Shell 中使用交互模式时提示用户登录的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-696">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="fc76f-697">修复了缺少参数补全时的回归问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-697">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="fc76f-698">IoT</span><span class="sxs-lookup"><span data-stu-id="fc76f-698">IoT</span></span>

* <span data-ttu-id="fc76f-699">修复了 `iot dps access policy [create|update]` 在成功时返回“not found”错误的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-699">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="fc76f-700">修复了 `iot dps linked-hub [create|update]` 在成功时返回“not found”错误的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-700">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="fc76f-701">向 `iot dps access policy [create|update]` 和 `iot dps linked-hub [create|update]` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-701">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="fc76f-702">更改了 `iot hub create` 以允许指定分区数</span><span class="sxs-lookup"><span data-stu-id="fc76f-702">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="fc76f-703">监视</span><span class="sxs-lookup"><span data-stu-id="fc76f-703">Monitor</span></span>

* <span data-ttu-id="fc76f-704">修复了 `az monitor log-profiles create` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-704">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-705">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-705">Network</span></span>

* <span data-ttu-id="fc76f-706">修复了以下命令的 `--tags` 选项：</span><span class="sxs-lookup"><span data-stu-id="fc76f-706">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="fc76f-707">配置文件</span><span class="sxs-lookup"><span data-stu-id="fc76f-707">Profile</span></span>

* <span data-ttu-id="fc76f-708">在交互模式中启用了 `az login`</span><span class="sxs-lookup"><span data-stu-id="fc76f-708">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="fc76f-709">资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-709">Resource</span></span>

* <span data-ttu-id="fc76f-710">重新添加了 `feature show`</span><span class="sxs-lookup"><span data-stu-id="fc76f-710">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="fc76f-711">角色</span><span class="sxs-lookup"><span data-stu-id="fc76f-711">Role</span></span>

* <span data-ttu-id="fc76f-712">为 `ad app update` 添加了 `--available-to-other-tenants` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-712">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="fc76f-713">SQL</span><span class="sxs-lookup"><span data-stu-id="fc76f-713">SQL</span></span>

* <span data-ttu-id="fc76f-714">添加了 `sql server dns-alias` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-714">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="fc76f-715">添加了 `sql db rename`</span><span class="sxs-lookup"><span data-stu-id="fc76f-715">Added `sql db rename`</span></span>
* <span data-ttu-id="fc76f-716">向所有 sql 命令添加了对 `--ids` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-716">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-717">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-717">Storage</span></span>

* <span data-ttu-id="fc76f-718">添加了 `storage blob service-properties delete-policy` 和 `storage blob undelete` 命令以启用软删除</span><span class="sxs-lookup"><span data-stu-id="fc76f-718">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-719">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-719">VM</span></span>

* <span data-ttu-id="fc76f-720">修复了无法完全初始化 VM 加密时出现的崩溃</span><span class="sxs-lookup"><span data-stu-id="fc76f-720">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="fc76f-721">添加了启用 MSI 时的主体 ID 输出</span><span class="sxs-lookup"><span data-stu-id="fc76f-721">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="fc76f-722">固定 `vm boot-diagnostics get-boot-log`</span><span class="sxs-lookup"><span data-stu-id="fc76f-722">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="fc76f-723">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-723">January 31, 2018</span></span>

<span data-ttu-id="fc76f-724">版本 2.0.26</span><span class="sxs-lookup"><span data-stu-id="fc76f-724">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="fc76f-725">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-725">Core</span></span>

* <span data-ttu-id="fc76f-726">添加了支持在 MSI 上下文中检索原始令牌</span><span class="sxs-lookup"><span data-stu-id="fc76f-726">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="fc76f-727">删除了完成对 Windows cmd.exe 进行 LRO 操作后轮询指示器字符串</span><span class="sxs-lookup"><span data-stu-id="fc76f-727">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="fc76f-728">添加了将使用配置的默认值时显示的警告更改为信息级别条目。</span><span class="sxs-lookup"><span data-stu-id="fc76f-728">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="fc76f-729">请使用 `--verbose` 查看</span><span class="sxs-lookup"><span data-stu-id="fc76f-729">Use `--verbose` to see</span></span>
* <span data-ttu-id="fc76f-730">为等待命令添加了进度指示器</span><span class="sxs-lookup"><span data-stu-id="fc76f-730">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-731">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-731">ACS</span></span>

* <span data-ttu-id="fc76f-732">说明了 `--disable-browser` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-732">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="fc76f-733">改进了 `--vm-size` 参数的 tab 键补全功能</span><span class="sxs-lookup"><span data-stu-id="fc76f-733">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-734">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-734">Appservice</span></span>

* <span data-ttu-id="fc76f-735">固定 `webapp log [tail|download]`</span><span class="sxs-lookup"><span data-stu-id="fc76f-735">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="fc76f-736">删除了对 Web 应用和函数的 `kind` 检查</span><span class="sxs-lookup"><span data-stu-id="fc76f-736">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="fc76f-737">CDN</span><span class="sxs-lookup"><span data-stu-id="fc76f-737">CDN</span></span>

* <span data-ttu-id="fc76f-738">修复了运行 `cdn custom-domain create` 时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-738">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="fc76f-739">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="fc76f-739">CosmosDB</span></span>

* <span data-ttu-id="fc76f-740">修复了故障转移策略的参数说明</span><span class="sxs-lookup"><span data-stu-id="fc76f-740">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="fc76f-741">交互</span><span class="sxs-lookup"><span data-stu-id="fc76f-741">Interactive</span></span>

* <span data-ttu-id="fc76f-742">修复了不再显示命令选项补全的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-742">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-743">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-743">Network</span></span>

* <span data-ttu-id="fc76f-744">向 `application-gateway create` 添加了对 `--cert-password` 的保护</span><span class="sxs-lookup"><span data-stu-id="fc76f-744">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="fc76f-745">修复了 `application-gateway update` 出现的 `--sku` 错误应用默认值的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-745">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="fc76f-746">向 `vpn-connection create` 添加了对 `--shared-key` 和 `--authorization-key` 的保护</span><span class="sxs-lookup"><span data-stu-id="fc76f-746">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="fc76f-747">修复了运行 `asg create` 时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-747">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="fc76f-748">向 `dns zone export` 添加了用于导出名称的 `--file-name / -f` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-748">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="fc76f-749">修复了 `dns zone export` 存在的以下问题：</span><span class="sxs-lookup"><span data-stu-id="fc76f-749">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="fc76f-750">修复了未正确导出长 TXT 记录的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-750">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="fc76f-751">修复了不使用转义引号无法正确导出带引号的 TXT 记录的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-751">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="fc76f-752">修复了使用 `dns zone import` 某些记录会导入两次的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-752">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="fc76f-753">已还原 `vnet-gateway root-cert` 和 `vnet-gateway revoked-cert` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-753">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="fc76f-754">配置文件</span><span class="sxs-lookup"><span data-stu-id="fc76f-754">Profile</span></span>

* <span data-ttu-id="fc76f-755">修复了 `get-access-token`，使其在 VM 中使用标识正常工作</span><span class="sxs-lookup"><span data-stu-id="fc76f-755">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="fc76f-756">资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-756">Resource</span></span>

* <span data-ttu-id="fc76f-757">修复了 `deployment [create|validate]` 存在的 bug，即当模板的 type 字段包含大写值时错误地显示警告</span><span class="sxs-lookup"><span data-stu-id="fc76f-757">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-758">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-758">Storage</span></span>

* <span data-ttu-id="fc76f-759">修复了将存储 V1 帐户迁移到存储 V2 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-759">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="fc76f-760">为所有上传/下载命令添加了进度报告</span><span class="sxs-lookup"><span data-stu-id="fc76f-760">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="fc76f-761">修复了 `storage account check-name` 不显示“-n”参数选项的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-761">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="fc76f-762">向 `blob [list|show]` 的表输出添加了“snapshot”列</span><span class="sxs-lookup"><span data-stu-id="fc76f-762">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="fc76f-763">修复了需要作为整数分析的各种参数的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-763">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-764">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-764">VM</span></span>

* <span data-ttu-id="fc76f-765">添加了 `vm image accept-terms` 命令，以允许使用额外费用从映像创建 VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-765">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="fc76f-766">修复了 `[vm|vmss create]`，以确保可以在使用未签名证书的代理下运行命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-766">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="fc76f-767">[预览] 向 VMSS 添加了对“低”优先级的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-767">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="fc76f-768">向 `[vm|vmss] create` 添加了对 `--admin-password` 的保护</span><span class="sxs-lookup"><span data-stu-id="fc76f-768">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="fc76f-769">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-769">January 17, 2018</span></span>

<span data-ttu-id="fc76f-770">版本 2.0.25</span><span class="sxs-lookup"><span data-stu-id="fc76f-770">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="fc76f-771">ACR</span><span class="sxs-lookup"><span data-stu-id="fc76f-771">ACR</span></span>

* <span data-ttu-id="fc76f-772">添加了发生 Windows 凭据错误时执行 acr 登录回退的功能</span><span class="sxs-lookup"><span data-stu-id="fc76f-772">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="fc76f-773">启用了注册表日志</span><span class="sxs-lookup"><span data-stu-id="fc76f-773">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-774">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-774">ACS</span></span>

* <span data-ttu-id="fc76f-775">修复了 `get-credentials` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-775">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="fc76f-776">删除了 SPN 角色要求</span><span class="sxs-lookup"><span data-stu-id="fc76f-776">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-777">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-777">Appservice</span></span>

* <span data-ttu-id="fc76f-778">修复了 `hosting_environment_profile` 为 null 时 `config ssl upload` 存在的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-778">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="fc76f-779">为 `browse` 添加了自定义 URL 支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-779">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="fc76f-780">修复了 `log tail` 的槽位支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-780">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="fc76f-781">备份</span><span class="sxs-lookup"><span data-stu-id="fc76f-781">Backup</span></span>

* <span data-ttu-id="fc76f-782">将 `backup item list` 的 `--container-name` 选项更改为可选</span><span class="sxs-lookup"><span data-stu-id="fc76f-782">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="fc76f-783">为 `backup restore restore-disks` 添加了存储帐户选项</span><span class="sxs-lookup"><span data-stu-id="fc76f-783">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="fc76f-784">修复了 `backup protection enable-for-vm` 中的位置检查，使之区分大小写</span><span class="sxs-lookup"><span data-stu-id="fc76f-784">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="fc76f-785">修复了容器名称无效时命令失败的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-785">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="fc76f-786">已将 `backup item list` 更改为默认包含“Health Status”</span><span class="sxs-lookup"><span data-stu-id="fc76f-786">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="fc76f-787">Batch</span><span class="sxs-lookup"><span data-stu-id="fc76f-787">Batch</span></span>

* <span data-ttu-id="fc76f-788">已将 `batch login` 更改为返回身份验证详细信息</span><span class="sxs-lookup"><span data-stu-id="fc76f-788">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="fc76f-789">云</span><span class="sxs-lookup"><span data-stu-id="fc76f-789">Cloud</span></span>

* <span data-ttu-id="fc76f-790">已更改为在云中设置 `--profile` 时不需要终结点</span><span class="sxs-lookup"><span data-stu-id="fc76f-790">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="fc76f-791">消耗</span><span class="sxs-lookup"><span data-stu-id="fc76f-791">Consumption</span></span>

* <span data-ttu-id="fc76f-792">添加了用于预留的新命令：`consumption reservations summaries` 和 `consumption reservations details`</span><span class="sxs-lookup"><span data-stu-id="fc76f-792">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="fc76f-793">事件网格</span><span class="sxs-lookup"><span data-stu-id="fc76f-793">Event Grid</span></span>

* <span data-ttu-id="fc76f-794">[重大更改] 已将 `az eventgrid topic event-subscription` 命令变动为 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="fc76f-794">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="fc76f-795">[重大更改] 已将 `az eventgrid resource event-subscription` 命令变动为 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="fc76f-795">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="fc76f-796">[重大更改] 已删除 `eventgrid event-subscription show-endpoint-url` 命令。</span><span class="sxs-lookup"><span data-stu-id="fc76f-796">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="fc76f-797">请改用 `eventgrid event-subscription show --include-full-endpoint-url`</span><span class="sxs-lookup"><span data-stu-id="fc76f-797">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="fc76f-798">添加了命令 `eventgrid topic update`</span><span class="sxs-lookup"><span data-stu-id="fc76f-798">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="fc76f-799">添加了命令 `eventgrid event-subscription update`</span><span class="sxs-lookup"><span data-stu-id="fc76f-799">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="fc76f-800">为 `eventgrid topic` 命令添加了 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-800">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="fc76f-801">添加了主题名称的 Tab 键补全支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-801">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="fc76f-802">交互</span><span class="sxs-lookup"><span data-stu-id="fc76f-802">Interactive</span></span>

* <span data-ttu-id="fc76f-803">修复了无法在 Python 2.x 中使用交互模式的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-803">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="fc76f-804">修复了启动时出错的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-804">Fixed errors on startup</span></span>
* <span data-ttu-id="fc76f-805">修复了无法在交互模式下运行某些命令的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-805">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="fc76f-806">IoT</span><span class="sxs-lookup"><span data-stu-id="fc76f-806">IoT</span></span>

* <span data-ttu-id="fc76f-807">添加了对设备预配服务的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-807">Added support for device provisioning service</span></span>
* <span data-ttu-id="fc76f-808">在命令和命令帮助中添加了弃用消息</span><span class="sxs-lookup"><span data-stu-id="fc76f-808">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="fc76f-809">添加了 IoT 检查，以告知用户有 IoT 扩展可用</span><span class="sxs-lookup"><span data-stu-id="fc76f-809">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="fc76f-810">监视</span><span class="sxs-lookup"><span data-stu-id="fc76f-810">Monitor</span></span>

* <span data-ttu-id="fc76f-811">添加了多诊断设置支持。</span><span class="sxs-lookup"><span data-stu-id="fc76f-811">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="fc76f-812">`az monitor diagnostic-settings create` 现在必需 `--name` 参数。</span><span class="sxs-lookup"><span data-stu-id="fc76f-812">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="fc76f-813">添加了命令 `monitor diagnostic-settings categories` 用于获取诊断设置类别</span><span class="sxs-lookup"><span data-stu-id="fc76f-813">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-814">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-814">Network</span></span>

* <span data-ttu-id="fc76f-815">修复了使用 `vnet-gateway update` 进入/退出主动-待机模式时出现的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-815">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="fc76f-816">在 `application-gateway [create|update]` 中添加了对 HTTP2 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-816">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="fc76f-817">配置文件</span><span class="sxs-lookup"><span data-stu-id="fc76f-817">Profile</span></span>

* <span data-ttu-id="fc76f-818">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-818">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="fc76f-819">角色</span><span class="sxs-lookup"><span data-stu-id="fc76f-819">Role</span></span>

* <span data-ttu-id="fc76f-820">为 `role assignment create` 添加了 `--assignee-object-id` 参数用于绕过图形查询</span><span class="sxs-lookup"><span data-stu-id="fc76f-820">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="fc76f-821">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="fc76f-821">Service Fabric</span></span>

* <span data-ttu-id="fc76f-822">在创建群集时生成的验证响应中添加了详细错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-822">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="fc76f-823">修复了运行多个命令时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-823">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-824">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-824">VM</span></span>

* <span data-ttu-id="fc76f-825">[预览] `vmss` 的跨区域支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-825">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="fc76f-826">[重大更改] 已将单区域 `vmss` 默认值更改为“Standard”负载均衡器</span><span class="sxs-lookup"><span data-stu-id="fc76f-826">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="fc76f-827">[重大更改] 已将EMSI 的 `externalIdentities` 更改为 `userAssignedIdentities`</span><span class="sxs-lookup"><span data-stu-id="fc76f-827">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="fc76f-828">[预览] 添加了 OS 磁盘交换支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-828">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="fc76f-829">添加了使用其他订阅中的 VM 映像的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-829">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="fc76f-830">为 `[vm|vmss] create` 添加了 `--plan-name`、`--plan-product`、`--plan-promotion-code` 和 `--plan-publisher` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-830">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="fc76f-831">修复了 `[vm|vmss] create` 出错问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-831">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="fc76f-832">修复了 `vm image list --all` 导致资源使用过度的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-832">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="fc76f-833">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-833">December 19, 2017</span></span>

<span data-ttu-id="fc76f-834">版本 2.0.23</span><span class="sxs-lookup"><span data-stu-id="fc76f-834">Version 2.0.23</span></span>

* <span data-ttu-id="fc76f-835">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-835">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="fc76f-836">容器</span><span class="sxs-lookup"><span data-stu-id="fc76f-836">Container</span></span>

* <span data-ttu-id="fc76f-837">纠正了容器日志参数的错误顺序</span><span class="sxs-lookup"><span data-stu-id="fc76f-837">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-838">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-838">Network</span></span>

* <span data-ttu-id="fc76f-839">为 `route-table [create|update]` 添加了 `--disable-bgp-route-propagation` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-839">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="fc76f-840">为 `public-ip [create|update]` 添加了 `--ip-tags` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-840">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-841">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-841">Storage</span></span>

* <span data-ttu-id="fc76f-842">添加了对存储 V2 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-842">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-843">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-843">VM</span></span>

* <span data-ttu-id="fc76f-844">[预览] 添加了对 VM 和 VMSS 的用户分配标识的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-844">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="fc76f-845">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-845">December 5, 2017</span></span>

<span data-ttu-id="fc76f-846">版本 2.0.22</span><span class="sxs-lookup"><span data-stu-id="fc76f-846">Version 2.0.22</span></span>

* <span data-ttu-id="fc76f-847">已删除 `az component` 命令。</span><span class="sxs-lookup"><span data-stu-id="fc76f-847">Removed `az component` commands.</span></span> <span data-ttu-id="fc76f-848">请改用 `az extension`</span><span class="sxs-lookup"><span data-stu-id="fc76f-848">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="fc76f-849">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-849">Core</span></span>
* <span data-ttu-id="fc76f-850">已将 `AZURE_US_GOV_CLOUD` AAD 颁发机构终结点从 login.microsoftonline.com 修改为 login.microsoftonline.us</span><span class="sxs-lookup"><span data-stu-id="fc76f-850">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="fc76f-851">已修复持续重新发送遥测数据的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-851">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-852">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-852">ACS</span></span>

* <span data-ttu-id="fc76f-853">已添加 `aks install-connector` 和 `aks remove-connector` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-853">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="fc76f-854">已改进 `acs create` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="fc76f-854">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="fc76f-855">已修复不带完全限定路径的 `aks get-credentials -f` 的用法</span><span class="sxs-lookup"><span data-stu-id="fc76f-855">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="fc76f-856">顾问</span><span class="sxs-lookup"><span data-stu-id="fc76f-856">Advisor</span></span>

* <span data-ttu-id="fc76f-857">初始版本</span><span class="sxs-lookup"><span data-stu-id="fc76f-857">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-858">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-858">Appservice</span></span>

* <span data-ttu-id="fc76f-859">已修复使用 `webapp config ssl upload` 时的证书名称生成问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-859">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="fc76f-860">已修复 `webapp [list|show]` 和 `functionapp [list|show]` 以显示正确的应用</span><span class="sxs-lookup"><span data-stu-id="fc76f-860">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="fc76f-861">已为 `WEBSITE_NODE_DEFAULT_VERSION` 添加了默认值</span><span class="sxs-lookup"><span data-stu-id="fc76f-861">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="fc76f-862">消耗</span><span class="sxs-lookup"><span data-stu-id="fc76f-862">Consumption</span></span>

* <span data-ttu-id="fc76f-863">已添加对 API 版本 2017-11-30 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-863">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="fc76f-864">容器</span><span class="sxs-lookup"><span data-stu-id="fc76f-864">Container</span></span>

* <span data-ttu-id="fc76f-865">已修复默认端口回归</span><span class="sxs-lookup"><span data-stu-id="fc76f-865">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="fc76f-866">监视</span><span class="sxs-lookup"><span data-stu-id="fc76f-866">Monitor</span></span>

* <span data-ttu-id="fc76f-867">已添加对指标命令的多维支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-867">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="fc76f-868">资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-868">Resource</span></span>

* <span data-ttu-id="fc76f-869">为 `resource show` 添加了 `--include-response-body` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-869">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="fc76f-870">角色</span><span class="sxs-lookup"><span data-stu-id="fc76f-870">Role</span></span>

* <span data-ttu-id="fc76f-871">已将“经典”管理员的默认分配显示添加到 `role assignment list`</span><span class="sxs-lookup"><span data-stu-id="fc76f-871">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="fc76f-872">已添加对 `ad sp reset-credentials` 的支持以便添加凭据而不是覆盖</span><span class="sxs-lookup"><span data-stu-id="fc76f-872">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="fc76f-873">已改进 `ad sp create-for-rbac` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="fc76f-873">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="fc76f-874">SQL</span><span class="sxs-lookup"><span data-stu-id="fc76f-874">SQL</span></span>

* <span data-ttu-id="fc76f-875">已添加 `sql db list-usages` 和 `sql db show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-875">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="fc76f-876">已添加 `sql server conn-policy show` 和 `sql server conn-policy update` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-876">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-877">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-877">VM</span></span>

* <span data-ttu-id="fc76f-878">已对 `az vm list-skus` 添加区域信息</span><span class="sxs-lookup"><span data-stu-id="fc76f-878">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="fc76f-879">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-879">November 14, 2017</span></span>

<span data-ttu-id="fc76f-880">版本 2.0.21</span><span class="sxs-lookup"><span data-stu-id="fc76f-880">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="fc76f-881">ACR</span><span class="sxs-lookup"><span data-stu-id="fc76f-881">ACR</span></span>

* <span data-ttu-id="fc76f-882">添加了在复制区域中创建 Webhook 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-882">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="fc76f-883">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-883">ACS</span></span>

* <span data-ttu-id="fc76f-884">已在 AKS 中将所有“代理”一词更改为“节点”</span><span class="sxs-lookup"><span data-stu-id="fc76f-884">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="fc76f-885">弃用了 `acs create` 的 `--orchestrator-release` 选项</span><span class="sxs-lookup"><span data-stu-id="fc76f-885">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="fc76f-886">已将 AKS 的默认 VM 大小更改为 `Standard_D1_v2`</span><span class="sxs-lookup"><span data-stu-id="fc76f-886">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="fc76f-887">在 Windows 上修复了 `az aks browse`</span><span class="sxs-lookup"><span data-stu-id="fc76f-887">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="fc76f-888">在 Windows 上修复了 `az aks get-credentials`</span><span class="sxs-lookup"><span data-stu-id="fc76f-888">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-889">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-889">Appservice</span></span>

* <span data-ttu-id="fc76f-890">添加了 Web 应用和函数应用的部署源 `config-zip`</span><span class="sxs-lookup"><span data-stu-id="fc76f-890">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="fc76f-891">为 `az webapp log config` 添加了 `--docker-container-logging` 选项</span><span class="sxs-lookup"><span data-stu-id="fc76f-891">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="fc76f-892">从 `az webapp log config` 的参数 `--web-server-logging` 中删除了 `storage` 选项</span><span class="sxs-lookup"><span data-stu-id="fc76f-892">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="fc76f-893">完善了 `deployment user set` 的错误消息</span><span class="sxs-lookup"><span data-stu-id="fc76f-893">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="fc76f-894">添加了创建 Linux 函数应用的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-894">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="fc76f-895">固定 `list-locations`</span><span class="sxs-lookup"><span data-stu-id="fc76f-895">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="fc76f-896">Batch</span><span class="sxs-lookup"><span data-stu-id="fc76f-896">Batch</span></span>

* <span data-ttu-id="fc76f-897">修复了在 pool create 命令中结合 `--image` 标志使用资源 ID 时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-897">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="fc76f-898">Batchai</span><span class="sxs-lookup"><span data-stu-id="fc76f-898">Batchai</span></span>

* <span data-ttu-id="fc76f-899">在 `file-server create` 命令中提供了 `--vm-size` 的简短选项 `-s`（提供 VM 大小）</span><span class="sxs-lookup"><span data-stu-id="fc76f-899">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="fc76f-900">为 `cluster create` 参数添加了存储帐户名称和密钥自变量</span><span class="sxs-lookup"><span data-stu-id="fc76f-900">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="fc76f-901">纠正了 `job list-files` 和 `job stream-file` 的文档</span><span class="sxs-lookup"><span data-stu-id="fc76f-901">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="fc76f-902">在 `job create` 命令中提供了 `--cluster-name` 的简短选项 `-r`（提供群集名称）</span><span class="sxs-lookup"><span data-stu-id="fc76f-902">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="fc76f-903">云</span><span class="sxs-lookup"><span data-stu-id="fc76f-903">Cloud</span></span>

* <span data-ttu-id="fc76f-904">更改了 `cloud [register|update]`，以防止注册缺少所需终结点的云</span><span class="sxs-lookup"><span data-stu-id="fc76f-904">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="fc76f-905">容器</span><span class="sxs-lookup"><span data-stu-id="fc76f-905">Container</span></span>

* <span data-ttu-id="fc76f-906">添加了打开多个端口的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-906">Added support to open multiple ports</span></span>
* <span data-ttu-id="fc76f-907">添加了容器组重启策略</span><span class="sxs-lookup"><span data-stu-id="fc76f-907">Added container group restart policy</span></span>
* <span data-ttu-id="fc76f-908">添加了将 Azure 文件共享装载为卷的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-908">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="fc76f-909">更新了帮助器文档</span><span class="sxs-lookup"><span data-stu-id="fc76f-909">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="fc76f-910">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="fc76f-910">Data Lake Analytics</span></span>

* <span data-ttu-id="fc76f-911">更改了 `[job|account] list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="fc76f-911">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="fc76f-912">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="fc76f-912">Data Lake Store</span></span>

* <span data-ttu-id="fc76f-913">更改了 `account list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="fc76f-913">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="fc76f-914">分机</span><span class="sxs-lookup"><span data-stu-id="fc76f-914">Extension</span></span>

* <span data-ttu-id="fc76f-915">添加了 `extension list-available` 用于列出官方的 Microsoft 扩展</span><span class="sxs-lookup"><span data-stu-id="fc76f-915">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="fc76f-916">为 `extension [add|update]` 添加了 `--name`，以便按名称安装扩展</span><span class="sxs-lookup"><span data-stu-id="fc76f-916">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="fc76f-917">IoT</span><span class="sxs-lookup"><span data-stu-id="fc76f-917">IoT</span></span>

* <span data-ttu-id="fc76f-918">添加了对证书颁发机构 (CA) 和证书链的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-918">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="fc76f-919">监视</span><span class="sxs-lookup"><span data-stu-id="fc76f-919">Monitor</span></span>

* <span data-ttu-id="fc76f-920">添加了 `activity-log alert` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-920">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-921">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-921">Network</span></span>

* <span data-ttu-id="fc76f-922">添加了对 CAA DNS 记录的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-922">Added support for CAA DNS records</span></span>
* <span data-ttu-id="fc76f-923">修复了无法使用 `traffic-manager profile update` 更新终结点的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-923">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="fc76f-924">修复了在采用某种 VNET 创建方式时 `vnet update --dns-servers` 无法正常运行的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-924">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="fc76f-925">修复了 `dns zone import` 错误导入相对 DNS 名称的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-925">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="fc76f-926">预留</span><span class="sxs-lookup"><span data-stu-id="fc76f-926">Reservations</span></span>

* <span data-ttu-id="fc76f-927">初始预览版</span><span class="sxs-lookup"><span data-stu-id="fc76f-927">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="fc76f-928">资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-928">Resource</span></span>

* <span data-ttu-id="fc76f-929">添加了在 `--resource` 参数中指定资源 ID 的支持，以及对资源级锁的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-929">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="fc76f-930">SQL</span><span class="sxs-lookup"><span data-stu-id="fc76f-930">SQL</span></span>

* <span data-ttu-id="fc76f-931">为 `sql server vnet-rule [create|update]` 添加了 `--ignore-missing-vnet-service-endpoint` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-931">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-932">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-932">Storage</span></span>

* <span data-ttu-id="fc76f-933">更改了 `storage account create` 以使用 SKU `Standard_RAGRS` 作为默认值</span><span class="sxs-lookup"><span data-stu-id="fc76f-933">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="fc76f-934">修复了处理包含非 ASCII 字符的文件/Blob 名称时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-934">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="fc76f-935">修复了阻止在 `storage [blob|file] copy start-batch` 中使用 `--source-uri` 的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-935">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="fc76f-936">添加了在 `storage [blob|file] delete-batch` 中包含和删除多个对象的命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-936">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="fc76f-937">修复了使用 `storage metrics update` 启用指标时出现的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-937">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="fc76f-938">修复了使用 `storage blob upload-batch` 时，如果文件超过 200GB 所出现的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-938">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="fc76f-939">修复了 `storage account [create|update]` 忽略 `--bypass` 和 `--default-action` 的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-939">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-940">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-940">VM</span></span>

* <span data-ttu-id="fc76f-941">修复了 `vmss create` 阻止使用 `Basic` 大小层的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-941">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="fc76f-942">针对包含计费信息的自定义映像，为 `[vm|vmss] create` 添加了 `--plan` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-942">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="fc76f-943">添加了 `vm secret `[add|remove|list]\` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-943">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="fc76f-944">已将 `vm format-secret` 重命名为 `vm secret format`</span><span class="sxs-lookup"><span data-stu-id="fc76f-944">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="fc76f-945">为 `vm encryption enable` 添加了 `--encrypt format` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-945">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="fc76f-946">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-946">October 24, 2017</span></span>

<span data-ttu-id="fc76f-947">版本 2.0.20</span><span class="sxs-lookup"><span data-stu-id="fc76f-947">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="fc76f-948">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-948">Core</span></span>

* <span data-ttu-id="fc76f-949">已更新 `2017-03-09-profile` 以使用 `MGMT_STORAGE` API 版本 `2016-01-01`</span><span class="sxs-lookup"><span data-stu-id="fc76f-949">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="fc76f-950">ACR</span><span class="sxs-lookup"><span data-stu-id="fc76f-950">ACR</span></span>

* <span data-ttu-id="fc76f-951">已更新资源管理以指向 `2017-10-01` API 版本</span><span class="sxs-lookup"><span data-stu-id="fc76f-951">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="fc76f-952">已将“带来你自己的存储”SKU 更改为“经典”</span><span class="sxs-lookup"><span data-stu-id="fc76f-952">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="fc76f-953">已将注册表 SKU 重命名为“基本”、“标准”和“高级”</span><span class="sxs-lookup"><span data-stu-id="fc76f-953">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-954">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-954">ACS</span></span>

* <span data-ttu-id="fc76f-955">[PREVIEW] 添加了 `az aks` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-955">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="fc76f-956">已修复 Kubernetes `get-credentials`</span><span class="sxs-lookup"><span data-stu-id="fc76f-956">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-957">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-957">Appservice</span></span>

* <span data-ttu-id="fc76f-958">已修复所下载 `webapp` 日志可能无效的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-958">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="fc76f-959">组件</span><span class="sxs-lookup"><span data-stu-id="fc76f-959">Component</span></span>

* <span data-ttu-id="fc76f-960">为所有安装程序添加了更清晰的弃用消息并添加了确认提示</span><span class="sxs-lookup"><span data-stu-id="fc76f-960">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="fc76f-961">监视</span><span class="sxs-lookup"><span data-stu-id="fc76f-961">Monitor</span></span>

* <span data-ttu-id="fc76f-962">添加了 `action-group` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-962">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="fc76f-963">资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-963">Resource</span></span>

* <span data-ttu-id="fc76f-964">修复了 `group export` 中与 msrest 依赖项的最新版本不兼容的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-964">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="fc76f-965">修复了 `policy assignment create` 以使用内置策略定义和策略集定义</span><span class="sxs-lookup"><span data-stu-id="fc76f-965">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-966">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-966">VM</span></span>

* <span data-ttu-id="fc76f-967">为 `vmss create` 添加了 `--accelerated-networking` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-967">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="fc76f-968">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-968">October 9, 2017</span></span>

<span data-ttu-id="fc76f-969">版本 2.0.19</span><span class="sxs-lookup"><span data-stu-id="fc76f-969">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="fc76f-970">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-970">Core</span></span>

* <span data-ttu-id="fc76f-971">在 Azure Stack 中添加了一个尾随斜杠用于处理 ADFS 机构 URL</span><span class="sxs-lookup"><span data-stu-id="fc76f-971">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-972">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-972">Appservice</span></span>

* <span data-ttu-id="fc76f-973">添加了新命令 `webapp update` 用于执行常规更新</span><span class="sxs-lookup"><span data-stu-id="fc76f-973">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="fc76f-974">Batch</span><span class="sxs-lookup"><span data-stu-id="fc76f-974">Batch</span></span>

* <span data-ttu-id="fc76f-975">已更新为 Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="fc76f-975">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="fc76f-976">更新了 VirtualMachineConfiguration 的 `--image`，用于支持除 publish:offer:sku:version 以外的 ARM 映像引用</span><span class="sxs-lookup"><span data-stu-id="fc76f-976">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="fc76f-977">添加了对 Batch 扩展命令新 CLI 扩展模型的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-977">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="fc76f-978">从组件模型中删除了 Batch 支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-978">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="fc76f-979">Batchai</span><span class="sxs-lookup"><span data-stu-id="fc76f-979">Batchai</span></span>

* <span data-ttu-id="fc76f-980">Batch AI 模块初始版本</span><span class="sxs-lookup"><span data-stu-id="fc76f-980">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="fc76f-981">KeyVault</span><span class="sxs-lookup"><span data-stu-id="fc76f-981">Keyvault</span></span>

* <span data-ttu-id="fc76f-982">修复了在 Azure Stack 中使用 ADFS 时发生的 Key Vault 身份验证问题。</span><span class="sxs-lookup"><span data-stu-id="fc76f-982">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="fc76f-983">(#4448)</span><span class="sxs-lookup"><span data-stu-id="fc76f-983">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="fc76f-984">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-984">Network</span></span>

* <span data-ttu-id="fc76f-985">已将 `application-gateway address-pool create` 的 `--server` 参数更改为可选，以允许空地址池</span><span class="sxs-lookup"><span data-stu-id="fc76f-985">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="fc76f-986">更新了 `traffic-manager` 以支持最新功能</span><span class="sxs-lookup"><span data-stu-id="fc76f-986">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="fc76f-987">资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-987">Resource</span></span>

* <span data-ttu-id="fc76f-988">在 `group` 中添加了对资源组名称使用 `--resource-group/-g` 选项的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-988">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="fc76f-989">为 `account lock` 添加了命令用于处理订阅级锁</span><span class="sxs-lookup"><span data-stu-id="fc76f-989">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="fc76f-990">为 `group lock` 添加了命令用于处理组级锁</span><span class="sxs-lookup"><span data-stu-id="fc76f-990">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="fc76f-991">为 `resource lock` 添加了命令用于处理资源级锁</span><span class="sxs-lookup"><span data-stu-id="fc76f-991">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="fc76f-992">Sql</span><span class="sxs-lookup"><span data-stu-id="fc76f-992">Sql</span></span>

* <span data-ttu-id="fc76f-993">添加了 SQL 透明数据加密 (TDE) 和自带密钥 TDE 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-993">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="fc76f-994">添加了 `db list-deleted` 命令和 `db restore --deleted-time` 参数，以便能够找到和还原已删除的数据库</span><span class="sxs-lookup"><span data-stu-id="fc76f-994">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="fc76f-995">添加了 `db op list` 和 `db op cancel`，以便能够列出和取消正在对数据库执行的操作</span><span class="sxs-lookup"><span data-stu-id="fc76f-995">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-996">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-996">Storage</span></span>

* <span data-ttu-id="fc76f-997">添加了对文件共享快照的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-997">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-998">Vm</span><span class="sxs-lookup"><span data-stu-id="fc76f-998">Vm</span></span>

* <span data-ttu-id="fc76f-999">修复了 `vm show` 中的一个 bug：在缺少专用 IP 地址的情况下使用 `-d` 会导致崩溃</span><span class="sxs-lookup"><span data-stu-id="fc76f-999">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="fc76f-1000">[预览] 添加了滚动升级到 `vmss create` 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1000">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="fc76f-1001">添加了使用 `vm encryption enable` 更新加密设置的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1001">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="fc76f-1002">为 `vm create` 添加了 `--os-disk-size-gb` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1002">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="fc76f-1003">为 Windows 中的 `vmss create` 添加了 `--license-type` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1003">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="fc76f-1004">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-1004">September 22, 2017</span></span>

<span data-ttu-id="fc76f-1005">版本 2.0.18</span><span class="sxs-lookup"><span data-stu-id="fc76f-1005">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="fc76f-1006">资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-1006">Resource</span></span>

* <span data-ttu-id="fc76f-1007">添加了对显示内置策略定义的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1007">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="fc76f-1008">添加了用于创建策略定义的支持模式参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1008">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="fc76f-1009">为 `managedapp definition create` 添加了对 UI 定义和模板的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1009">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="fc76f-1010">[重大更改] 已将 `managedapp` 资源类型从 `appliances` 更改到 `applications`，从 `applianceDefinitions` 更改到 `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1010">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-1011">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-1011">Network</span></span>

* <span data-ttu-id="fc76f-1012">为 `network lb` 和 `network public-ip` 子命令添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1012">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="fc76f-1013">为 `express-route` 添加了对 IPv6 Microsoft 对等互连的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1013">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="fc76f-1014">添加了 `asg` 应用程序安全组命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1014">Added `asg` application security group commands</span></span>
* <span data-ttu-id="fc76f-1015">为 `nic [create|ip-config create|ip-config update]` 添加了 `--application-security-groups` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1015">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="fc76f-1016">为 `nsg rule [create|update]` 添加了 `--source-asgs` 和 `--destination-asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1016">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="fc76f-1017">为 `vnet [create|update]` 添加了 `--ddos-protection` 和 `--vm-protection` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1017">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="fc76f-1018">添加了 `network [vnet-gateway|vpn-client|show-url]` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1018">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-1019">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-1019">Storage</span></span>

* <span data-ttu-id="fc76f-1020">已修复了 `storage account network-rule` 命令在更新 SDK 后可能会失败的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1020">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="fc76f-1021">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="fc76f-1021">Eventgrid</span></span>

* <span data-ttu-id="fc76f-1022">更新了 Azure 事件网格 Python SDK 以使用较新的 API 版本“2017-09-15-preview”</span><span class="sxs-lookup"><span data-stu-id="fc76f-1022">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="fc76f-1023">SQL</span><span class="sxs-lookup"><span data-stu-id="fc76f-1023">SQL</span></span>

* <span data-ttu-id="fc76f-1024">将 `sql server list` 的参数 `--resource-group` 更改为可选。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1024">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="fc76f-1025">如果未指定，将返回订阅中的所有 SQL 服务器</span><span class="sxs-lookup"><span data-stu-id="fc76f-1025">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="fc76f-1026">为 `db [create|copy|restore|update|replica create|create|update]` 和 `dw [create|update]` 添加了 `--no-wait` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1026">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="fc76f-1027">KeyVault</span><span class="sxs-lookup"><span data-stu-id="fc76f-1027">Keyvault</span></span>

* <span data-ttu-id="fc76f-1028">添加了对从代理后执行 Keyvault 命令的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1028">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-1029">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-1029">VM</span></span>

* <span data-ttu-id="fc76f-1030">为 `[vm|vmss|disk] create` 添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1030">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="fc76f-1031">已修复了将 `--app-gateway ID` 与 `vmss create` 一起使用会导致故障的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1031">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="fc76f-1032">为 `vm create` 添加了 `--asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1032">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="fc76f-1033">添加了对使用 `vm run-command` 在 VM 上运行命令的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1033">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="fc76f-1034">[预览] 添加了对使用 `vmss encryption` 进行 VMSS 磁盘加密的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1034">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="fc76f-1035">添加了对使用 `vm perform-maintenance` 在 VM 上执行维护的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1035">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-1036">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-1036">ACS</span></span>

* <span data-ttu-id="fc76f-1037">[预览] 为适用于 ACS 预览区域的 `acs create` 添加了 `--orchestrator-release` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1037">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-1038">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-1038">Appservice</span></span>

* <span data-ttu-id="fc76f-1039">添加了使用 `webapp auth [update|show]` 更新和显示身份验证设置的功能</span><span class="sxs-lookup"><span data-stu-id="fc76f-1039">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="fc76f-1040">备份</span><span class="sxs-lookup"><span data-stu-id="fc76f-1040">Backup</span></span>

* <span data-ttu-id="fc76f-1041">预览版</span><span class="sxs-lookup"><span data-stu-id="fc76f-1041">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="fc76f-1042">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-1042">September 11, 2017</span></span>

<span data-ttu-id="fc76f-1043">版本 2.0.17</span><span class="sxs-lookup"><span data-stu-id="fc76f-1043">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="fc76f-1044">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-1044">Core</span></span>

* <span data-ttu-id="fc76f-1045">启用了命令模块在遥测中设置其自己的相关 ID</span><span class="sxs-lookup"><span data-stu-id="fc76f-1045">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="fc76f-1046">修复了在遥测设置为诊断模式时的 JSON 转储问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1046">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-1047">Acs</span><span class="sxs-lookup"><span data-stu-id="fc76f-1047">Acs</span></span>

* <span data-ttu-id="fc76f-1048">添加了 `acs list-locations` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1048">Added `acs list-locations` command</span></span>
* <span data-ttu-id="fc76f-1049">使 `ssh-key-file` 附带预期的默认值</span><span class="sxs-lookup"><span data-stu-id="fc76f-1049">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-1050">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-1050">Appservice</span></span>

* <span data-ttu-id="fc76f-1051">添加了在未包含活动服务计划的资源组中创建 Web 应用的功能</span><span class="sxs-lookup"><span data-stu-id="fc76f-1051">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="fc76f-1052">CDN</span><span class="sxs-lookup"><span data-stu-id="fc76f-1052">CDN</span></span>

* <span data-ttu-id="fc76f-1053">修复了 `cdn custom-domain create` 的“CustomDomain is not interable”bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1053">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="fc76f-1054">分机</span><span class="sxs-lookup"><span data-stu-id="fc76f-1054">Extension</span></span>

* <span data-ttu-id="fc76f-1055">初始版本</span><span class="sxs-lookup"><span data-stu-id="fc76f-1055">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="fc76f-1056">KeyVault</span><span class="sxs-lookup"><span data-stu-id="fc76f-1056">Keyvault</span></span>

* <span data-ttu-id="fc76f-1057">为 `keyvault set-policy` 修复了权限区分大小写的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1057">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-1058">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-1058">Network</span></span>

* <span data-ttu-id="fc76f-1059">已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1059">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="fc76f-1060">已为 `vnet subnet create/update` 将 `--private-access-services` 参数重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1060">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="fc76f-1061">在 `nsg rule create/update` 中添加了对多个 IP 范围和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1061">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="fc76f-1062">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1062">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="fc76f-1063">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1063">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="fc76f-1064">资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-1064">Resource</span></span>

* <span data-ttu-id="fc76f-1065">允许在 `policy definition create` 和 `policy definition update` 中传入资源策略参数定义</span><span class="sxs-lookup"><span data-stu-id="fc76f-1065">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="fc76f-1066">允许为 `policy assignment create` 传入参数值</span><span class="sxs-lookup"><span data-stu-id="fc76f-1066">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="fc76f-1067">允许为所有参数传入 JSON 或文件</span><span class="sxs-lookup"><span data-stu-id="fc76f-1067">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="fc76f-1068">更新了 API 版本</span><span class="sxs-lookup"><span data-stu-id="fc76f-1068">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="fc76f-1069">SQL</span><span class="sxs-lookup"><span data-stu-id="fc76f-1069">SQL</span></span>

* <span data-ttu-id="fc76f-1070">添加了 `sql server vnet-rule` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1070">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-1071">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-1071">VM</span></span>

* <span data-ttu-id="fc76f-1072">已修复：除非提供 `--scope`，否则不分配访问权限</span><span class="sxs-lookup"><span data-stu-id="fc76f-1072">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="fc76f-1073">已修复：使用与门户相同的扩展命名</span><span class="sxs-lookup"><span data-stu-id="fc76f-1073">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="fc76f-1074">已从 `[vm|vmss] create` 输出中删除了 `subscription`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1074">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="fc76f-1075">已修复：`[vm|vmss] create` SKU 无法应用于带映像的数据磁盘</span><span class="sxs-lookup"><span data-stu-id="fc76f-1075">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="fc76f-1076">已修复：`vm format-secret --secrets` 不接受新行分隔的 ID</span><span class="sxs-lookup"><span data-stu-id="fc76f-1076">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="fc76f-1077">2017 年 8 月31 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-1077">August 31, 2017</span></span>

<span data-ttu-id="fc76f-1078">版本 2.0.16</span><span class="sxs-lookup"><span data-stu-id="fc76f-1078">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="fc76f-1079">KeyVault</span><span class="sxs-lookup"><span data-stu-id="fc76f-1079">Keyvault</span></span>

* <span data-ttu-id="fc76f-1080">修复了在尝试使用 `secret download` 自动解析机密编码时的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1080">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="fc76f-1081">Sf</span><span class="sxs-lookup"><span data-stu-id="fc76f-1081">Sf</span></span>

* <span data-ttu-id="fc76f-1082">弃用所有支持 Service Fabric CLI (sfctl) 的命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1082">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-1083">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-1083">Storage</span></span>

* <span data-ttu-id="fc76f-1084">修复了无法在不支持 NetworkACLs 功能的区域中创建存储帐户的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1084">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="fc76f-1085">在 Blob 和文件上载过程中确定内容类型和内容编码（如果既未指定内容类型，也未指定内容编码）</span><span class="sxs-lookup"><span data-stu-id="fc76f-1085">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="fc76f-1086">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-1086">August 28, 2017</span></span>

<span data-ttu-id="fc76f-1087">版本 2.0.15</span><span class="sxs-lookup"><span data-stu-id="fc76f-1087">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="fc76f-1088">CLI</span><span class="sxs-lookup"><span data-stu-id="fc76f-1088">CLI</span></span>

* <span data-ttu-id="fc76f-1089">在 `--version` 中添加了法律说明</span><span class="sxs-lookup"><span data-stu-id="fc76f-1089">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-1090">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-1090">ACS</span></span>

* <span data-ttu-id="fc76f-1091">更正了预览区域</span><span class="sxs-lookup"><span data-stu-id="fc76f-1091">Corrected preview regions</span></span>
* <span data-ttu-id="fc76f-1092">正确设置了默认 `dns_name_prefix` 的格式</span><span class="sxs-lookup"><span data-stu-id="fc76f-1092">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="fc76f-1093">优化了 acs 命令输出</span><span class="sxs-lookup"><span data-stu-id="fc76f-1093">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-1094">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-1094">Appservice</span></span>

* <span data-ttu-id="fc76f-1095">[重大更改] 修复了 `az webapp config appsettings [delete|set]` 输出中的不一致</span><span class="sxs-lookup"><span data-stu-id="fc76f-1095">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="fc76f-1096">为 `az webapp config container set --docker-custom-image-name` 的 `-i` 添加了新别名</span><span class="sxs-lookup"><span data-stu-id="fc76f-1096">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="fc76f-1097">公开了 `az webapp log show`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1097">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="fc76f-1098">公开了 `az webapp delete` 中的新参数，用于保留应用服务计划、指标或 dns 注册</span><span class="sxs-lookup"><span data-stu-id="fc76f-1098">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="fc76f-1099">已修复：正确检测槽位设置</span><span class="sxs-lookup"><span data-stu-id="fc76f-1099">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="fc76f-1100">IoT</span><span class="sxs-lookup"><span data-stu-id="fc76f-1100">IoT</span></span>

* <span data-ttu-id="fc76f-1101">修复了 #3934：策略创建操作不再清除现有的策略</span><span class="sxs-lookup"><span data-stu-id="fc76f-1101">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-1102">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-1102">Network</span></span>

* <span data-ttu-id="fc76f-1103">[重大更改] 已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1103">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="fc76f-1104">[重大更改] 已将 `vnet subnet [create|update]` 的选项 `--private-access-services` 重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1104">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="fc76f-1105">在 `nsg rule [create|update]` 中添加了对多个 IP 和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1105">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="fc76f-1106">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1106">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="fc76f-1107">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1107">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="fc76f-1108">配置文件</span><span class="sxs-lookup"><span data-stu-id="fc76f-1108">Profile</span></span>

* <span data-ttu-id="fc76f-1109">公开了 `--msi` 和 `--msi-port`，以便使用虚拟机的标识登录</span><span class="sxs-lookup"><span data-stu-id="fc76f-1109">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="fc76f-1110">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="fc76f-1110">Service Fabric</span></span>

* <span data-ttu-id="fc76f-1111">预览版</span><span class="sxs-lookup"><span data-stu-id="fc76f-1111">Preview release</span></span>
* <span data-ttu-id="fc76f-1112">简化了命令的注册表用户/密码规则</span><span class="sxs-lookup"><span data-stu-id="fc76f-1112">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="fc76f-1113">修复了即使在参数中传入了密码，也提示用户输入密码的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1113">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="fc76f-1114">添加了对空 `registry_cred` 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1114">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-1115">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-1115">Storage</span></span>

* <span data-ttu-id="fc76f-1116">启用了设置 Blob 层</span><span class="sxs-lookup"><span data-stu-id="fc76f-1116">Enabled setting blob tier</span></span>
* <span data-ttu-id="fc76f-1117">为 `storage account [create|update]` 添加了 `--bypass` 和 `--default-action` 参数用于支持服务隧道</span><span class="sxs-lookup"><span data-stu-id="fc76f-1117">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="fc76f-1118">添加了用于在 `storage account network-rule` 中添加 VNET 规则和基于 IP 的规则的命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1118">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="fc76f-1119">启用了使用客户管理的密钥进行服务加密的功能</span><span class="sxs-lookup"><span data-stu-id="fc76f-1119">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="fc76f-1120">[重大更改] 已将 `az storage account create and az storage account update` 命令的选项 `--encryption` 重命名为 `--encryption-services`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1120">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="fc76f-1121">修复了 #4220：`az storage account update encryption` - 语法不匹配</span><span class="sxs-lookup"><span data-stu-id="fc76f-1121">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-1122">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-1122">VM</span></span>

* <span data-ttu-id="fc76f-1123">修复了使用 `--instance-id *` 时，针对 `vmss get-instance-view` 显示多余且错误的信息的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1123">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="fc76f-1124">在 `vmss create` 中添加了对 `--lb-sku` 的支持：</span><span class="sxs-lookup"><span data-stu-id="fc76f-1124">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="fc76f-1125">从 `[vm|vmss] create` 的管理员名称方块列表中删除了人员名称</span><span class="sxs-lookup"><span data-stu-id="fc76f-1125">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="fc76f-1126">修复了当无法从映像中提取计划信息时，`[vm|vmss] create` 引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1126">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="fc76f-1127">修复了创建包含内部 LB 的 vmms 规模集时发生崩溃的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1127">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="fc76f-1128">修复了 `--no-wait` 参数无法配合 `vm availability-set create` 工作的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1128">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="fc76f-1129">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-1129">August 15, 2017</span></span>

<span data-ttu-id="fc76f-1130">版本 2.0.14</span><span class="sxs-lookup"><span data-stu-id="fc76f-1130">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-1131">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-1131">ACS</span></span>

* <span data-ttu-id="fc76f-1132">更正了 kubernetes 的 sshMaster0 端口号</span><span class="sxs-lookup"><span data-stu-id="fc76f-1132">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-1133">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-1133">Appservice</span></span>

* <span data-ttu-id="fc76f-1134">修复了创建基于新 Git 的 Linux Web 应用时发生异常的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1134">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="fc76f-1135">事件网格</span><span class="sxs-lookup"><span data-stu-id="fc76f-1135">Event Grid</span></span>

* <span data-ttu-id="fc76f-1136">添加了 SDK 依赖项</span><span class="sxs-lookup"><span data-stu-id="fc76f-1136">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="fc76f-1137">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-1137">August 11, 2017</span></span>

<span data-ttu-id="fc76f-1138">版本 2.0.13</span><span class="sxs-lookup"><span data-stu-id="fc76f-1138">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-1139">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-1139">ACS</span></span>

* <span data-ttu-id="fc76f-1140">添加了更多预览区域</span><span class="sxs-lookup"><span data-stu-id="fc76f-1140">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="fc76f-1141">Batch</span><span class="sxs-lookup"><span data-stu-id="fc76f-1141">Batch</span></span>

* <span data-ttu-id="fc76f-1142">已更新到 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="fc76f-1142">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="fc76f-1143">添加了新命令用于显示作业的任务计数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1143">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="fc76f-1144">修复了处理资源文件 SAS URL 时的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1144">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="fc76f-1145">Batch 帐户终结点现在支持可选的“https://” 前缀</span><span class="sxs-lookup"><span data-stu-id="fc76f-1145">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="fc76f-1146">支持将包含 100 多个任务的列表添加到作业</span><span class="sxs-lookup"><span data-stu-id="fc76f-1146">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="fc76f-1147">添加了加载扩展命令模块的调试日志记录</span><span class="sxs-lookup"><span data-stu-id="fc76f-1147">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="fc76f-1148">组件</span><span class="sxs-lookup"><span data-stu-id="fc76f-1148">Component</span></span>

* <span data-ttu-id="fc76f-1149">为“az component”命令添加了弃用警告</span><span class="sxs-lookup"><span data-stu-id="fc76f-1149">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="fc76f-1150">容器</span><span class="sxs-lookup"><span data-stu-id="fc76f-1150">Container</span></span>

* <span data-ttu-id="fc76f-1151">`create`：修复了某个环境变量中不允许等于号的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1151">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="fc76f-1152">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="fc76f-1152">Data Lake Store</span></span>

* <span data-ttu-id="fc76f-1153">启用了进度控件</span><span class="sxs-lookup"><span data-stu-id="fc76f-1153">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="fc76f-1154">事件网格</span><span class="sxs-lookup"><span data-stu-id="fc76f-1154">Event Grid</span></span>

* <span data-ttu-id="fc76f-1155">初始版本</span><span class="sxs-lookup"><span data-stu-id="fc76f-1155">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-1156">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-1156">Network</span></span>

* <span data-ttu-id="fc76f-1157">`lb`：修复了某些子资源名称在省略时无法正确解析的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1157">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="fc76f-1158">`application-gateway {subresource} delete`：修复了不遵循 `--no-wait` 的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1158">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="fc76f-1159">`application-gateway http-settings update`：修复了无法关闭 `--connection-draining-timeout` 的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1159">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="fc76f-1160">修复了 `az network vpn-connection ipsec-policy add` 包含意外关键字参数 `sa_data_size_kilobyes` 的错误</span><span class="sxs-lookup"><span data-stu-id="fc76f-1160">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="fc76f-1161">配置文件</span><span class="sxs-lookup"><span data-stu-id="fc76f-1161">Profile</span></span>

* <span data-ttu-id="fc76f-1162">`account list`：添加了 `--refresh` 用于从服务器同步最新订阅</span><span class="sxs-lookup"><span data-stu-id="fc76f-1162">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-1163">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-1163">Storage</span></span>

* <span data-ttu-id="fc76f-1164">启用了使用系统分配的标识更新存储帐户的功能</span><span class="sxs-lookup"><span data-stu-id="fc76f-1164">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-1165">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-1165">VM</span></span>

* <span data-ttu-id="fc76f-1166">`availability-set`：公开了转换时的容错域计数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1166">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="fc76f-1167">公开了 `list-skus` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1167">Exposed `list-skus` command</span></span>
* <span data-ttu-id="fc76f-1168">支持在不创建角色分配的情况下分配标识</span><span class="sxs-lookup"><span data-stu-id="fc76f-1168">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="fc76f-1169">附加数据磁盘时应用存储 SKU</span><span class="sxs-lookup"><span data-stu-id="fc76f-1169">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="fc76f-1170">删除了使用托管磁盘时的默认 OS 磁盘名称和存储 SKU</span><span class="sxs-lookup"><span data-stu-id="fc76f-1170">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="fc76f-1171">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-1171">July 28, 2017</span></span>

<span data-ttu-id="fc76f-1172">版本 2.0.12</span><span class="sxs-lookup"><span data-stu-id="fc76f-1172">Version 2.0.12</span></span>

* <span data-ttu-id="fc76f-1173">添加了容器命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1173">Added container commands</span></span>
* <span data-ttu-id="fc76f-1174">添加了计费和消耗模块</span><span class="sxs-lookup"><span data-stu-id="fc76f-1174">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="fc76f-1175">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-1175">Core</span></span>

* <span data-ttu-id="fc76f-1176">输出包含证书的服务主体的 SDK 身份验证信息</span><span class="sxs-lookup"><span data-stu-id="fc76f-1176">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="fc76f-1177">修复了部署进度异常</span><span class="sxs-lookup"><span data-stu-id="fc76f-1177">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="fc76f-1178">使用当前云中的 arm 终结点创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="fc76f-1178">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="fc76f-1179">改进了 clouds.config 文件的并发处理 (#3636)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1179">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="fc76f-1180">刷新每个命令执行进程的客户端请求 ID</span><span class="sxs-lookup"><span data-stu-id="fc76f-1180">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="fc76f-1181">使用适当的 SDK 配置文件创建订阅客户端 (#3635)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1181">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="fc76f-1182">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1182">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="fc76f-1183">添加了通过 jmespath 查询选择表输出字段的支持 (#3581)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1183">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="fc76f-1184">改进了分析参数的静默和包含手势的追加历史记录 (#3434)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1184">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="fc76f-1185">使用适当的 SDK 配置文件创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="fc76f-1185">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="fc76f-1186">将所有现有记录文件移到最新的文件夹</span><span class="sxs-lookup"><span data-stu-id="fc76f-1186">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="fc76f-1187">修复了 VM/VMSS 创建操作的幂等性 (#3586)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1187">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="fc76f-1188">命令路径不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="fc76f-1188">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="fc76f-1189">某些布尔类型的参数不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="fc76f-1189">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="fc76f-1190">支持登录到 Azure Stack 等本地服务器上的 ADFS</span><span class="sxs-lookup"><span data-stu-id="fc76f-1190">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="fc76f-1191">修复了并发写入 clouds.config 的问题 (#3255)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1191">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="fc76f-1192">ACR</span><span class="sxs-lookup"><span data-stu-id="fc76f-1192">ACR</span></span>

* <span data-ttu-id="fc76f-1193">针对托管注册表添加了 `show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1193">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="fc76f-1194">支持托管注册表的 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="fc76f-1194">Support SKU update for managed registries</span></span>
* <span data-ttu-id="fc76f-1195">添加了包含托管 SKU 的托管注册表</span><span class="sxs-lookup"><span data-stu-id="fc76f-1195">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="fc76f-1196">通过 ACR Webhook 命令模块添加了托管注册表的 Webhook</span><span class="sxs-lookup"><span data-stu-id="fc76f-1196">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="fc76f-1197">添加了使用 acr login 命令进行 AAD 身份验证的功能</span><span class="sxs-lookup"><span data-stu-id="fc76f-1197">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="fc76f-1198">添加了 Docker 存储库、清单和标记的 delete 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1198">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-1199">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-1199">ACS</span></span>

* <span data-ttu-id="fc76f-1200">API 版本 2017-07-01 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1200">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-1201">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-1201">Appservice</span></span>

* <span data-ttu-id="fc76f-1202">修复了列出 Linux Web 应用时不返回任何内容的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1202">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="fc76f-1203">支持从 ACR 检索凭据</span><span class="sxs-lookup"><span data-stu-id="fc76f-1203">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="fc76f-1204">删除 `appservice web` 下的所有命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1204">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="fc76f-1205">将命令输出中的 Docker 注册表密码掩码 (#3656)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1205">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="fc76f-1206">确保在 macOS 上使用默认浏览器且不出错 (#3623)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1206">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="fc76f-1207">改进了 `webapp log tail` 和 `webapp log download` 的帮助 (#3624)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1207">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="fc76f-1208">公开了 `traffic-routing` 命令用于配置静态路由 (#3566)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1208">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="fc76f-1209">添加了用于配置源代码管理的可靠性修复 (#3245)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1209">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="fc76f-1210">从 `webapp config update` 中删除了 Windows Web 应用不支持的 `--node-version` 参数。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1210">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="fc76f-1211">需改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1211">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="fc76f-1212">Batch</span><span class="sxs-lookup"><span data-stu-id="fc76f-1212">Batch</span></span>

* <span data-ttu-id="fc76f-1213">已更新到 Batch SDK 3.0.0，支持池中的低优先级 VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-1213">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="fc76f-1214">已将 `pool create` 选项 `--target-dedicated` 重命名为 `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1214">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="fc76f-1215">添加了 `pool create` 选项 `--target-low-priority-nodes` 和 `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1215">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="fc76f-1216">CDN</span><span class="sxs-lookup"><span data-stu-id="fc76f-1216">CDN</span></span>

* <span data-ttu-id="fc76f-1217">当 `--profile-name` 指定的配置文件不存在时，为 `cdn endpoint list` 提供更完善的错误消息</span><span class="sxs-lookup"><span data-stu-id="fc76f-1217">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="fc76f-1218">云</span><span class="sxs-lookup"><span data-stu-id="fc76f-1218">Cloud</span></span>

* <span data-ttu-id="fc76f-1219">已将云元数据终结点的 API 版本更改为 YYYY-MM-DD 格式</span><span class="sxs-lookup"><span data-stu-id="fc76f-1219">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="fc76f-1220">不需要库终结点</span><span class="sxs-lookup"><span data-stu-id="fc76f-1220">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="fc76f-1221">支持只将云注册到 ARM 资源管理器终结点</span><span class="sxs-lookup"><span data-stu-id="fc76f-1221">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="fc76f-1222">提供 `cloud set` 的选项用于在选择当前云时选择配置文件</span><span class="sxs-lookup"><span data-stu-id="fc76f-1222">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="fc76f-1223">公开了 `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1223">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="fc76f-1224">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="fc76f-1224">CosmosDB</span></span>

* <span data-ttu-id="fc76f-1225">修复了允许使用自定义分区键创建集合的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1225">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="fc76f-1226">添加了对集合默认 TTL 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1226">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="fc76f-1227">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="fc76f-1227">Data Lake Analytics</span></span>

* <span data-ttu-id="fc76f-1228">在 `dla account compute-policy` 标题下添加了用于计算策略管理的命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1228">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="fc76f-1229">添加了 `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1229">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="fc76f-1230">添加了 `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1230">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="fc76f-1231">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="fc76f-1231">Data Lake Store</span></span>

* <span data-ttu-id="fc76f-1232">在 `dls account update` 中添加了用户管理的 Key Vault 密钥轮换的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1232">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="fc76f-1233">更新了底层 Data Lake Store 文件系统 SDK 版本，解决了一个性能问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1233">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="fc76f-1234">添加了命令 `dls enable-key-vault`。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1234">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="fc76f-1235">此命令尝试使用用户提供的 Key Vault 加密 Data Lake Store 帐户中的数据</span><span class="sxs-lookup"><span data-stu-id="fc76f-1235">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="fc76f-1236">交互</span><span class="sxs-lookup"><span data-stu-id="fc76f-1236">Interactive</span></span>

* <span data-ttu-id="fc76f-1237">使用缓存的命令改进启动时间</span><span class="sxs-lookup"><span data-stu-id="fc76f-1237">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="fc76f-1238">增大了测试覆盖率</span><span class="sxs-lookup"><span data-stu-id="fc76f-1238">Increased test coverage</span></span>
* <span data-ttu-id="fc76f-1239">增强了“?”手势，使之也可注入到下一条命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1239">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="fc76f-1240">修复了配置文件 2017-03-09-profile-preview 的交互错误 (#3587)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1240">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="fc76f-1241">允许使用 `--version` 作为交互模式的参数 (#3645)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1241">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="fc76f-1242">阻止交互模式在验证填写内容中引发错误 (#3570)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1242">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="fc76f-1243">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1243">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="fc76f-1244">添加了 `--progress` 标志</span><span class="sxs-lookup"><span data-stu-id="fc76f-1244">Added `--progress` flag</span></span>
* <span data-ttu-id="fc76f-1245">从填写内容中删除了 `--debug` 和 `--verbose`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1245">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="fc76f-1246">从填写内容中删除了 `interactive` (#3324)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1246">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="fc76f-1247">IoT</span><span class="sxs-lookup"><span data-stu-id="fc76f-1247">IoT</span></span>

* <span data-ttu-id="fc76f-1248">修复了策略创建操作不再清除现有策略的问题。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1248">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="fc76f-1249">(#3934)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1249">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="fc76f-1250">密钥保管库</span><span class="sxs-lookup"><span data-stu-id="fc76f-1250">Key vault</span></span>

* <span data-ttu-id="fc76f-1251">添加了 Key Vault 恢复功能的命令：</span><span class="sxs-lookup"><span data-stu-id="fc76f-1251">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="fc76f-1252">`keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1252">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="fc76f-1253">`keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1253">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="fc76f-1254">`keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1254">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="fc76f-1255">`keyvault key` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1255">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="fc76f-1256">添加了服务主体的 Key Vault 集成 (#3133)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1256">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="fc76f-1257">已将 Key Vault 数据平面更新到 0.3.2。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1257">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="fc76f-1258">(#3307)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1258">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="fc76f-1259">实验室</span><span class="sxs-lookup"><span data-stu-id="fc76f-1259">Lab</span></span>

* <span data-ttu-id="fc76f-1260">添加了通过 `az lab vm claim` 在实验室中声明任何 VM 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1260">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="fc76f-1261">为 `az lab vm list` 和 `az lab vm show` 添加了表输出格式化程序</span><span class="sxs-lookup"><span data-stu-id="fc76f-1261">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="fc76f-1262">监视</span><span class="sxs-lookup"><span data-stu-id="fc76f-1262">Monitor</span></span>

* <span data-ttu-id="fc76f-1263">修复了与 `monitor autoscale-settings get-parameters-template` 命令结合使用的模板文件 (#3349)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1263">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="fc76f-1264">已将 `monitor alert-rule-incidents list` 重命名为 `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1264">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="fc76f-1265">已将 `monitor alert-rule-incidents show` 重命名为 `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1265">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="fc76f-1266">已将 `monitor metric-defintions list` 重命名为 `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1266">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="fc76f-1267">已将 `monitor alert-rules` 重命名为 `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1267">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="fc76f-1268">更改了 `monitor alert create`：</span><span class="sxs-lookup"><span data-stu-id="fc76f-1268">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="fc76f-1269">`condition` 和 `action` 子命令不再接受 JSON</span><span class="sxs-lookup"><span data-stu-id="fc76f-1269">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="fc76f-1270">添加了大量的参数来简化规则创建过程</span><span class="sxs-lookup"><span data-stu-id="fc76f-1270">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="fc76f-1271">`location` 不再是必需的</span><span class="sxs-lookup"><span data-stu-id="fc76f-1271">`location` no longer required</span></span>
  * <span data-ttu-id="fc76f-1272">添加了目标的名称和 ID 支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1272">Add name and ID support for target</span></span>
  * <span data-ttu-id="fc76f-1273">删除了 `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1273">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="fc76f-1274">`is-enabled` 重命名为 `enabled`，不再是必需的</span><span class="sxs-lookup"><span data-stu-id="fc76f-1274">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="fc76f-1275">`description` 默认值现在基于提供的条件</span><span class="sxs-lookup"><span data-stu-id="fc76f-1275">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="fc76f-1276">添加了示例用于帮助澄清新格式</span><span class="sxs-lookup"><span data-stu-id="fc76f-1276">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="fc76f-1277">支持在 `monitor metric` 命令中使用名称或 ID</span><span class="sxs-lookup"><span data-stu-id="fc76f-1277">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="fc76f-1278">为 `monitor alert rule update` 添加了方便的参数和示例</span><span class="sxs-lookup"><span data-stu-id="fc76f-1278">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-1279">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-1279">Network</span></span>

* <span data-ttu-id="fc76f-1280">添加了 `list-private-access-services` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1280">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="fc76f-1281">为 `vnet subnet create` 和 `vnet subnet update` 添加了 `--private-access-services` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1281">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="fc76f-1282">修复了 `application-gateway redirect-config create` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1282">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="fc76f-1283">修复了无法结合 `--no-wait` 使用 `application-gateway redirect-config update` 的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1283">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="fc76f-1284">修复了结合 `application-gateway address-pool create` 和 `application-gateway address-pool update` 使用 `--servers` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1284">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="fc76f-1285">添加了 `application-gateway redirect-config` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1285">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="fc76f-1286">添加了 `application-gateway ssl-policy` 的命令：`list-options`、`predefined list`、`predefined show`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1286">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="fc76f-1287">添加了 `application-gateway ssl-policy set` 的参数：`--name`、`--cipher-suites`、`--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1287">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="fc76f-1288">添加了 `application-gateway http-settings create` 和 `application-gateway http-settings update` 的参数：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1288">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="fc76f-1289">添加了 `application-gateway url-path-map create` 和 `application-gateway url-path-map update` 的参数：`--default-redirect-config`、`--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1289">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="fc76f-1290">为 `application-gateway url-path-map rule create` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1290">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="fc76f-1291">在 `application-gateway url-path-map rule delete` 中添加了对 `--no-wait` 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1291">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="fc76f-1292">添加了 `application-gateway probe create` 和 `application-gateway probe update` 的参数：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1292">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="fc76f-1293">为 `application-gateway rule create` 和 `application-gateway rule update` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1293">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="fc76f-1294">在 `nic create` 和 `nic update` 中添加了对 `--accelerated-networking` 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1294">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="fc76f-1295">从 `nic create` 中删除了 `--internal-dns-name-suffix` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1295">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="fc76f-1296">在 `nic update` 和 `nic create` 中添加了对 `--dns-servers` 的支持：添加了对 --dns-servers 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1296">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="fc76f-1297">修复了 `local-gateway create` 忽略 `--local-address-prefixes` 的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1297">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="fc76f-1298">在 `vnet update` 中添加了对 `--dns-servers` 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1298">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="fc76f-1299">修复了使用 `express-route peering create` 创建不包含路由筛选的对等互连时的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1299">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="fc76f-1300">修复了无法结合 `--provider` 和 `--bandwidth` 参数使用 `express-route update` 的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1300">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="fc76f-1301">修复了 `network watcher show-topology` 默认逻辑的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1301">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="fc76f-1302">改进了 `network list-usages` 的输出格式</span><span class="sxs-lookup"><span data-stu-id="fc76f-1302">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="fc76f-1303">如果只存在一个，则对 `application-gateway http-listener create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="fc76f-1303">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="fc76f-1304">如果只存在一个，则对 `application-gateway rule create` 使用默认地址池、HTTP 设置和 HTTP 侦听器</span><span class="sxs-lookup"><span data-stu-id="fc76f-1304">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="fc76f-1305">如果只存在一个，则对 `lb rule create` 使用默认前端 IP 和后端池</span><span class="sxs-lookup"><span data-stu-id="fc76f-1305">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="fc76f-1306">如果只存在一个，则对 `lb inbound-nat-rule create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="fc76f-1306">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="fc76f-1307">配置文件</span><span class="sxs-lookup"><span data-stu-id="fc76f-1307">Profile</span></span>

* <span data-ttu-id="fc76f-1308">支持使用托管标识在 VM 内部登录</span><span class="sxs-lookup"><span data-stu-id="fc76f-1308">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="fc76f-1309">支持采用 SDK 身份验证文件格式的 `account show` 输出</span><span class="sxs-lookup"><span data-stu-id="fc76f-1309">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="fc76f-1310">使用 '--expanded-view' 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="fc76f-1310">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="fc76f-1311">添加了 `get-access-token` 命令来提供原始 AAD 令牌</span><span class="sxs-lookup"><span data-stu-id="fc76f-1311">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="fc76f-1312">支持使用不包含关联订阅的用户帐户登录</span><span class="sxs-lookup"><span data-stu-id="fc76f-1312">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="fc76f-1313">RDBMS</span><span class="sxs-lookup"><span data-stu-id="fc76f-1313">RDBMS</span></span>

* <span data-ttu-id="fc76f-1314">支持跨订阅列出服务器 (#3417)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1314">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="fc76f-1315">修复了由于缺少 `% server_type` 而不处理 `%s` 的问题 (#3393)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1315">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="fc76f-1316">修复了文档源映射并添加了 CI 任务用于验证 (#3361)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1316">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="fc76f-1317">修复了 MySQL 和 PostgreSQL 帮助 (#3369)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1317">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="fc76f-1318">资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-1318">Resource</span></span>

* <span data-ttu-id="fc76f-1319">改进了有关 `group deployment create` 缺少参数的提示</span><span class="sxs-lookup"><span data-stu-id="fc76f-1319">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="fc76f-1320">改进了 `--parameters KEY=VALUE` 语法分析</span><span class="sxs-lookup"><span data-stu-id="fc76f-1320">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="fc76f-1321">修复了不再能够使用 `@<file>` 语法识别 `group deployment create` 参数文件的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1321">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="fc76f-1322">支持 `resource` 和 `managedapp` 命令的 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1322">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="fc76f-1323">修复了一些分析和错误消息 (#3584)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1323">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="fc76f-1324">修复了 `lock` 命令的 `--resource-type` 分析，接受 `<resource-namespace>` 和 `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1324">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="fc76f-1325">添加了模板链接模板的参数检查 (#3629)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1325">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="fc76f-1326">添加了使用 `KEY=VALUE` 语法指定部署参数的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1326">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="fc76f-1327">角色</span><span class="sxs-lookup"><span data-stu-id="fc76f-1327">Role</span></span>

* <span data-ttu-id="fc76f-1328">支持采用 SDK 身份验证文件格式的 `create-for-rbac` 输出</span><span class="sxs-lookup"><span data-stu-id="fc76f-1328">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="fc76f-1329">删除服务主体时清理角色分配和相关的 AAD 应用程序 (#3610)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1329">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="fc76f-1330">在 `app create` 参数 `--start-date` 和 `--end-date` 说明中包含时间格式</span><span class="sxs-lookup"><span data-stu-id="fc76f-1330">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="fc76f-1331">使用 `--expanded-view` 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="fc76f-1331">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="fc76f-1332">在 `create-for-rbac` 和 `reset-credentials` 命令中添加了 Key Vault 集成</span><span class="sxs-lookup"><span data-stu-id="fc76f-1332">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="fc76f-1333">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="fc76f-1333">Service Fabric</span></span>
* <span data-ttu-id="fc76f-1334">修复了上传时截断应用程序中的大型文件的问题 (#3666)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1334">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="fc76f-1335">添加了 Service Fabric 命令的测试 (#3424)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1335">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="fc76f-1336">添加了大量的 Service Fabric 命令 (#3234)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1336">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="fc76f-1337">SQL</span><span class="sxs-lookup"><span data-stu-id="fc76f-1337">SQL</span></span>

* <span data-ttu-id="fc76f-1338">删除了无效的 `sql server create` `--identity` 参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1338">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="fc76f-1339">从 `sql server create` 和 `sql server update` 命令输出中删除了密码值</span><span class="sxs-lookup"><span data-stu-id="fc76f-1339">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="fc76f-1340">添加了命令 `sql db list-editions` 和 `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1340">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-1341">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-1341">Storage</span></span>

* <span data-ttu-id="fc76f-1342">从 `storage blob list`、`storage container list` 和 `storage share list` 命令中删除了 `--marker` 选项 (#3745)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1342">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="fc76f-1343">启用了创建仅限 https 的存储帐户</span><span class="sxs-lookup"><span data-stu-id="fc76f-1343">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="fc76f-1344">更新了存储指标、日志记录和 CORS 命令 (#3495)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1344">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="fc76f-1345">重新编写了 CORS add 命令的异常消息 (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1345">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="fc76f-1346">已在下载批处理命令试运行模式下将生成器转换为列表 (#3592)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1346">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="fc76f-1347">修复了 Blob 下载批处理试运行问题 (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1347">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-1348">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-1348">VM</span></span>

* <span data-ttu-id="fc76f-1349">支持配置 NSG</span><span class="sxs-lookup"><span data-stu-id="fc76f-1349">Support configuring nsg</span></span>
* <span data-ttu-id="fc76f-1350">修复了无法正确配置 DNS 服务器的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1350">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="fc76f-1351">支持托管服务标识</span><span class="sxs-lookup"><span data-stu-id="fc76f-1351">Support managed service identities</span></span>
* <span data-ttu-id="fc76f-1352">修复了包含现有负载均衡器的 `cmss create` 需要 `--backend-pool-name` 的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1352">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="fc76f-1353">要求使用 `vm image create` LUN 创建的数据磁盘以 0 开头</span><span class="sxs-lookup"><span data-stu-id="fc76f-1353">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="fc76f-1354">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-1354">May 10, 2017</span></span>

<span data-ttu-id="fc76f-1355">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="fc76f-1355">Version 2.0.6</span></span>

* <span data-ttu-id="fc76f-1356">Documentdb 已重命名为 Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="fc76f-1356">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="fc76f-1357">添加 rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1357">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="fc76f-1358">包括 Data Lake Analytics 和 Data Lake Store 模块</span><span class="sxs-lookup"><span data-stu-id="fc76f-1358">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="fc76f-1359">包括认知服务模块</span><span class="sxs-lookup"><span data-stu-id="fc76f-1359">Include Cognitive Services module</span></span>
* <span data-ttu-id="fc76f-1360">包括 Service Fabric 模块</span><span class="sxs-lookup"><span data-stu-id="fc76f-1360">Include Service Fabric module</span></span>
* <span data-ttu-id="fc76f-1361">包括交互式模块（重命名 az-shell）</span><span class="sxs-lookup"><span data-stu-id="fc76f-1361">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="fc76f-1362">添加对 CDN 命令的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1362">Add support for CDN commands</span></span>
* <span data-ttu-id="fc76f-1363">删除容器模块</span><span class="sxs-lookup"><span data-stu-id="fc76f-1363">Remove Container module</span></span>
* <span data-ttu-id="fc76f-1364">添加“az -v”作为“az --version”的快捷方式 ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1364">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="fc76f-1365">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1365">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="fc76f-1366">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-1366">Core</span></span>

* <span data-ttu-id="fc76f-1367">核心：捕获未注册提供程序引发的异常并自动注册</span><span class="sxs-lookup"><span data-stu-id="fc76f-1367">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="fc76f-1368">性能：将 ADAL 令牌缓存保留在内存中，直至进程退出 ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1368">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="fc76f-1369">修复从十六进制指纹 -o tsv 返回的字节 ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1369">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="fc76f-1370">改进的 Key Vault 证书下载和 AAD SP 集成 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1370">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="fc76f-1371">将 Python 位置添加到“az —version”([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1371">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="fc76f-1372">登录：无订阅时支持登录 ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1372">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="fc76f-1373">核心：修复重复使用服务主体登录时出现的故障 ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1373">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="fc76f-1374">核心：允许通过 env var 配置 accessTokens.json 的文件路径 ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1374">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="fc76f-1375">核心：允许配置的默认值应用于可选参数 ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1375">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="fc76f-1376">核心：提高了性能</span><span class="sxs-lookup"><span data-stu-id="fc76f-1376">core: Improved performance</span></span>
* <span data-ttu-id="fc76f-1377">核心：自定义 CA 证书 - 支持设置 REQUESTS_CA_BUNDLE 环境变量</span><span class="sxs-lookup"><span data-stu-id="fc76f-1377">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="fc76f-1378">核心：云配置 - 如果未设置“management”终结点，则使用“resource manager”终结点</span><span class="sxs-lookup"><span data-stu-id="fc76f-1378">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-1379">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-1379">ACS</span></span>

* <span data-ttu-id="fc76f-1380">将主计数和代理计数修复为整数而不是字符串</span><span class="sxs-lookup"><span data-stu-id="fc76f-1380">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="fc76f-1381">公开“az acs create --no-wait”和“az acs wait”用于异步创建</span><span class="sxs-lookup"><span data-stu-id="fc76f-1381">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="fc76f-1382">公开“az acs create --validate”用于试运行验证</span><span class="sxs-lookup"><span data-stu-id="fc76f-1382">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="fc76f-1383">在 PUT 调用 scale 命令前删除 Windows 配置文件 ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1383">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-1384">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-1384">AppService</span></span>

* <span data-ttu-id="fc76f-1385">Function App：添加完整的 Function App 支持，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="fc76f-1385">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="fc76f-1386">将 Team Services (vsts) 作为持续交付选项添加到“appservice web source-control config”</span><span class="sxs-lookup"><span data-stu-id="fc76f-1386">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="fc76f-1387">创建“az webapp”以替换“az appservice web”（为了向后兼容，“az appservice web”将保留 2 个版本）</span><span class="sxs-lookup"><span data-stu-id="fc76f-1387">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="fc76f-1388">公开参数以针对 webapp create 配置部署和“运行时堆栈”</span><span class="sxs-lookup"><span data-stu-id="fc76f-1388">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="fc76f-1389">公开“webapp list-runtimes”</span><span class="sxs-lookup"><span data-stu-id="fc76f-1389">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="fc76f-1390">支持配置连接字符串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1390">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="fc76f-1391">支持与预览版交换槽</span><span class="sxs-lookup"><span data-stu-id="fc76f-1391">support slot swap with preview</span></span>
* <span data-ttu-id="fc76f-1392">修改 appservice 命令的错误 ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1392">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="fc76f-1393">将应用服务计划的资源组用于证书操作 ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1393">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="fc76f-1394">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="fc76f-1394">CosmosDB</span></span>

* <span data-ttu-id="fc76f-1395">将 documentdb 模块重命名为 cosmosdb</span><span class="sxs-lookup"><span data-stu-id="fc76f-1395">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="fc76f-1396">增加对 DocumentDB 数据平面 API 的支持：数据库和集合管理</span><span class="sxs-lookup"><span data-stu-id="fc76f-1396">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="fc76f-1397">增加对数据库帐户启用自动故障转移的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1397">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="fc76f-1398">增加对新一致性策略 ConsistentPrefix 的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1398">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="fc76f-1399">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="fc76f-1399">Data Lake Analytics</span></span>

* <span data-ttu-id="fc76f-1400">修复了在筛选作业结果和状态列表时会引发错误的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1400">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="fc76f-1401">增加对新目录项类型的支持：包。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1401">Add support for new catalog item type: package.</span></span> <span data-ttu-id="fc76f-1402">访问方法：`az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="fc76f-1402">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="fc76f-1403">可从数据库内列出下列目录项（无需架构规范）：</span><span class="sxs-lookup"><span data-stu-id="fc76f-1403">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="fc76f-1404">表</span><span class="sxs-lookup"><span data-stu-id="fc76f-1404">Table</span></span>
  * <span data-ttu-id="fc76f-1405">表值函数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1405">Table valued function</span></span>
  * <span data-ttu-id="fc76f-1406">查看</span><span class="sxs-lookup"><span data-stu-id="fc76f-1406">View</span></span>
  * <span data-ttu-id="fc76f-1407">表统计信息。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1407">Table Statistics.</span></span> <span data-ttu-id="fc76f-1408">这也可以使用架构（但无需指定表名）列出</span><span class="sxs-lookup"><span data-stu-id="fc76f-1408">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="fc76f-1409">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="fc76f-1409">Data Lake Store</span></span>

* <span data-ttu-id="fc76f-1410">更新基础文件系统 SDK 的版本，以便为处理服务器端限制场景提供更好的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1410">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="fc76f-1411">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1411">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="fc76f-1412">访问显示帮助丢失。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1412">missed help for access show.</span></span> <span data-ttu-id="fc76f-1413">正在添加。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1413">adding it.</span></span> <span data-ttu-id="fc76f-1414">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1414">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="fc76f-1415">查找</span><span class="sxs-lookup"><span data-stu-id="fc76f-1415">Find</span></span>

* <span data-ttu-id="fc76f-1416">改进搜索结果，允许搜索索引的版本控制</span><span class="sxs-lookup"><span data-stu-id="fc76f-1416">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="fc76f-1417">KeyVault</span><span class="sxs-lookup"><span data-stu-id="fc76f-1417">KeyVault</span></span>

* <span data-ttu-id="fc76f-1418">BC：`az keyvault certificate download` 将 -e 从字符串或二进制更改为 PEM 或 DER，从而更好地表示选项</span><span class="sxs-lookup"><span data-stu-id="fc76f-1418">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="fc76f-1419">BC：从 `keyvault certificate create` 删除 --expires 和 --not-before，因为此服务不支持这些参数</span><span class="sxs-lookup"><span data-stu-id="fc76f-1419">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="fc76f-1420">将 --validity 参数添加到 `keyvault certificate create`，有选择地替代 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="fc76f-1420">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="fc76f-1421">修复了 `keyvault certificate get-default-policy` 中已公开“expires”和“not_before”但未公开“validity_in_months”的问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1421">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="fc76f-1422">KeyVault 解决了 pem 和 pfx 的导入问题 ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1422">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="fc76f-1423">实验室</span><span class="sxs-lookup"><span data-stu-id="fc76f-1423">Lab</span></span>

* <span data-ttu-id="fc76f-1424">为实验室中的环境添加 create、show、delete 和 list 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1424">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="fc76f-1425">添加 show 和 list 命令以查看实验室中的 ARM 模板</span><span class="sxs-lookup"><span data-stu-id="fc76f-1425">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="fc76f-1426">在 `az lab vm list` 中添加 --environment 标志，以便按实验室中的环境筛选 VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-1426">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="fc76f-1427">添加方便命令 `az lab formula export-artifacts`，以便导出实验室公式中的项目基架</span><span class="sxs-lookup"><span data-stu-id="fc76f-1427">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="fc76f-1428">添加命令以管理实验室中的机密</span><span class="sxs-lookup"><span data-stu-id="fc76f-1428">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="fc76f-1429">监视</span><span class="sxs-lookup"><span data-stu-id="fc76f-1429">Monitor</span></span>

* <span data-ttu-id="fc76f-1430">Bug 修复：为 `az alert-rules create` 的 `--actions` 建模，以使用 JSON 字符串 ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1430">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="fc76f-1431">Bug 修复 - diagnostic settings create 不接受来自 show 命令的日志/指标 ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1431">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="fc76f-1432">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-1432">Network</span></span>

* <span data-ttu-id="fc76f-1433">添加 `network watcher test-connectivity` 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1433">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="fc76f-1434">为 `network watcher packet-capture create` 添加对 `--filters` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1434">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="fc76f-1435">添加对应用程序网关连接排出的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1435">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="fc76f-1436">添加对应用程序网关 WAF 规则集配置的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1436">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="fc76f-1437">添加对 ExpressRoute 路由筛选器和规则的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1437">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="fc76f-1438">添加对 TrafficManager 地理路由的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1438">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="fc76f-1439">添加对基于 VPN 连接策略的流量选择器的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1439">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="fc76f-1440">添加对 VPN 连接 IPSec 策略的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1440">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="fc76f-1441">修复使用 `--no-wait` 或 `--validate` 参数时 `vpn-connection create` 出现的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1441">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="fc76f-1442">添加对主动-主动 VNet 网关的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1442">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="fc76f-1443">从 `network vpn-connection list/show` 命令的输出中删除 null 值</span><span class="sxs-lookup"><span data-stu-id="fc76f-1443">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="fc76f-1444">BC：修复 `vpn-connection create` 输出中的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1444">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="fc76f-1445">修复无法正确分析“vpn-connection create”的“--key-length”参数的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1445">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="fc76f-1446">修复 `dns zone import` 中无法正确导入记录的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1446">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="fc76f-1447">修复 `traffic-manager endpoint update` 不起作用的 bug</span><span class="sxs-lookup"><span data-stu-id="fc76f-1447">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="fc76f-1448">添加“network watcher”预览命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1448">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="fc76f-1449">配置文件</span><span class="sxs-lookup"><span data-stu-id="fc76f-1449">Profile</span></span>

* <span data-ttu-id="fc76f-1450">支持在未找到订阅时登录 ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1450">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="fc76f-1451">支持在 az account set --subscription 中使用短参数名 ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1451">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="fc76f-1452">Redis</span><span class="sxs-lookup"><span data-stu-id="fc76f-1452">Redis</span></span>

* <span data-ttu-id="fc76f-1453">添加 update 命令，也增加了对 redis 缓存进行缩放的功能</span><span class="sxs-lookup"><span data-stu-id="fc76f-1453">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="fc76f-1454">弃用“update-settings”命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1454">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="fc76f-1455">资源</span><span class="sxs-lookup"><span data-stu-id="fc76f-1455">Resource</span></span>

* <span data-ttu-id="fc76f-1456">添加 managedapp 和 managedapp 定义命令 ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1456">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="fc76f-1457">支持“provider operation”命令([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1457">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="fc76f-1458">支持 generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1458">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="fc76f-1459">修复资源分析和 API 版本查找。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1459">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="fc76f-1460">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1460">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="fc76f-1461">为 az lock update 添加文档。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1461">Add docs for az lock update.</span></span> <span data-ttu-id="fc76f-1462">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1462">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="fc76f-1463">尝试为不存在的组列出资源时出错。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1463">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="fc76f-1464">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1464">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="fc76f-1465">[计算] 修复 VMSS 和 VM 可用性集更新的相关问题。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1465">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="fc76f-1466">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1466">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="fc76f-1467">parent-resource-path 为 None 时修复 lock create 和 delete ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1467">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="fc76f-1468">角色</span><span class="sxs-lookup"><span data-stu-id="fc76f-1468">Role</span></span>

* <span data-ttu-id="fc76f-1469">create-for-rbac：确保 SP 的结束日期不超过证书的到期日期 ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1469">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="fc76f-1470">RBAC：添加对“ad group”的完整支持 ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1470">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="fc76f-1471">role：解决角色定义更新的相关问题 ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1471">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="fc76f-1472">create-for-rbac：确保已选取用户提供的密码</span><span class="sxs-lookup"><span data-stu-id="fc76f-1472">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="fc76f-1473">SQL</span><span class="sxs-lookup"><span data-stu-id="fc76f-1473">SQL</span></span>

* <span data-ttu-id="fc76f-1474">添加了 az sql server list-usages 和 az sql db list-usages 命令</span><span class="sxs-lookup"><span data-stu-id="fc76f-1474">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="fc76f-1475">SQL - 能够直接连接到资源提供程序 ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1475">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="fc76f-1476">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-1476">Storage</span></span>

* <span data-ttu-id="fc76f-1477">对于 `storage account create`，将位置默认为资源组位置</span><span class="sxs-lookup"><span data-stu-id="fc76f-1477">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="fc76f-1478">添加对增量 blob 复制的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1478">Add support for incremental blob copy</span></span>
* <span data-ttu-id="fc76f-1479">添加对大型块 blob 上传的支持</span><span class="sxs-lookup"><span data-stu-id="fc76f-1479">Add support for large block blob upload</span></span>
* <span data-ttu-id="fc76f-1480">如果要上传的文件大于 200GB，则将块大小更改为 100MB</span><span class="sxs-lookup"><span data-stu-id="fc76f-1480">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-1481">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-1481">VM</span></span>

* <span data-ttu-id="fc76f-1482">avail-set：将 UD 和 FD 域计数设为可选</span><span class="sxs-lookup"><span data-stu-id="fc76f-1482">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="fc76f-1483">注意：最高等级云中的 VM 命令。请避免与托管磁盘相关的功能，包括以下项：</span><span class="sxs-lookup"><span data-stu-id="fc76f-1483">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="fc76f-1484">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="fc76f-1484">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="fc76f-1485">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="fc76f-1485">az vm/vmss disk</span></span>
  3. <span data-ttu-id="fc76f-1486">在“az vm/vmss create”内，使用“—use-unmanaged-disk”避免托管磁盘 其他命令应有效</span><span class="sxs-lookup"><span data-stu-id="fc76f-1486">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="fc76f-1487">vm/vmss：改进生成 SSH 密钥对时的警告文本</span><span class="sxs-lookup"><span data-stu-id="fc76f-1487">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="fc76f-1488">vm/vmss：支持通过需要计划信息的市场映像创建 ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1488">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="fc76f-1489">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-1489">April 3, 2017</span></span>

<span data-ttu-id="fc76f-1490">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="fc76f-1490">Version 2.0.2</span></span>

<span data-ttu-id="fc76f-1491">此版本中已发布 ACR、Batch、KeyVault 和 SQL 组件</span><span class="sxs-lookup"><span data-stu-id="fc76f-1491">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="fc76f-1492">核心</span><span class="sxs-lookup"><span data-stu-id="fc76f-1492">Core</span></span>

* <span data-ttu-id="fc76f-1493">在默认列表中添加了 acr、lab、monitor 和 find 模块</span><span class="sxs-lookup"><span data-stu-id="fc76f-1493">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="fc76f-1494">登录：跳过错误的租户 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1494">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="fc76f-1495">登录：将默认订阅设置为处于“已启用”状态的订阅 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1495">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="fc76f-1496">添加了 wait 命令，并添加了对其他命令的 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1496">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="fc76f-1497">核心：支持结合证书使用服务主体登录 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1497">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="fc76f-1498">添加了有关缺少模板参数的提示。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1498">Add prompting for missing template parameters.</span></span> <span data-ttu-id="fc76f-1499">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1499">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="fc76f-1500">支持为资源组、默认 Web、 默认 VM 等常见参数设置默认值</span><span class="sxs-lookup"><span data-stu-id="fc76f-1500">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="fc76f-1501">支持登录到特定的租户</span><span class="sxs-lookup"><span data-stu-id="fc76f-1501">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="fc76f-1502">ACS</span><span class="sxs-lookup"><span data-stu-id="fc76f-1502">ACS</span></span>

* <span data-ttu-id="fc76f-1503">[ACS] 添加了配置默认 ACS 群集的支持 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1503">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="fc76f-1504">添加了 SSH 密钥密码提示的支持。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1504">Add support for ssh key password prompting.</span></span> <span data-ttu-id="fc76f-1505">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1505">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="fc76f-1506">添加了对 Windows 群集的支持。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1506">Add support for windows clusters.</span></span> <span data-ttu-id="fc76f-1507">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1507">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="fc76f-1508">从“所有者”角色切换到“参与者”角色。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1508">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="fc76f-1509">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1509">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="fc76f-1510">应用服务</span><span class="sxs-lookup"><span data-stu-id="fc76f-1510">AppService</span></span>

* <span data-ttu-id="fc76f-1511">应用服务：支持获取用于 DNS A 记录的外部 IP 地址 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1511">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="fc76f-1512">应用服务：支持绑定通配符证书 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1512">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="fc76f-1513">应用服务：支持列出发布配置文件 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1513">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="fc76f-1514">应用服务 - 配置后触发源代码管理同步 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1514">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="fc76f-1515">DataLake</span><span class="sxs-lookup"><span data-stu-id="fc76f-1515">DataLake</span></span>

* <span data-ttu-id="fc76f-1516">Data Lake Analytics 模块的初始版本</span><span class="sxs-lookup"><span data-stu-id="fc76f-1516">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="fc76f-1517">Data Lake Store 模块的初始版本</span><span class="sxs-lookup"><span data-stu-id="fc76f-1517">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="fc76f-1518">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="fc76f-1518">DocuemntDB</span></span>

* <span data-ttu-id="fc76f-1519">DocumentDB：添加了列出连接字符串的支持 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1519">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="fc76f-1520">VM</span><span class="sxs-lookup"><span data-stu-id="fc76f-1520">VM</span></span>

* <span data-ttu-id="fc76f-1521">[计算] 添加了用于创建虚拟机规模集的应用网关支持 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1521">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="fc76f-1522">[VM/VMSS] 改进了磁盘缓存支持 ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1522">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="fc76f-1523">VM/VMSS：合并了门户使用的凭据验证逻辑 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1523">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="fc76f-1524">添加了 wait 命令和 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1524">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="fc76f-1525">虚拟机规模集：支持使用 \* 列出不同 VM 上的实例视图 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1525">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="fc76f-1526">为 VM 和虚拟机规模集添加了 --secrets ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1526">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="fc76f-1527">允许使用专用 VHD 创建 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="fc76f-1527">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="fc76f-1528">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="fc76f-1528">February 27, 2017</span></span>

<span data-ttu-id="fc76f-1529">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="fc76f-1529">Version 2.0.0</span></span>

<span data-ttu-id="fc76f-1530">此 Azure CLI 2.0 发布版是第一个“正式版”。正式版适用于以下命令模块：</span><span class="sxs-lookup"><span data-stu-id="fc76f-1530">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="fc76f-1531">容器服务 (ACS)</span><span class="sxs-lookup"><span data-stu-id="fc76f-1531">Container Service (acs)</span></span>
- <span data-ttu-id="fc76f-1532">计算（包括 Resource Manager、VM、虚拟机规模集、托管磁盘）</span><span class="sxs-lookup"><span data-stu-id="fc76f-1532">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="fc76f-1533">网络</span><span class="sxs-lookup"><span data-stu-id="fc76f-1533">Networking</span></span>
- <span data-ttu-id="fc76f-1534">存储</span><span class="sxs-lookup"><span data-stu-id="fc76f-1534">Storage</span></span>

<span data-ttu-id="fc76f-1535">这些命令模块可在生产中使用，并且受标准 Microsoft SLA 支持。可以直接通过 Microsoft 支持部门创建问题，也可以在我们的 [github 问题列表](https://github.com/azure/azure-cli/issues/)中创建问题。可以[使用 azure-cli 标记在 StackOverflow 上](http://stackoverflow.com/questions/tagged/azure-cli)提问，也可以通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队。可以从命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1535">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="fc76f-1536">这些模块中的命令非常稳定，其语法在此 Azure CLI 版本即将到来的发行版中预期不会变化。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1536">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="fc76f-1537">若要验证 CLI 的版本，请使用 `az --version`。输出中将列出 CLI 本身的版本（在此发行版中为 2.0.0）、各个命令模块的版本，以及所用 Python 和 GCC 的版本。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1537">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="fc76f-1538">其中的一些命令模块有“b*n*”或“rc*n*”后缀。这些命令模块仍在预览版中提供，将来会发布正式版。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1538">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="fc76f-1539">此外，我们还提供 CLI 夜间预览版。有关信息，请参阅有关[获取夜间预览版](https://github.com/Azure/azure-cli#nightly-builds)的说明，以及有关[开发人员设置与贡献代码](https://github.com/Azure/azure-cli#developer-setup)的说明。</span><span class="sxs-lookup"><span data-stu-id="fc76f-1539">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="fc76f-1540">可通过以下方式报告夜间预览版的问题：</span><span class="sxs-lookup"><span data-stu-id="fc76f-1540">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="fc76f-1541">在 [github 问题列表](https://github.com/azure/azure-cli/issues/)中报告问题</span><span class="sxs-lookup"><span data-stu-id="fc76f-1541">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="fc76f-1542">通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队</span><span class="sxs-lookup"><span data-stu-id="fc76f-1542">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="fc76f-1543">通过命令行使用 `az feedback` 命令提供反馈</span><span class="sxs-lookup"><span data-stu-id="fc76f-1543">Provide feedback from the command line with the `az feedback` command</span></span>

