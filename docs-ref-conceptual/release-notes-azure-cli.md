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
ms.openlocfilehash: 39e4710a29ac57730919b82ab76b9c9a4b9ca786
ms.sourcegitcommit: 43d4f838d132ab9bcfa59dbda3b544c06373b6a9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="a211d-104">Azure CLI 2.0 发行说明</span><span class="sxs-lookup"><span data-stu-id="a211d-104">Azure CLI 2.0 release notes</span></span>

## <a name="august-15-2017"></a><span data-ttu-id="a211d-105">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a211d-105">August 15, 2017</span></span>

<span data-ttu-id="a211d-106">版本 2.0.14</span><span class="sxs-lookup"><span data-stu-id="a211d-106">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="a211d-107">ACS</span><span class="sxs-lookup"><span data-stu-id="a211d-107">ACS</span></span>

* <span data-ttu-id="a211d-108">更正了 kubernetes 的 sshMaster0 端口号</span><span class="sxs-lookup"><span data-stu-id="a211d-108">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="a211d-109">应用服务</span><span class="sxs-lookup"><span data-stu-id="a211d-109">Appservice</span></span>

* <span data-ttu-id="a211d-110">修复了创建基于新 Git 的 Linux Web 应用时发生异常的问题</span><span class="sxs-lookup"><span data-stu-id="a211d-110">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="a211d-111">事件网格</span><span class="sxs-lookup"><span data-stu-id="a211d-111">Event Grid</span></span>

* <span data-ttu-id="a211d-112">添加了 SDK 依赖项</span><span class="sxs-lookup"><span data-stu-id="a211d-112">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="a211d-113">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="a211d-113">August 11, 2017</span></span>

<span data-ttu-id="a211d-114">版本 2.0.13</span><span class="sxs-lookup"><span data-stu-id="a211d-114">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="a211d-115">ACS</span><span class="sxs-lookup"><span data-stu-id="a211d-115">ACS</span></span>

* <span data-ttu-id="a211d-116">添加了更多预览区域</span><span class="sxs-lookup"><span data-stu-id="a211d-116">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="a211d-117">批处理</span><span class="sxs-lookup"><span data-stu-id="a211d-117">Batch</span></span>

* <span data-ttu-id="a211d-118">已更新到 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="a211d-118">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="a211d-119">添加了新命令用于显示作业的任务计数</span><span class="sxs-lookup"><span data-stu-id="a211d-119">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="a211d-120">修复了处理资源文件 SAS URL 时的 bug</span><span class="sxs-lookup"><span data-stu-id="a211d-120">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="a211d-121">Batch 帐户终结点现在支持可选的“https://”前缀</span><span class="sxs-lookup"><span data-stu-id="a211d-121">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="a211d-122">支持将包含 100 多个任务的列表添加到作业</span><span class="sxs-lookup"><span data-stu-id="a211d-122">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="a211d-123">添加了加载扩展命令模块的调试日志记录</span><span class="sxs-lookup"><span data-stu-id="a211d-123">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="a211d-124">组件</span><span class="sxs-lookup"><span data-stu-id="a211d-124">Component</span></span>

* <span data-ttu-id="a211d-125">为“az component”命令添加了弃用警告</span><span class="sxs-lookup"><span data-stu-id="a211d-125">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="a211d-126">容器</span><span class="sxs-lookup"><span data-stu-id="a211d-126">Container</span></span>

* <span data-ttu-id="a211d-127">`create`：修复了某个环境变量中不允许等于号的问题</span><span class="sxs-lookup"><span data-stu-id="a211d-127">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="a211d-128">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="a211d-128">Data Lake Store</span></span>

* <span data-ttu-id="a211d-129">启用了进度控件</span><span class="sxs-lookup"><span data-stu-id="a211d-129">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="a211d-130">事件网格</span><span class="sxs-lookup"><span data-stu-id="a211d-130">Event Grid</span></span>

* <span data-ttu-id="a211d-131">初始版本</span><span class="sxs-lookup"><span data-stu-id="a211d-131">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="a211d-132">网络</span><span class="sxs-lookup"><span data-stu-id="a211d-132">Network</span></span>

* <span data-ttu-id="a211d-133">`lb`：修复了某些子资源名称在省略时无法正确解析的问题</span><span class="sxs-lookup"><span data-stu-id="a211d-133">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="a211d-134">`application-gateway {subresource} delete`：修复了不遵循 `--no-wait` 的问题</span><span class="sxs-lookup"><span data-stu-id="a211d-134">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="a211d-135">`application-gateway http-settings update`：修复了无法关闭 `--connection-draining-timeout` 的问题</span><span class="sxs-lookup"><span data-stu-id="a211d-135">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="a211d-136">修复了 `az network vpn-connection ipsec-policy add` 包含意外关键字参数 `sa_data_size_kilobyes` 的错误</span><span class="sxs-lookup"><span data-stu-id="a211d-136">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="a211d-137">配置文件</span><span class="sxs-lookup"><span data-stu-id="a211d-137">Profile</span></span>

* <span data-ttu-id="a211d-138">`account list`：添加了 `--refresh` 用于从服务器同步最新订阅</span><span class="sxs-lookup"><span data-stu-id="a211d-138">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="a211d-139">存储</span><span class="sxs-lookup"><span data-stu-id="a211d-139">Storage</span></span>

* <span data-ttu-id="a211d-140">启用了使用系统分配的标识更新存储帐户的功能</span><span class="sxs-lookup"><span data-stu-id="a211d-140">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="a211d-141">VM</span><span class="sxs-lookup"><span data-stu-id="a211d-141">VM</span></span>

* <span data-ttu-id="a211d-142">`availability-set`：公开了转换时的容错域计数</span><span class="sxs-lookup"><span data-stu-id="a211d-142">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="a211d-143">公开了 `list-skus` 命令</span><span class="sxs-lookup"><span data-stu-id="a211d-143">Exposed `list-skus` command</span></span>
* <span data-ttu-id="a211d-144">支持在不创建角色分配的情况下分配标识</span><span class="sxs-lookup"><span data-stu-id="a211d-144">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="a211d-145">附加数据磁盘时应用存储 SKU</span><span class="sxs-lookup"><span data-stu-id="a211d-145">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="a211d-146">删除了使用托管磁盘时的默认 OS 磁盘名称和存储 SKU</span><span class="sxs-lookup"><span data-stu-id="a211d-146">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="a211d-147">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="a211d-147">July 28, 2017</span></span>

<span data-ttu-id="a211d-148">版本 2.0.12</span><span class="sxs-lookup"><span data-stu-id="a211d-148">Version 2.0.12</span></span>

* <span data-ttu-id="a211d-149">添加了容器命令</span><span class="sxs-lookup"><span data-stu-id="a211d-149">Added container commands</span></span>
* <span data-ttu-id="a211d-150">添加了计费和消耗模块</span><span class="sxs-lookup"><span data-stu-id="a211d-150">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="a211d-151">核心</span><span class="sxs-lookup"><span data-stu-id="a211d-151">Core</span></span>

* <span data-ttu-id="a211d-152">输出包含证书的服务主体的 SDK 身份验证信息</span><span class="sxs-lookup"><span data-stu-id="a211d-152">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="a211d-153">修复了部署进度异常</span><span class="sxs-lookup"><span data-stu-id="a211d-153">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="a211d-154">使用当前云中的 arm 终结点创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="a211d-154">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="a211d-155">改进了 clouds.config 文件的并发处理 (#3636)</span><span class="sxs-lookup"><span data-stu-id="a211d-155">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="a211d-156">刷新每个命令执行进程的客户端请求 ID</span><span class="sxs-lookup"><span data-stu-id="a211d-156">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="a211d-157">使用适当的 SDK 配置文件创建订阅客户端 (#3635)</span><span class="sxs-lookup"><span data-stu-id="a211d-157">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="a211d-158">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="a211d-158">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="a211d-159">添加了通过 jmespath 查询选择表输出字段的支持 (#3581)</span><span class="sxs-lookup"><span data-stu-id="a211d-159">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="a211d-160">改进了分析参数的静默和包含手势的追加历史记录 (#3434)</span><span class="sxs-lookup"><span data-stu-id="a211d-160">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="a211d-161">使用适当的 SDK 配置文件创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="a211d-161">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="a211d-162">将所有现有记录文件移到最新的文件夹</span><span class="sxs-lookup"><span data-stu-id="a211d-162">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="a211d-163">修复了 VM/VMSS 创建操作的幂等性 (#3586)</span><span class="sxs-lookup"><span data-stu-id="a211d-163">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="a211d-164">命令路径不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="a211d-164">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="a211d-165">某些布尔类型的参数不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="a211d-165">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="a211d-166">支持登录到 Azure Stack 等本地服务器上的 ADFS</span><span class="sxs-lookup"><span data-stu-id="a211d-166">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="a211d-167">修复了并发写入 clouds.config 的问题 (#3255)</span><span class="sxs-lookup"><span data-stu-id="a211d-167">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="a211d-168">ACR</span><span class="sxs-lookup"><span data-stu-id="a211d-168">ACR</span></span>

* <span data-ttu-id="a211d-169">针对托管注册表添加了 `show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="a211d-169">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="a211d-170">支持托管注册表的 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="a211d-170">Support SKU update for managed registries</span></span>
* <span data-ttu-id="a211d-171">添加了包含托管 SKU 的托管注册表</span><span class="sxs-lookup"><span data-stu-id="a211d-171">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="a211d-172">通过 ACR Webhook 命令模块添加了托管注册表的 Webhook</span><span class="sxs-lookup"><span data-stu-id="a211d-172">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="a211d-173">添加了使用 acr login 命令进行 AAD 身份验证的功能</span><span class="sxs-lookup"><span data-stu-id="a211d-173">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="a211d-174">添加了 Docker 存储库、清单和标记的 delete 命令</span><span class="sxs-lookup"><span data-stu-id="a211d-174">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="a211d-175">ACS</span><span class="sxs-lookup"><span data-stu-id="a211d-175">ACS</span></span>

* <span data-ttu-id="a211d-176">API 版本 2017-07-01 的支持</span><span class="sxs-lookup"><span data-stu-id="a211d-176">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="a211d-177">应用服务</span><span class="sxs-lookup"><span data-stu-id="a211d-177">Appservice</span></span>

* <span data-ttu-id="a211d-178">修复了列出 Linux Web 应用时不返回任何内容的 bug</span><span class="sxs-lookup"><span data-stu-id="a211d-178">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="a211d-179">支持从 ACR 检索凭据</span><span class="sxs-lookup"><span data-stu-id="a211d-179">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="a211d-180">删除 `appservice web` 下的所有命令</span><span class="sxs-lookup"><span data-stu-id="a211d-180">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="a211d-181">将命令输出中的 Docker 注册表密码掩码 (#3656)</span><span class="sxs-lookup"><span data-stu-id="a211d-181">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="a211d-182">确保在 macOS 上使用默认浏览器且不出错 (#3623)</span><span class="sxs-lookup"><span data-stu-id="a211d-182">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="a211d-183">改进了 `webapp log tail` 和 `webapp log download` 的帮助 (#3624)</span><span class="sxs-lookup"><span data-stu-id="a211d-183">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="a211d-184">公开了 `traffic-routing` 命令用于配置静态路由 (#3566)</span><span class="sxs-lookup"><span data-stu-id="a211d-184">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="a211d-185">添加了用于配置源代码管理的可靠性修复 (#3245)</span><span class="sxs-lookup"><span data-stu-id="a211d-185">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="a211d-186">从 `webapp config update` 中删除了 Windows Web 应用不支持的 `--node-version` 参数。</span><span class="sxs-lookup"><span data-stu-id="a211d-186">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="a211d-187">需改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`。</span><span class="sxs-lookup"><span data-stu-id="a211d-187">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="a211d-188">批处理</span><span class="sxs-lookup"><span data-stu-id="a211d-188">Batch</span></span>

* <span data-ttu-id="a211d-189">已更新到 Batch SDK 3.0.0，支持池中的低优先级 VM</span><span class="sxs-lookup"><span data-stu-id="a211d-189">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="a211d-190">已将 `pool create` 选项 `--target-dedicated` 重命名为 `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="a211d-190">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="a211d-191">添加了 `pool create` 选项 `--target-low-priority-nodes` 和 `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="a211d-191">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="a211d-192">CDN</span><span class="sxs-lookup"><span data-stu-id="a211d-192">CDN</span></span>

* <span data-ttu-id="a211d-193">当 `--profile-name` 指定的配置文件不存在时，针对 `cdn endpoint list` 提供更完善的错误消息。</span><span class="sxs-lookup"><span data-stu-id="a211d-193">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="a211d-194">云</span><span class="sxs-lookup"><span data-stu-id="a211d-194">Cloud</span></span>

* <span data-ttu-id="a211d-195">已将云元数据终结点的 API 版本更改为 YYYY-MM-DD 格式</span><span class="sxs-lookup"><span data-stu-id="a211d-195">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="a211d-196">不需要库终结点</span><span class="sxs-lookup"><span data-stu-id="a211d-196">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="a211d-197">支持只将云注册到 ARM 资源管理器终结点</span><span class="sxs-lookup"><span data-stu-id="a211d-197">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="a211d-198">提供 `cloud set` 的选项用于在选择当前云时选择配置文件</span><span class="sxs-lookup"><span data-stu-id="a211d-198">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="a211d-199">公开了 `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="a211d-199">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="a211d-200">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="a211d-200">CosmosDB</span></span>

* <span data-ttu-id="a211d-201">修复了允许使用自定义分区键创建集合的问题</span><span class="sxs-lookup"><span data-stu-id="a211d-201">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="a211d-202">添加了对集合默认 TTL 的支持。</span><span class="sxs-lookup"><span data-stu-id="a211d-202">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="a211d-203">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="a211d-203">Data Lake Analytics</span></span>

* <span data-ttu-id="a211d-204">在 `dla account compute-policy` 标题下添加了用于计算策略管理的命令</span><span class="sxs-lookup"><span data-stu-id="a211d-204">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="a211d-205">添加了 `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="a211d-205">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="a211d-206">添加了 `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="a211d-206">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="a211d-207">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="a211d-207">Data Lake Store</span></span>

* <span data-ttu-id="a211d-208">在 `dls account update` 中添加了用户管理的 Key Vault 密钥轮换的支持</span><span class="sxs-lookup"><span data-stu-id="a211d-208">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="a211d-209">更新了底层 Data Lake Store 文件系统 SDK 版本，解决了一个性能问题</span><span class="sxs-lookup"><span data-stu-id="a211d-209">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="a211d-210">添加了命令 `dls enable-key-vault`。</span><span class="sxs-lookup"><span data-stu-id="a211d-210">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="a211d-211">此命令尝试使用用户提供的 Key Vault 加密 Data Lake Store 帐户中的数据</span><span class="sxs-lookup"><span data-stu-id="a211d-211">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="a211d-212">交互</span><span class="sxs-lookup"><span data-stu-id="a211d-212">Interactive</span></span>

* <span data-ttu-id="a211d-213">使用缓存的命令改进启动时间</span><span class="sxs-lookup"><span data-stu-id="a211d-213">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="a211d-214">增大了测试覆盖率</span><span class="sxs-lookup"><span data-stu-id="a211d-214">Increased test coverage</span></span>
* <span data-ttu-id="a211d-215">增强了“?”手势，使之也可注入到下一条命令</span><span class="sxs-lookup"><span data-stu-id="a211d-215">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="a211d-216">修复了配置文件 2017-03-09-profile-preview 的交互错误 (#3587)</span><span class="sxs-lookup"><span data-stu-id="a211d-216">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="a211d-217">允许使用 `--version` 作为交互模式的参数 (#3645)</span><span class="sxs-lookup"><span data-stu-id="a211d-217">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="a211d-218">阻止交互模式在验证填写内容中引发错误 (#3570)</span><span class="sxs-lookup"><span data-stu-id="a211d-218">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="a211d-219">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="a211d-219">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="a211d-220">添加了 `--progress` 标志</span><span class="sxs-lookup"><span data-stu-id="a211d-220">Added `--progress` flag</span></span>
* <span data-ttu-id="a211d-221">从填写内容中删除了 `--debug` 和 `--verbose`</span><span class="sxs-lookup"><span data-stu-id="a211d-221">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="a211d-222">从填写内容中删除了 `interactive` (#3324)</span><span class="sxs-lookup"><span data-stu-id="a211d-222">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="a211d-223">IoT</span><span class="sxs-lookup"><span data-stu-id="a211d-223">IoT</span></span>

* <span data-ttu-id="a211d-224">修复了策略创建操作不再清除现有策略的问题。</span><span class="sxs-lookup"><span data-stu-id="a211d-224">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="a211d-225">(#3934)</span><span class="sxs-lookup"><span data-stu-id="a211d-225">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="a211d-226">密钥保管库</span><span class="sxs-lookup"><span data-stu-id="a211d-226">Key vault</span></span>

* <span data-ttu-id="a211d-227">添加了 Key Vault 恢复功能的命令：</span><span class="sxs-lookup"><span data-stu-id="a211d-227">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="a211d-228">`keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="a211d-228">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="a211d-229">`keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="a211d-229">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="a211d-230">`keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="a211d-230">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="a211d-231">`keyvault key` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="a211d-231">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="a211d-232">添加了服务主体的 Key Vault 集成 (#3133)</span><span class="sxs-lookup"><span data-stu-id="a211d-232">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="a211d-233">已将 Key Vault 数据平面更新到 0.3.2。</span><span class="sxs-lookup"><span data-stu-id="a211d-233">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="a211d-234">(#3307)</span><span class="sxs-lookup"><span data-stu-id="a211d-234">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="a211d-235">实验室</span><span class="sxs-lookup"><span data-stu-id="a211d-235">Lab</span></span>

* <span data-ttu-id="a211d-236">添加了通过 `az lab vm claim` 在实验室中声明任何 VM 的支持</span><span class="sxs-lookup"><span data-stu-id="a211d-236">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="a211d-237">为 `az lab vm list` 和 `az lab vm show` 添加了表输出格式化程序</span><span class="sxs-lookup"><span data-stu-id="a211d-237">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="a211d-238">监视</span><span class="sxs-lookup"><span data-stu-id="a211d-238">Monitor</span></span>

* <span data-ttu-id="a211d-239">修复了与 `monitor autoscale-settings get-parameters-template` 命令结合使用的模板文件 (#3349)</span><span class="sxs-lookup"><span data-stu-id="a211d-239">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="a211d-240">已将 `monitor alert-rule-incidents list` 重命名为 `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="a211d-240">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="a211d-241">已将 `monitor alert-rule-incidents show` 重命名为 `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="a211d-241">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="a211d-242">已将 `monitor metric-defintions list` 重命名为 `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="a211d-242">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="a211d-243">已将 `monitor alert-rules` 重命名为 `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="a211d-243">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="a211d-244">更改了 `monitor alert create`：</span><span class="sxs-lookup"><span data-stu-id="a211d-244">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="a211d-245">`condition` 和 `action` 子命令不再接受 JSON</span><span class="sxs-lookup"><span data-stu-id="a211d-245">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="a211d-246">添加了大量的参数来简化规则创建过程</span><span class="sxs-lookup"><span data-stu-id="a211d-246">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="a211d-247">`location` 不再是必需的</span><span class="sxs-lookup"><span data-stu-id="a211d-247">`location` no longer required</span></span>
  * <span data-ttu-id="a211d-248">添加了目标的名称和 ID 支持</span><span class="sxs-lookup"><span data-stu-id="a211d-248">Add name and ID support for target</span></span>
  * <span data-ttu-id="a211d-249">删除了 `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="a211d-249">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="a211d-250">`is-enabled` 重命名为 `enabled`，不再是必需的</span><span class="sxs-lookup"><span data-stu-id="a211d-250">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="a211d-251">`description` 默认值现在基于提供的条件</span><span class="sxs-lookup"><span data-stu-id="a211d-251">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="a211d-252">添加了示例用于帮助澄清新格式</span><span class="sxs-lookup"><span data-stu-id="a211d-252">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="a211d-253">支持在 `monitor metric` 命令中使用名称或 ID</span><span class="sxs-lookup"><span data-stu-id="a211d-253">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="a211d-254">为 `monitor alert rule update` 添加了方便的参数和示例</span><span class="sxs-lookup"><span data-stu-id="a211d-254">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="a211d-255">网络</span><span class="sxs-lookup"><span data-stu-id="a211d-255">Network</span></span>

* <span data-ttu-id="a211d-256">添加了 `list-private-access-services` 命令</span><span class="sxs-lookup"><span data-stu-id="a211d-256">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="a211d-257">为 `vnet subnet create` 和 `vnet subnet update` 添加了 `--private-access-services` 参数</span><span class="sxs-lookup"><span data-stu-id="a211d-257">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="a211d-258">修复了 `application-gateway redirect-config create` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="a211d-258">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="a211d-259">修复了无法结合 `--no-wait` 使用 `application-gateway redirect-config update` 的问题</span><span class="sxs-lookup"><span data-stu-id="a211d-259">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="a211d-260">修复了结合 `application-gateway address-pool create` 和 `application-gateway address-pool update` 使用 `--servers` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="a211d-260">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="a211d-261">添加了 `application-gateway redirect-config` 命令</span><span class="sxs-lookup"><span data-stu-id="a211d-261">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="a211d-262">添加了 `application-gateway ssl-policy` 的命令：`list-options`、`predefined list`、`predefined show`</span><span class="sxs-lookup"><span data-stu-id="a211d-262">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="a211d-263">添加了 `application-gateway ssl-policy set` 的参数：`--name`、`--cipher-suites`、`--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="a211d-263">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="a211d-264">添加了 `application-gateway http-settings create` 和 `application-gateway http-settings update` 的参数：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`</span><span class="sxs-lookup"><span data-stu-id="a211d-264">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="a211d-265">添加了 `application-gateway url-path-map create` 和 `application-gateway url-path-map update` 的参数：`--default-redirect-config`、`--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="a211d-265">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="a211d-266">为 `application-gateway url-path-map rule create` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="a211d-266">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="a211d-267">在 `application-gateway url-path-map rule delete` 中添加了对 `--no-wait` 的支持</span><span class="sxs-lookup"><span data-stu-id="a211d-267">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="a211d-268">添加了 `application-gateway probe create` 和 `application-gateway probe update` 的参数：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="a211d-268">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="a211d-269">为 `application-gateway rule create` 和 `application-gateway rule update` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="a211d-269">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="a211d-270">在 `nic create` 和 `nic update` 中添加了对 `--accelerated-networking` 的支持</span><span class="sxs-lookup"><span data-stu-id="a211d-270">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="a211d-271">从 `nic create` 中删除了 `--internal-dns-name-suffix` 参数</span><span class="sxs-lookup"><span data-stu-id="a211d-271">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="a211d-272">在 `nic update` 和 `nic create` 中添加了对 `--dns-servers` 的支持：添加了对 --dns-servers 的支持</span><span class="sxs-lookup"><span data-stu-id="a211d-272">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="a211d-273">修复了 `local-gateway create` 忽略 `--local-address-prefixes` 的 bug</span><span class="sxs-lookup"><span data-stu-id="a211d-273">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="a211d-274">在 `vnet update` 中添加了对 `--dns-servers` 的支持</span><span class="sxs-lookup"><span data-stu-id="a211d-274">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="a211d-275">修复了使用 `express-route peering create` 创建不包含路由筛选的对等互连时的 bug</span><span class="sxs-lookup"><span data-stu-id="a211d-275">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="a211d-276">修复了无法结合 `--provider` 和 `--bandwidth` 参数使用 `express-route update` 的 bug</span><span class="sxs-lookup"><span data-stu-id="a211d-276">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="a211d-277">修复了 `network watcher show-topology` 默认逻辑的 bug</span><span class="sxs-lookup"><span data-stu-id="a211d-277">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="a211d-278">改进了 `network list-usages` 的输出格式</span><span class="sxs-lookup"><span data-stu-id="a211d-278">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="a211d-279">如果只存在一个，则对 `application-gateway http-listener create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="a211d-279">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="a211d-280">如果只存在一个，则对 `application-gateway rule create` 使用默认地址池、HTTP 设置和 HTTP 侦听器</span><span class="sxs-lookup"><span data-stu-id="a211d-280">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="a211d-281">如果只存在一个，则对 `lb rule create` 使用默认前端 IP 和后端池</span><span class="sxs-lookup"><span data-stu-id="a211d-281">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="a211d-282">如果只存在一个，则对 `lb inbound-nat-rule create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="a211d-282">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="a211d-283">配置文件</span><span class="sxs-lookup"><span data-stu-id="a211d-283">Profile</span></span>

* <span data-ttu-id="a211d-284">支持使用托管标识在 VM 内部登录</span><span class="sxs-lookup"><span data-stu-id="a211d-284">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="a211d-285">支持采用 SDK 身份验证文件格式的 `account show` 输出</span><span class="sxs-lookup"><span data-stu-id="a211d-285">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="a211d-286">使用 '--expanded-view' 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="a211d-286">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="a211d-287">添加了 `get-access-token` 命令来提供原始 AAD 令牌</span><span class="sxs-lookup"><span data-stu-id="a211d-287">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="a211d-288">支持使用不包含关联订阅的用户帐户登录</span><span class="sxs-lookup"><span data-stu-id="a211d-288">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="a211d-289">RDBMS</span><span class="sxs-lookup"><span data-stu-id="a211d-289">RDBMS</span></span>

* <span data-ttu-id="a211d-290">支持跨订阅列出服务器 (#3417)</span><span class="sxs-lookup"><span data-stu-id="a211d-290">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="a211d-291">修复了由于缺少 `% server_type` 而不处理 `%s` 的问题 (#3393)</span><span class="sxs-lookup"><span data-stu-id="a211d-291">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="a211d-292">修复了文档源映射并添加了 CI 任务用于验证 (#3361)</span><span class="sxs-lookup"><span data-stu-id="a211d-292">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="a211d-293">修复了 MySQL 和 PostgreSQL 帮助 (#3369)</span><span class="sxs-lookup"><span data-stu-id="a211d-293">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="a211d-294">资源</span><span class="sxs-lookup"><span data-stu-id="a211d-294">Resource</span></span>

* <span data-ttu-id="a211d-295">改进了有关 `group deployment create` 缺少参数的提示</span><span class="sxs-lookup"><span data-stu-id="a211d-295">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="a211d-296">改进了 `--parameters KEY=VALUE` 语法分析</span><span class="sxs-lookup"><span data-stu-id="a211d-296">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="a211d-297">修复了不再能够使用 `@<file>` 语法识别 `group deployment create` 参数文件的问题</span><span class="sxs-lookup"><span data-stu-id="a211d-297">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="a211d-298">支持 `resource` 和 `managedapp` 命令的 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="a211d-298">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="a211d-299">修复了一些分析和错误消息 (#3584)</span><span class="sxs-lookup"><span data-stu-id="a211d-299">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="a211d-300">修复了 `lock` 命令的 `--resource-type` 分析，接受 `<resource-namespace>` 和 `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="a211d-300">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="a211d-301">添加了模板链接模板的参数检查 (#3629)</span><span class="sxs-lookup"><span data-stu-id="a211d-301">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="a211d-302">添加了使用 `KEY=VALUE` 语法指定部署参数的支持</span><span class="sxs-lookup"><span data-stu-id="a211d-302">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="a211d-303">角色</span><span class="sxs-lookup"><span data-stu-id="a211d-303">Role</span></span>

* <span data-ttu-id="a211d-304">支持采用 SDK 身份验证文件格式的 `create-for-rbac` 输出</span><span class="sxs-lookup"><span data-stu-id="a211d-304">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="a211d-305">删除服务主体时清理角色分配和相关的 AAD 应用程序 (#3610)</span><span class="sxs-lookup"><span data-stu-id="a211d-305">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="a211d-306">在 `app create` 参数 `--start-date` 和 `--end-date` 说明中包含时间格式</span><span class="sxs-lookup"><span data-stu-id="a211d-306">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="a211d-307">使用 `--expanded-view` 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="a211d-307">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="a211d-308">在 `create-for-rbac` 和 `reset-credentials` 命令中添加了 Key Vault 集成</span><span class="sxs-lookup"><span data-stu-id="a211d-308">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="a211d-309">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="a211d-309">Service Fabric</span></span>
* <span data-ttu-id="a211d-310">修复了上传时截断应用程序中的大型文件的问题 (#3666)</span><span class="sxs-lookup"><span data-stu-id="a211d-310">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="a211d-311">添加了 Service Fabric 命令的测试 (#3424)</span><span class="sxs-lookup"><span data-stu-id="a211d-311">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="a211d-312">添加了大量的 Service Fabric 命令 (#3234)</span><span class="sxs-lookup"><span data-stu-id="a211d-312">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="a211d-313">SQL</span><span class="sxs-lookup"><span data-stu-id="a211d-313">SQL</span></span>

* <span data-ttu-id="a211d-314">删除了无效的 `sql server create` `--identity` 参数</span><span class="sxs-lookup"><span data-stu-id="a211d-314">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="a211d-315">从 `sql server create` 和 `sql server update` 命令输出中删除了密码值</span><span class="sxs-lookup"><span data-stu-id="a211d-315">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="a211d-316">添加了命令 `sql db list-editions` 和 `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="a211d-316">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="a211d-317">存储</span><span class="sxs-lookup"><span data-stu-id="a211d-317">Storage</span></span>

* <span data-ttu-id="a211d-318">从 `storage blob list`、`storage container list` 和 `storage share list` 命令中删除了 `--marker` 选项 (#3745)</span><span class="sxs-lookup"><span data-stu-id="a211d-318">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="a211d-319">启用了创建仅限 https 的存储帐户</span><span class="sxs-lookup"><span data-stu-id="a211d-319">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="a211d-320">更新了存储指标、日志记录和 CORS 命令 (#3495)</span><span class="sxs-lookup"><span data-stu-id="a211d-320">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="a211d-321">重新编写了 CORS add 命令的异常消息 (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="a211d-321">Rephrased exception message from CORS add (#3638) (#3362)</span></span>  
* <span data-ttu-id="a211d-322">已在下载批处理命令试运行模式下将生成器转换为列表 (#3592)</span><span class="sxs-lookup"><span data-stu-id="a211d-322">Converted generator to a list in download batch command dry run mode (#3592)</span></span> 
* <span data-ttu-id="a211d-323">修复了 Blob 下载批处理试运行问题 (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="a211d-323">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="a211d-324">VM</span><span class="sxs-lookup"><span data-stu-id="a211d-324">VM</span></span>

* <span data-ttu-id="a211d-325">支持配置 NSG</span><span class="sxs-lookup"><span data-stu-id="a211d-325">Support configuring nsg</span></span>
* <span data-ttu-id="a211d-326">修复了无法正确配置 DNS 服务器的 bug</span><span class="sxs-lookup"><span data-stu-id="a211d-326">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="a211d-327">支持托管服务标识</span><span class="sxs-lookup"><span data-stu-id="a211d-327">Support managed service identities</span></span>
* <span data-ttu-id="a211d-328">修复了包含现有负载均衡器的 `cmss create` 需要 `--backend-pool-name` 的问题。</span><span class="sxs-lookup"><span data-stu-id="a211d-328">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="a211d-329">要求使用 `vm image create` LUN 创建的数据磁盘以 0 开头</span><span class="sxs-lookup"><span data-stu-id="a211d-329">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="a211d-330">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="a211d-330">May 10, 2017</span></span>

<span data-ttu-id="a211d-331">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="a211d-331">Version 2.0.6</span></span>

* <span data-ttu-id="a211d-332">Documentdb 已重命名为 Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="a211d-332">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="a211d-333">添加 rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="a211d-333">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="a211d-334">包括 Data Lake Analytics 和 Data Lake Store 模块。</span><span class="sxs-lookup"><span data-stu-id="a211d-334">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="a211d-335">包括认知服务模块。</span><span class="sxs-lookup"><span data-stu-id="a211d-335">Include Cognitive Services module.</span></span>
* <span data-ttu-id="a211d-336">包括 Service Fabric 模块。</span><span class="sxs-lookup"><span data-stu-id="a211d-336">Include Service Fabric module.</span></span>
* <span data-ttu-id="a211d-337">包括交互式模块（重命名 az-shell）。</span><span class="sxs-lookup"><span data-stu-id="a211d-337">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="a211d-338">添加对 CDN 命令的支持。</span><span class="sxs-lookup"><span data-stu-id="a211d-338">Add support for CDN commands.</span></span>
* <span data-ttu-id="a211d-339">删除容器模块。</span><span class="sxs-lookup"><span data-stu-id="a211d-339">Remove Container module.</span></span>
* <span data-ttu-id="a211d-340">添加“az -v”作为“az --version”的快捷方式 ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="a211d-340">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="a211d-341">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="a211d-341">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="a211d-342">核心</span><span class="sxs-lookup"><span data-stu-id="a211d-342">Core</span></span>

* <span data-ttu-id="a211d-343">核心：捕获未注册提供程序引发的异常并自动注册</span><span class="sxs-lookup"><span data-stu-id="a211d-343">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="a211d-344">性能：将 ADAL 令牌缓存保留在内存中，直至进程退出 ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="a211d-344">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="a211d-345">修复从十六进制指纹 -o tsv 返回的字节 ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="a211d-345">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="a211d-346">改进的 Key Vault 证书下载和 AAD SP 集成 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="a211d-346">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="a211d-347">将 Python 位置添加到“az —version”([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="a211d-347">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="a211d-348">登录：无订阅时支持登录 ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="a211d-348">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="a211d-349">核心：修复重复使用服务主体登录时出现的故障 ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="a211d-349">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="a211d-350">核心：允许通过 env var 配置 accessTokens.json 的文件路径 ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="a211d-350">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="a211d-351">核心：允许配置的默认值应用于可选参数 ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="a211d-351">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="a211d-352">核心：提高了性能</span><span class="sxs-lookup"><span data-stu-id="a211d-352">core: Improved performance</span></span>
* <span data-ttu-id="a211d-353">核心：自定义 CA 证书 - 支持设置 REQUESTS_CA_BUNDLE 环境变量</span><span class="sxs-lookup"><span data-stu-id="a211d-353">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="a211d-354">核心：云配置 - 如果未设置“management”终结点，则使用“resource manager”终结点</span><span class="sxs-lookup"><span data-stu-id="a211d-354">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="a211d-355">ACS</span><span class="sxs-lookup"><span data-stu-id="a211d-355">ACS</span></span>

* <span data-ttu-id="a211d-356">将主计数和代理计数修复为整数而不是字符串</span><span class="sxs-lookup"><span data-stu-id="a211d-356">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="a211d-357">公开“az acs create --no-wait”和“az acs wait”用于异步创建</span><span class="sxs-lookup"><span data-stu-id="a211d-357">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="a211d-358">公开“az acs create --validate”用于试运行验证</span><span class="sxs-lookup"><span data-stu-id="a211d-358">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="a211d-359">在 PUT 调用 scale 命令前删除 Windows 配置文件 ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="a211d-359">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="a211d-360">应用服务</span><span class="sxs-lookup"><span data-stu-id="a211d-360">AppService</span></span>

* <span data-ttu-id="a211d-361">Function App：添加完整的 Function App 支持，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="a211d-361">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="a211d-362">将 Team Services (vsts) 作为持续交付选项添加到“appservice web source-control config”</span><span class="sxs-lookup"><span data-stu-id="a211d-362">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="a211d-363">创建“az webapp”以替换“az appservice web”（为了向后兼容，“az appservice web”将保留 2 个版本）</span><span class="sxs-lookup"><span data-stu-id="a211d-363">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="a211d-364">公开参数以针对 webapp create 配置部署和“运行时堆栈”</span><span class="sxs-lookup"><span data-stu-id="a211d-364">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="a211d-365">公开“webapp list-runtimes”</span><span class="sxs-lookup"><span data-stu-id="a211d-365">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="a211d-366">支持配置连接字符串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="a211d-366">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="a211d-367">支持与预览版交换槽</span><span class="sxs-lookup"><span data-stu-id="a211d-367">support slot swap with preview</span></span>
* <span data-ttu-id="a211d-368">修改 appservice 命令的错误 ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="a211d-368">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="a211d-369">将应用服务计划的资源组用于证书操作 ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="a211d-369">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="a211d-370">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="a211d-370">CosmosDB</span></span>

* <span data-ttu-id="a211d-371">将 DocumentDB 模块重命名为 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="a211d-371">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="a211d-372">增加对 DocumentDB 数据平面 API 的支持：数据库和集合管理</span><span class="sxs-lookup"><span data-stu-id="a211d-372">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="a211d-373">增加对数据库帐户启用自动故障转移的支持</span><span class="sxs-lookup"><span data-stu-id="a211d-373">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="a211d-374">增加对新一致性策略 ConsistentPrefix 的支持</span><span class="sxs-lookup"><span data-stu-id="a211d-374">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="a211d-375">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="a211d-375">Data Lake Analytics</span></span>

* <span data-ttu-id="a211d-376">Bug 修复：在筛选作业结果和状态列表时会引发错误。</span><span class="sxs-lookup"><span data-stu-id="a211d-376">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="a211d-377">增加对新目录项类型的支持：包。</span><span class="sxs-lookup"><span data-stu-id="a211d-377">Add support for new catalog item type: package.</span></span> <span data-ttu-id="a211d-378">访问方法：`az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="a211d-378">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="a211d-379">可从数据库内列出下列目录项（无需架构规范）：</span><span class="sxs-lookup"><span data-stu-id="a211d-379">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="a211d-380">表</span><span class="sxs-lookup"><span data-stu-id="a211d-380">Table</span></span>
  * <span data-ttu-id="a211d-381">表值函数</span><span class="sxs-lookup"><span data-stu-id="a211d-381">Table valued function</span></span>
  * <span data-ttu-id="a211d-382">查看</span><span class="sxs-lookup"><span data-stu-id="a211d-382">View</span></span>
  * <span data-ttu-id="a211d-383">表统计信息。</span><span class="sxs-lookup"><span data-stu-id="a211d-383">Table Statistics.</span></span> <span data-ttu-id="a211d-384">也可以使用架构列出，但无需指定表名。</span><span class="sxs-lookup"><span data-stu-id="a211d-384">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="a211d-385">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="a211d-385">Data Lake Store</span></span>

* <span data-ttu-id="a211d-386">更新基础文件系统 SDK 版本，可更好地支持处理服务器端限制方案。</span><span class="sxs-lookup"><span data-stu-id="a211d-386">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="a211d-387">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="a211d-387">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="a211d-388">访问显示帮助丢失。</span><span class="sxs-lookup"><span data-stu-id="a211d-388">missed help for access show.</span></span> <span data-ttu-id="a211d-389">正在添加。</span><span class="sxs-lookup"><span data-stu-id="a211d-389">adding it.</span></span> <span data-ttu-id="a211d-390">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="a211d-390">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="a211d-391">查找</span><span class="sxs-lookup"><span data-stu-id="a211d-391">Find</span></span>

* <span data-ttu-id="a211d-392">改进搜索结果，允许搜索索引的版本控制</span><span class="sxs-lookup"><span data-stu-id="a211d-392">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="a211d-393">KeyVault</span><span class="sxs-lookup"><span data-stu-id="a211d-393">KeyVault</span></span>

* <span data-ttu-id="a211d-394">BC：`az keyvault certificate download` 将 -e 从字符串或二进制更改为 PEM 或 DER，从而更好地表示选项</span><span class="sxs-lookup"><span data-stu-id="a211d-394">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="a211d-395">BC：从 `keyvault certificate create` 删除 --expires 和 --not-before，因为此服务不支持这些参数。</span><span class="sxs-lookup"><span data-stu-id="a211d-395">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="a211d-396">将 --validity 参数添加到 `keyvault certificate create`，有选择地替代 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="a211d-396">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="a211d-397">解决 `keyvault certificate get-default-policy` 中的问题：“expires”和“not_before”已公开，但“validity_in_months”未公开。</span><span class="sxs-lookup"><span data-stu-id="a211d-397">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="a211d-398">KeyVault 解决了 pem 和 pfx 的导入问题 ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="a211d-398">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="a211d-399">实验室</span><span class="sxs-lookup"><span data-stu-id="a211d-399">Lab</span></span>

* <span data-ttu-id="a211d-400">针对实验室环境添加 create、show、delete 和 list 命令。</span><span class="sxs-lookup"><span data-stu-id="a211d-400">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="a211d-401">添加 show 和 list 命令，查看实验室中的 ARM 模板。</span><span class="sxs-lookup"><span data-stu-id="a211d-401">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="a211d-402">在 `az lab vm list` 中添加 --environment 标志，按实验室环境筛选 VM。</span><span class="sxs-lookup"><span data-stu-id="a211d-402">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="a211d-403">添加 convenience 命令 `az lab formula export-artifacts`，导出实验室公式中的项目基架。</span><span class="sxs-lookup"><span data-stu-id="a211d-403">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="a211d-404">添加命令，管理实验室中的机密。</span><span class="sxs-lookup"><span data-stu-id="a211d-404">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="a211d-405">监视</span><span class="sxs-lookup"><span data-stu-id="a211d-405">Monitor</span></span>

* <span data-ttu-id="a211d-406">Bug 修复：为 `az alert-rules create` 的 `--actions` 建模，以使用 JSON 字符串 ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="a211d-406">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="a211d-407">Bug 修复 - diagnostic settings create 不接受来自 show 命令的日志/指标 ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="a211d-407">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="a211d-408">网络</span><span class="sxs-lookup"><span data-stu-id="a211d-408">Network</span></span>

* <span data-ttu-id="a211d-409">添加 `network watcher test-connectivity` 命令。</span><span class="sxs-lookup"><span data-stu-id="a211d-409">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="a211d-410">添加对 `network watcher packet-capture create` 的 `--filters` 参数的支持。</span><span class="sxs-lookup"><span data-stu-id="a211d-410">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="a211d-411">添加对应用程序网关连接排出的支持。</span><span class="sxs-lookup"><span data-stu-id="a211d-411">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="a211d-412">添加对应用程序网关 WAF 规则集配置的支持。</span><span class="sxs-lookup"><span data-stu-id="a211d-412">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="a211d-413">添加对 ExpressRoute 路由筛选器和规则的支持。</span><span class="sxs-lookup"><span data-stu-id="a211d-413">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="a211d-414">添加对 TrafficManager 地理路由的支持。</span><span class="sxs-lookup"><span data-stu-id="a211d-414">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="a211d-415">添加对基于 VPN 连接策略的流量选择器的支持。</span><span class="sxs-lookup"><span data-stu-id="a211d-415">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="a211d-416">添加对 VPN 连接 IPSec 策略的支持。</span><span class="sxs-lookup"><span data-stu-id="a211d-416">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="a211d-417">修复使用 `--no-wait` 或 `--validate` 参数时 `vpn-connection create` 出现的 bug。</span><span class="sxs-lookup"><span data-stu-id="a211d-417">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="a211d-418">添加对主动-主动 VNet 网关的支持</span><span class="sxs-lookup"><span data-stu-id="a211d-418">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="a211d-419">从 `network vpn-connection list/show` 命令的输出中删除 null 值。</span><span class="sxs-lookup"><span data-stu-id="a211d-419">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="a211d-420">BC：修复 `vpn-connection create` 输出中的 bug</span><span class="sxs-lookup"><span data-stu-id="a211d-420">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="a211d-421">Bug 修复：“vpn-connection create”的“--key-length”参数未正确分析。</span><span class="sxs-lookup"><span data-stu-id="a211d-421">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="a211d-422">修复 `dns zone import` 中的 Bug：记录未正确导入。</span><span class="sxs-lookup"><span data-stu-id="a211d-422">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="a211d-423">Bug 修复：`traffic-manager endpoint update` 不起作用。</span><span class="sxs-lookup"><span data-stu-id="a211d-423">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="a211d-424">添加“network watcher”预览命令。</span><span class="sxs-lookup"><span data-stu-id="a211d-424">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="a211d-425">配置文件</span><span class="sxs-lookup"><span data-stu-id="a211d-425">Profile</span></span>

* <span data-ttu-id="a211d-426">支持在未找到订阅时登录 ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="a211d-426">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="a211d-427">支持在 az account set --subscription 中使用短参数名 ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="a211d-427">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="a211d-428">Redis</span><span class="sxs-lookup"><span data-stu-id="a211d-428">Redis</span></span>

* <span data-ttu-id="a211d-429">添加 update 命令，也增加了对 redis 缓存进行缩放的功能</span><span class="sxs-lookup"><span data-stu-id="a211d-429">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="a211d-430">弃用“update-settings”命令。</span><span class="sxs-lookup"><span data-stu-id="a211d-430">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="a211d-431">资源</span><span class="sxs-lookup"><span data-stu-id="a211d-431">Resource</span></span>

* <span data-ttu-id="a211d-432">添加 managedapp 和 managedapp 定义命令 ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="a211d-432">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="a211d-433">支持“provider operation”命令([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="a211d-433">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="a211d-434">支持 generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="a211d-434">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="a211d-435">修复资源分析和 API 版本查找。</span><span class="sxs-lookup"><span data-stu-id="a211d-435">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="a211d-436">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="a211d-436">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="a211d-437">为 az lock update 添加文档。</span><span class="sxs-lookup"><span data-stu-id="a211d-437">Add docs for az lock update.</span></span> <span data-ttu-id="a211d-438">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="a211d-438">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="a211d-439">尝试为不存在的组列出资源时出错。</span><span class="sxs-lookup"><span data-stu-id="a211d-439">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="a211d-440">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="a211d-440">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="a211d-441">[计算] 修复 VMSS 和 VM 可用性集更新的相关问题。</span><span class="sxs-lookup"><span data-stu-id="a211d-441">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="a211d-442">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="a211d-442">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="a211d-443">parent-resource-path 为 None 时修复 lock create 和 delete ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="a211d-443">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="a211d-444">角色</span><span class="sxs-lookup"><span data-stu-id="a211d-444">Role</span></span>

* <span data-ttu-id="a211d-445">create-for-rbac：确保 SP 的结束日期不超过证书的到期日期 ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="a211d-445">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="a211d-446">RBAC：添加对“ad group”的完整支持 ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="a211d-446">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="a211d-447">role：解决角色定义更新的相关问题 ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="a211d-447">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="a211d-448">create-for-rbac：确保已选取用户提供的密码</span><span class="sxs-lookup"><span data-stu-id="a211d-448">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="a211d-449">SQL</span><span class="sxs-lookup"><span data-stu-id="a211d-449">SQL</span></span>

* <span data-ttu-id="a211d-450">添加了 az sql server list-usages 和 az sql db list-usages 命令。</span><span class="sxs-lookup"><span data-stu-id="a211d-450">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="a211d-451">SQL - 能够直接连接到资源提供程序 ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="a211d-451">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="a211d-452">存储</span><span class="sxs-lookup"><span data-stu-id="a211d-452">Storage</span></span>

* <span data-ttu-id="a211d-453">位置默认为 `storage account create` 的资源组位置。</span><span class="sxs-lookup"><span data-stu-id="a211d-453">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="a211d-454">添加对增量 blob 复制的支持</span><span class="sxs-lookup"><span data-stu-id="a211d-454">Add support for incremental blob copy</span></span>
* <span data-ttu-id="a211d-455">添加对大型块 blob 上传的支持</span><span class="sxs-lookup"><span data-stu-id="a211d-455">Add support for large block blob upload</span></span>
* <span data-ttu-id="a211d-456">如果要上传的文件大于 200GB，则将块大小更改为 100MB</span><span class="sxs-lookup"><span data-stu-id="a211d-456">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="a211d-457">VM</span><span class="sxs-lookup"><span data-stu-id="a211d-457">VM</span></span>

* <span data-ttu-id="a211d-458">avail-set：将 UD 和 FD 域计数设为可选</span><span class="sxs-lookup"><span data-stu-id="a211d-458">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="a211d-459">注意：最高等级云中的 VM 命令。请避免与托管磁盘相关的功能，包括以下项：</span><span class="sxs-lookup"><span data-stu-id="a211d-459">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="a211d-460">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="a211d-460">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="a211d-461">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="a211d-461">az vm/vmss disk</span></span>
  3. <span data-ttu-id="a211d-462">在“az vm/vmss create”内，使用“—use-unmanaged-disk”避免托管磁盘 其他命令应有效</span><span class="sxs-lookup"><span data-stu-id="a211d-462">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="a211d-463">vm/vmss：改进生成 SSH 密钥对时的警告文本</span><span class="sxs-lookup"><span data-stu-id="a211d-463">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="a211d-464">vm/vmss：支持通过需要计划信息的市场映像创建 ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="a211d-464">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="a211d-465">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="a211d-465">April 3, 2017</span></span>

<span data-ttu-id="a211d-466">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="a211d-466">Version 2.0.2</span></span>

<span data-ttu-id="a211d-467">此版本中已发布 ACR、批处理、KeyVault 和 SQL 组件。</span><span class="sxs-lookup"><span data-stu-id="a211d-467">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="a211d-468">核心</span><span class="sxs-lookup"><span data-stu-id="a211d-468">Core</span></span>

* <span data-ttu-id="a211d-469">在默认列表中添加了 acr、实验室、监视和查找模块。</span><span class="sxs-lookup"><span data-stu-id="a211d-469">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="a211d-470">登录：跳过错误的租户 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="a211d-470">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="a211d-471">登录：将默认订阅设置为处于“已启用”状态的订阅 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="a211d-471">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="a211d-472">添加了 wait 命令，并添加了对其他命令的 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="a211d-472">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="a211d-473">核心：支持结合证书使用服务主体登录 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="a211d-473">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="a211d-474">添加了有关缺少模板参数的提示。</span><span class="sxs-lookup"><span data-stu-id="a211d-474">Add prompting for missing template parameters.</span></span> <span data-ttu-id="a211d-475">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="a211d-475">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="a211d-476">支持为资源组、默认 Web、 默认 VM 等常见参数设置默认值</span><span class="sxs-lookup"><span data-stu-id="a211d-476">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="a211d-477">支持登录到特定的租户</span><span class="sxs-lookup"><span data-stu-id="a211d-477">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="a211d-478">ACS</span><span class="sxs-lookup"><span data-stu-id="a211d-478">ACS</span></span>

* <span data-ttu-id="a211d-479">[ACS] 添加了配置默认 ACS 群集的支持 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="a211d-479">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="a211d-480">添加了 SSH 密钥密码提示的支持。</span><span class="sxs-lookup"><span data-stu-id="a211d-480">Add support for ssh key password prompting.</span></span> <span data-ttu-id="a211d-481">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="a211d-481">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="a211d-482">添加了对 Windows 群集的支持。</span><span class="sxs-lookup"><span data-stu-id="a211d-482">Add support for windows clusters.</span></span> <span data-ttu-id="a211d-483">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="a211d-483">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="a211d-484">从“所有者”角色切换到“参与者”角色。</span><span class="sxs-lookup"><span data-stu-id="a211d-484">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="a211d-485">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="a211d-485">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="a211d-486">应用服务</span><span class="sxs-lookup"><span data-stu-id="a211d-486">AppService</span></span>

* <span data-ttu-id="a211d-487">应用服务：支持获取用于 DNS A 记录的外部 IP 地址 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="a211d-487">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="a211d-488">应用服务：支持绑定通配符证书 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="a211d-488">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="a211d-489">应用服务：支持列出发布配置文件 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="a211d-489">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="a211d-490">应用服务 - 配置后触发源代码管理同步 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="a211d-490">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="a211d-491">DataLake</span><span class="sxs-lookup"><span data-stu-id="a211d-491">DataLake</span></span>

* <span data-ttu-id="a211d-492">Data Lake Analytics 模块的初始版本。</span><span class="sxs-lookup"><span data-stu-id="a211d-492">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="a211d-493">Data Lake Store 模块的初始版本。</span><span class="sxs-lookup"><span data-stu-id="a211d-493">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="a211d-494">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="a211d-494">DocuemntDB</span></span>

* <span data-ttu-id="a211d-495">DocumentDB：添加了列出连接字符串的支持 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="a211d-495">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="a211d-496">VM</span><span class="sxs-lookup"><span data-stu-id="a211d-496">VM</span></span>

* <span data-ttu-id="a211d-497">[计算] 添加了用于创建虚拟机规模集的应用网关支持 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="a211d-497">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="a211d-498">[VM/VMSS] 改进了磁盘缓存支持 ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="a211d-498">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="a211d-499">VM/VMSS：合并了门户使用的凭据验证逻辑 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="a211d-499">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="a211d-500">添加了 wait 命令和 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="a211d-500">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="a211d-501">虚拟机规模集：支持使用 * 列出不同 VM 上的实例视图 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="a211d-501">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="a211d-502">添加了适用于 VM 和虚拟机规模集的 --secrets ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="a211d-502">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="a211d-503">允许使用专用 VHD 创建 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="a211d-503">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="a211d-504">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="a211d-504">February 27, 2017</span></span>

<span data-ttu-id="a211d-505">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="a211d-505">Version 2.0.0</span></span>

<span data-ttu-id="a211d-506">此版 Azure CLI 2.0 是第一个“正式版”。</span><span class="sxs-lookup"><span data-stu-id="a211d-506">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="a211d-507">正式版适用于以下命令模块：</span><span class="sxs-lookup"><span data-stu-id="a211d-507">General availability applies to these command modules:</span></span>
- <span data-ttu-id="a211d-508">容器服务 (ACS)</span><span class="sxs-lookup"><span data-stu-id="a211d-508">Container Service (acs)</span></span>
- <span data-ttu-id="a211d-509">计算（包括 Resource Manager、VM、虚拟机规模集、托管磁盘）</span><span class="sxs-lookup"><span data-stu-id="a211d-509">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="a211d-510">网络</span><span class="sxs-lookup"><span data-stu-id="a211d-510">Networking</span></span>
- <span data-ttu-id="a211d-511">存储</span><span class="sxs-lookup"><span data-stu-id="a211d-511">Storage</span></span>

<span data-ttu-id="a211d-512">这些命令模块可在生产环境中使用，并受标准 Microsoft SLA 的支持。</span><span class="sxs-lookup"><span data-stu-id="a211d-512">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="a211d-513">可以直接向 Microsoft 支持部门或者通过 [github 问题列表](https://github.com/azure/azure-cli/issues/)提出问题。</span><span class="sxs-lookup"><span data-stu-id="a211d-513">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="a211d-514">可以[在 StackOverflow 上使用 azure-cli 标记](http://stackoverflow.com/questions/tagged/azure-cli)或者通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队来提出问题。可以通过命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="a211d-514">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="a211d-515">这些模块中的命令非常稳定，其语法在此 Azure CLI 版本的后续发行版中预期不会变化。</span><span class="sxs-lookup"><span data-stu-id="a211d-515">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="a211d-516">若要检查 CLI 版本，请使用 `az --version`。</span><span class="sxs-lookup"><span data-stu-id="a211d-516">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="a211d-517">输出中将列出 CLI 本身的版本（在此发行版中为 2.0.0）、各个命令模块的版本，以及所用 Python 和 GCC 的版本。</span><span class="sxs-lookup"><span data-stu-id="a211d-517">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="a211d-518">某些命令模块带有“bn”或“rcn”后缀。</span><span class="sxs-lookup"><span data-stu-id="a211d-518">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="a211d-519">这些命令模块仍以预览版提供，将来会发布正式版。</span><span class="sxs-lookup"><span data-stu-id="a211d-519">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="a211d-520">此外，我们还提供 CLI 夜间预览版。</span><span class="sxs-lookup"><span data-stu-id="a211d-520">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="a211d-521">有关信息，请参阅有关[获取夜间预览版](https://github.com/Azure/azure-cli#nightly-builds)的说明，以及有关[开发人员设置与贡献代码](https://github.com/Azure/azure-cli#developer-setup)的说明。</span><span class="sxs-lookup"><span data-stu-id="a211d-521">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="a211d-522">可通过以下方式报告夜间预览版的问题：</span><span class="sxs-lookup"><span data-stu-id="a211d-522">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="a211d-523">在 [github 问题列表](https://github.com/azure/azure-cli/issues/)中报告问题</span><span class="sxs-lookup"><span data-stu-id="a211d-523">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="a211d-524">通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队。</span><span class="sxs-lookup"><span data-stu-id="a211d-524">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="a211d-525">请通过命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="a211d-525">Provide feedback from the command line with the `az feedback` command.</span></span>

