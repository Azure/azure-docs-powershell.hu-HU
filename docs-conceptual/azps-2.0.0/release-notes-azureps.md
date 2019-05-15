---
ms.openlocfilehash: 3848f7fb8e298d137c747405f32a0776c1a8f029
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048631"
---
## <a name="200---may-2019"></a><span data-ttu-id="9a569-101">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="9a569-101">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9a569-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9a569-102">Az.Accounts</span></span>
* <span data-ttu-id="9a569-103">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="9a569-103">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="9a569-104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9a569-104">Az.CognitiveServices</span></span>
* <span data-ttu-id="9a569-105">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="9a569-105">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="9a569-106">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="9a569-106">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9a569-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9a569-107">Az.Compute</span></span>
* <span data-ttu-id="9a569-108">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="9a569-108">Proximity placement group feature.</span></span>
    - <span data-ttu-id="9a569-109">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="9a569-109">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="9a569-110">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="9a569-110">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="9a569-111">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="9a569-111">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="9a569-112">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="9a569-112">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="9a569-113">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="9a569-113">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="9a569-114">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="9a569-114">Breaking changes</span></span>
    - <span data-ttu-id="9a569-115">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="9a569-115">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="9a569-116">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="9a569-116">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="9a569-117">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="9a569-117">Az.DeploymentManager</span></span>
* <span data-ttu-id="9a569-118">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="9a569-118">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="9a569-119">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="9a569-119">Az.Dns</span></span>
* <span data-ttu-id="9a569-120">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="9a569-120">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="9a569-121">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-121">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="9a569-122">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="9a569-122">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="9a569-123">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="9a569-123">Az.FrontDoor</span></span>
* <span data-ttu-id="9a569-124">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="9a569-124">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="9a569-125">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="9a569-125">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="9a569-126">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="9a569-126">Az.HDInsight</span></span>
* <span data-ttu-id="9a569-127">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="9a569-127">Removed two cmdlets:</span></span>
    - <span data-ttu-id="9a569-128">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9a569-128">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="9a569-129">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9a569-129">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="9a569-130">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="9a569-130">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="9a569-131">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="9a569-131">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="9a569-132">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="9a569-132">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="9a569-133">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="9a569-133">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="9a569-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9a569-134">Az.Monitor</span></span>
* <span data-ttu-id="9a569-135">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="9a569-135">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="9a569-136">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="9a569-136">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="9a569-137">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="9a569-137">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="9a569-138">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="9a569-138">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="9a569-139">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="9a569-139">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="9a569-140">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="9a569-140">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="9a569-141">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="9a569-141">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="9a569-142">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="9a569-142">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="9a569-143">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="9a569-143">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="9a569-144">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="9a569-144">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="9a569-145">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="9a569-145">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="9a569-146">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="9a569-146">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="9a569-147">[További](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="9a569-147">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="9a569-148">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="9a569-148">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9a569-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9a569-149">Az.Network</span></span>
* <span data-ttu-id="9a569-150">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="9a569-150">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="9a569-151">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9a569-151">New cmdlets</span></span>
        - <span data-ttu-id="9a569-152">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="9a569-152">New-AzNatGateway</span></span>
        - <span data-ttu-id="9a569-153">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="9a569-153">Get-AzNatGateway</span></span>
        - <span data-ttu-id="9a569-154">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="9a569-154">Set-AzNatGateway</span></span>
        - <span data-ttu-id="9a569-155">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="9a569-155">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="9a569-156">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9a569-156">Updated cmdlets</span></span>
        - <span data-ttu-id="9a569-157">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="9a569-157">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="9a569-158">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="9a569-158">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="9a569-159">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="9a569-159">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="9a569-160">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="9a569-160">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="9a569-161">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="9a569-161">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="9a569-162">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="9a569-162">Az.PolicyInsights</span></span>
* <span data-ttu-id="9a569-163">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="9a569-163">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="9a569-164">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="9a569-164">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="9a569-165">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="9a569-165">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9a569-166">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9a569-166">Az.RecoveryServices</span></span>
* <span data-ttu-id="9a569-167">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="9a569-167">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="9a569-168">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="9a569-168">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="9a569-169">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="9a569-169">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="9a569-170">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="9a569-170">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="9a569-171">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="9a569-171">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="9a569-172">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="9a569-172">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="9a569-173">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="9a569-173">Az.Relay</span></span>
* <span data-ttu-id="9a569-174">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="9a569-174">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="9a569-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9a569-175">Az.ServiceBus</span></span>
* <span data-ttu-id="9a569-176">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="9a569-176">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9a569-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9a569-177">Az.Storage</span></span>
* <span data-ttu-id="9a569-178">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="9a569-178">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="9a569-179">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="9a569-179">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="9a569-180">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="9a569-180">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="9a569-181">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a569-181">New-AzStorageAccount</span></span>
* <span data-ttu-id="9a569-182">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="9a569-182">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="9a569-183">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a569-183">New-AzStorageAccount</span></span>
    - <span data-ttu-id="9a569-184">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a569-184">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="9a569-185">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a569-185">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9a569-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9a569-186">Az.Websites</span></span>
* <span data-ttu-id="9a569-187">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="9a569-187">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="9a569-188">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="9a569-188">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="9a569-189">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="9a569-189">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="9a569-190">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="9a569-190">Highlights since the last major release</span></span>
* <span data-ttu-id="9a569-191">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="9a569-191">General availability of `Az` module</span></span>
* <span data-ttu-id="9a569-192">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="9a569-192">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="9a569-193">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="9a569-193">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="9a569-194">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-194">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="9a569-195">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-195">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="9a569-196">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-196">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="9a569-197">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="9a569-197">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="9a569-198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9a569-198">Az.Accounts</span></span>
* <span data-ttu-id="9a569-199">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="9a569-199">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="9a569-200">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="9a569-200">Az.Batch</span></span>
* <span data-ttu-id="9a569-201">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="9a569-202">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="9a569-202">Az.Cdn</span></span>
* <span data-ttu-id="9a569-203">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="9a569-204">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9a569-204">Az.CognitiveServices</span></span>
* <span data-ttu-id="9a569-205">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9a569-206">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9a569-206">Az.Compute</span></span>
* <span data-ttu-id="9a569-207">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="9a569-207">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="9a569-208">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="9a569-209">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="9a569-209">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9a569-210">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9a569-210">Az.DataFactory</span></span>
* <span data-ttu-id="9a569-211">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="9a569-211">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9a569-212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9a569-212">Az.DataLakeStore</span></span>
* <span data-ttu-id="9a569-213">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-213">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="9a569-214">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="9a569-214">Az.EventGrid</span></span>
* <span data-ttu-id="9a569-215">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="9a569-215">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="9a569-216">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="9a569-216">Az.EventHub</span></span>
* <span data-ttu-id="9a569-217">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="9a569-217">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="9a569-218">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="9a569-218">Az.HDInsight</span></span>
* <span data-ttu-id="9a569-219">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="9a569-220">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="9a569-220">Az.IotHub</span></span>
* <span data-ttu-id="9a569-221">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-221">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="9a569-222">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9a569-222">Az.KeyVault</span></span>
* <span data-ttu-id="9a569-223">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-223">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="9a569-224">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="9a569-224">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="9a569-225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="9a569-225">Az.MachineLearning</span></span>
* <span data-ttu-id="9a569-226">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-226">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="9a569-227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="9a569-227">Az.Media</span></span>
* <span data-ttu-id="9a569-228">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-228">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="9a569-229">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9a569-229">Az.Monitor</span></span>
  * <span data-ttu-id="9a569-230">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9a569-230">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="9a569-231">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="9a569-231">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="9a569-232">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="9a569-232">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="9a569-233">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="9a569-233">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="9a569-234">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="9a569-234">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="9a569-235">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="9a569-235">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="9a569-236">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="9a569-236">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9a569-237">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9a569-237">Az.Network</span></span>
* <span data-ttu-id="9a569-238">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="9a569-239">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="9a569-239">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="9a569-240">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="9a569-240">Az.NotificationHubs</span></span>
* <span data-ttu-id="9a569-241">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-241">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="9a569-242">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9a569-242">Az.OperationalInsights</span></span>
* <span data-ttu-id="9a569-243">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="9a569-244">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="9a569-244">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="9a569-245">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9a569-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9a569-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="9a569-247">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-247">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="9a569-248">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="9a569-248">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="9a569-249">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="9a569-249">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="9a569-250">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="9a569-250">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="9a569-251">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="9a569-251">Az.RedisCache</span></span>
* <span data-ttu-id="9a569-252">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="9a569-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9a569-253">Az.Resources</span></span>
* <span data-ttu-id="9a569-254">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="9a569-254">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="9a569-255">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9a569-255">Az.Sql</span></span>
* <span data-ttu-id="9a569-256">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="9a569-256">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="9a569-257">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="9a569-258">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="9a569-258">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="9a569-259">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9a569-259">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="9a569-260">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="9a569-260">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="9a569-261">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="9a569-261">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="9a569-262">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="9a569-262">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9a569-263">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9a569-263">Az.Websites</span></span>
* <span data-ttu-id="9a569-264">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="9a569-264">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="9a569-265">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="9a569-265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="9a569-266">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="9a569-266">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="9a569-267">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="9a569-267">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="9a569-268">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="9a569-268">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="9a569-269">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="9a569-269">Highlights since the last major release</span></span>
* <span data-ttu-id="9a569-270">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="9a569-270">General availability of `Az` module</span></span>
* <span data-ttu-id="9a569-271">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="9a569-271">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="9a569-272">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="9a569-272">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="9a569-273">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-273">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="9a569-274">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-274">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="9a569-275">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-275">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="9a569-276">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="9a569-276">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="9a569-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9a569-277">Az.Accounts</span></span>
* <span data-ttu-id="9a569-278">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="9a569-278">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="9a569-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9a569-279">Az.AnalysisServices</span></span>
* <span data-ttu-id="9a569-280">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9a569-280">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="9a569-281">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="9a569-281">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9a569-282">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9a569-282">Az.Automation</span></span>
* <span data-ttu-id="9a569-283">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="9a569-283">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="9a569-284">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="9a569-284">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="9a569-285">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-285">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9a569-286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9a569-286">Az.Compute</span></span>
* <span data-ttu-id="9a569-287">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="9a569-287">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="9a569-288">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="9a569-288">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="9a569-289">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9a569-289">Az.ContainerInstance</span></span>
* <span data-ttu-id="9a569-290">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="9a569-290">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9a569-291">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9a569-291">Az.DataFactory</span></span>
* <span data-ttu-id="9a569-292">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="9a569-292">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="9a569-293">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="9a569-293">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="9a569-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9a569-294">Az.Resources</span></span>
* <span data-ttu-id="9a569-295">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="9a569-295">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="9a569-296">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-296">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="9a569-297">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="9a569-297">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="9a569-298">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="9a569-298">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="9a569-299">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="9a569-299">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="9a569-300">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="9a569-300">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="9a569-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9a569-301">Az.Sql</span></span>
* <span data-ttu-id="9a569-302">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="9a569-302">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9a569-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9a569-303">Az.Storage</span></span>
* <span data-ttu-id="9a569-304">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="9a569-304">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="9a569-305">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="9a569-305">New-AzStorageContext</span></span>
* <span data-ttu-id="9a569-306">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="9a569-306">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="9a569-307">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="9a569-307">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="9a569-308">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="9a569-308">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="9a569-309">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9a569-309">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="9a569-310">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9a569-310">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="9a569-311">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="9a569-311">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="9a569-312">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9a569-312">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="9a569-313">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9a569-313">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="9a569-314">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9a569-314">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="9a569-315">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9a569-315">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="9a569-316">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="9a569-316">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="9a569-317">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="9a569-317">Highlights since the last major release</span></span>
* <span data-ttu-id="9a569-318">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="9a569-318">General availability of `Az` module</span></span>
* <span data-ttu-id="9a569-319">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="9a569-319">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="9a569-320">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="9a569-320">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="9a569-321">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-321">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="9a569-322">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-322">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="9a569-323">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-323">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="9a569-324">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="9a569-324">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9a569-325">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9a569-325">Az.Automation</span></span>
* <span data-ttu-id="9a569-326">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="9a569-326">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="9a569-327">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="9a569-327">Dynamic grouping</span></span>
    * <span data-ttu-id="9a569-328">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="9a569-328">Pre-Post script</span></span>
    * <span data-ttu-id="9a569-329">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="9a569-329">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9a569-330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9a569-330">Az.Compute</span></span>
* <span data-ttu-id="9a569-331">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-331">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="9a569-332">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="9a569-332">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="9a569-333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9a569-333">Az.KeyVault</span></span>
* <span data-ttu-id="9a569-334">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="9a569-334">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9a569-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9a569-335">Az.Network</span></span>
* <span data-ttu-id="9a569-336">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="9a569-336">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="9a569-337">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="9a569-337">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9a569-338">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9a569-338">Az.RecoveryServices</span></span>
* <span data-ttu-id="9a569-339">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="9a569-339">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="9a569-340">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="9a569-340">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="9a569-341">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9a569-341">Az.Resources</span></span>
* <span data-ttu-id="9a569-342">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-342">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="9a569-343">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="9a569-343">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="9a569-344">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9a569-344">Az.Sql</span></span>
* <span data-ttu-id="9a569-345">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="9a569-345">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9a569-346">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9a569-346">Az.Storage</span></span>
* <span data-ttu-id="9a569-347">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="9a569-347">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="9a569-348">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9a569-348">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="9a569-349">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9a569-349">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="9a569-350">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9a569-350">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="9a569-351">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="9a569-351">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="9a569-352">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="9a569-352">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="9a569-353">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="9a569-353">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9a569-354">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9a569-354">Az.Websites</span></span>
* <span data-ttu-id="9a569-355">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="9a569-355">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="9a569-356">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="9a569-356">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9a569-357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9a569-357">Az.Accounts</span></span>
* <span data-ttu-id="9a569-358">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="9a569-358">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="9a569-359">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="9a569-359">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9a569-360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9a569-360">Az.Automation</span></span>
* <span data-ttu-id="9a569-361">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-361">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="9a569-362">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="9a569-362">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="9a569-363">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="9a569-363">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="9a569-364">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="9a569-364">Az.Cdn</span></span>
* <span data-ttu-id="9a569-365">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="9a569-365">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9a569-366">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9a569-366">Az.Compute</span></span>
* <span data-ttu-id="9a569-367">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="9a569-367">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9a569-368">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9a569-368">Az.DataFactory</span></span>
* <span data-ttu-id="9a569-369">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="9a569-369">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="9a569-370">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9a569-370">Az.LogicApp</span></span>
* <span data-ttu-id="9a569-371">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="9a569-371">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9a569-372">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9a569-372">Az.Network</span></span>
* <span data-ttu-id="9a569-373">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="9a569-373">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9a569-374">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9a569-374">Az.RecoveryServices</span></span>
* <span data-ttu-id="9a569-375">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="9a569-375">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="9a569-376">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="9a569-376">SDK Update</span></span>
* <span data-ttu-id="9a569-377">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="9a569-377">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="9a569-378">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="9a569-378">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="9a569-379">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9a569-379">Az.Resources</span></span>
* <span data-ttu-id="9a569-380">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="9a569-380">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="9a569-381">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="9a569-381">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="9a569-382">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="9a569-382">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="9a569-383">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="9a569-383">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="9a569-384">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="9a569-384">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="9a569-385">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="9a569-385">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="9a569-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9a569-386">Az.Sql</span></span>
* <span data-ttu-id="9a569-387">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="9a569-387">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="9a569-388">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="9a569-388">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9a569-389">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9a569-389">Az.Storage</span></span>
* <span data-ttu-id="9a569-390">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a569-390">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="9a569-391">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="9a569-391">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="9a569-392">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9a569-392">Az.AnalysisServices</span></span>
* <span data-ttu-id="9a569-393">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="9a569-393">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9a569-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9a569-394">Az.Automation</span></span>
* <span data-ttu-id="9a569-395">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="9a569-395">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="9a569-396">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="9a569-396">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="9a569-397">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-397">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="9a569-398">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9a569-398">Az.CognitiveServices</span></span>
* <span data-ttu-id="9a569-399">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="9a569-399">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9a569-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9a569-400">Az.Compute</span></span>
* <span data-ttu-id="9a569-401">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="9a569-401">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="9a569-402">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="9a569-402">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="9a569-403">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="9a569-403">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="9a569-404">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="9a569-404">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9a569-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9a569-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="9a569-406">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="9a569-406">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="9a569-407">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="9a569-407">Az.EventHub</span></span>
* <span data-ttu-id="9a569-408">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="9a569-408">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="9a569-409">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9a569-409">Az.KeyVault</span></span>
* <span data-ttu-id="9a569-410">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="9a569-410">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="9a569-411">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9a569-411">Az.LogicApp</span></span>
* <span data-ttu-id="9a569-412">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="9a569-412">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="9a569-413">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="9a569-413">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="9a569-414">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="9a569-414">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="9a569-415">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="9a569-415">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="9a569-416">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="9a569-416">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="9a569-417">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="9a569-417">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="9a569-418">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="9a569-418">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="9a569-419">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="9a569-419">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="9a569-420">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a569-420">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="9a569-421">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a569-421">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="9a569-422">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a569-422">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="9a569-423">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a569-423">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="9a569-424">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="9a569-424">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="9a569-425">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9a569-425">Az.Monitor</span></span>
* <span data-ttu-id="9a569-426">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="9a569-426">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9a569-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9a569-427">Az.Network</span></span>
* <span data-ttu-id="9a569-428">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="9a569-428">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="9a569-429">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9a569-429">Az.OperationalInsights</span></span>
* <span data-ttu-id="9a569-430">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="9a569-430">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="9a569-431">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="9a569-431">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="9a569-432">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="9a569-432">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="9a569-433">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9a569-433">Az.Resources</span></span>
* <span data-ttu-id="9a569-434">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="9a569-434">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="9a569-435">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="9a569-435">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="9a569-436">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="9a569-436">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="9a569-437">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="9a569-437">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="9a569-438">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9a569-438">Az.Sql</span></span>
* <span data-ttu-id="9a569-439">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="9a569-439">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="9a569-440">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="9a569-440">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9a569-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9a569-441">Az.Websites</span></span>
* <span data-ttu-id="9a569-442">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="9a569-442">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="9a569-443">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="9a569-443">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9a569-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9a569-444">Az.Accounts</span></span>
* <span data-ttu-id="9a569-445">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="9a569-445">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="9a569-446">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9a569-446">Az.AnalysisServices</span></span>
<span data-ttu-id="9a569-447">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="9a569-447">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9a569-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9a569-448">Az.Compute</span></span>
* <span data-ttu-id="9a569-449">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="9a569-449">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="9a569-450">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="9a569-450">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="9a569-451">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="9a569-451">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9a569-452">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9a569-452">Az.RecoveryServices</span></span>
<span data-ttu-id="9a569-453">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="9a569-453">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="9a569-454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9a569-454">Az.Resources</span></span>
* <span data-ttu-id="9a569-455">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="9a569-455">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="9a569-456">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="9a569-456">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="9a569-457">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="9a569-457">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="9a569-458">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="9a569-458">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="9a569-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9a569-459">Az.Sql</span></span>
* <span data-ttu-id="9a569-460">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="9a569-460">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="9a569-461">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="9a569-461">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="9a569-462">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="9a569-462">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="9a569-463">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="9a569-463">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9a569-464">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9a569-464">Az.Accounts</span></span>
* <span data-ttu-id="9a569-465">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="9a569-465">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="9a569-466">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9a569-466">Az.AnalysisServices</span></span>
* <span data-ttu-id="9a569-467">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="9a569-467">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9a569-468">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9a569-468">Az.RecoveryServices</span></span>
* <span data-ttu-id="9a569-469">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="9a569-469">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="9a569-470">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="9a569-470">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9a569-471">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9a569-471">Az.Accounts</span></span>
* <span data-ttu-id="9a569-472">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-472">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="9a569-473">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="9a569-473">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9a569-474">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="9a569-474">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="9a569-475">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="9a569-475">Az.Aks</span></span>
* <span data-ttu-id="9a569-476">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="9a569-476">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9a569-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9a569-477">Az.Automation</span></span>
* <span data-ttu-id="9a569-478">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="9a569-478">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="9a569-479">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="9a569-479">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="9a569-480">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="9a569-480">Az.Cdn</span></span>
* <span data-ttu-id="9a569-481">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="9a569-481">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9a569-482">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9a569-482">Az.Compute</span></span>
* <span data-ttu-id="9a569-483">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="9a569-483">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="9a569-484">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="9a569-484">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="9a569-485">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="9a569-485">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="9a569-486">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9a569-486">Az.ContainerRegistry</span></span>
* <span data-ttu-id="9a569-487">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="9a569-487">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9a569-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9a569-488">Az.DataFactory</span></span>
* <span data-ttu-id="9a569-489">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="9a569-489">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9a569-490">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9a569-490">Az.DataLakeStore</span></span>
* <span data-ttu-id="9a569-491">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="9a569-491">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="9a569-492">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="9a569-492">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="9a569-493">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="9a569-493">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="9a569-494">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="9a569-494">Az.IotHub</span></span>
* <span data-ttu-id="9a569-495">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="9a569-495">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="9a569-496">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9a569-496">Az.KeyVault</span></span>
* <span data-ttu-id="9a569-497">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="9a569-497">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9a569-498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9a569-498">Az.Network</span></span>
* <span data-ttu-id="9a569-499">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="9a569-499">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="9a569-500">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9a569-500">Az.Resources</span></span>
* <span data-ttu-id="9a569-501">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="9a569-501">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="9a569-502">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="9a569-502">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="9a569-503">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="9a569-503">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="9a569-504">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="9a569-504">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="9a569-505">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="9a569-505">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="9a569-506">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="9a569-506">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="9a569-507">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="9a569-507">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="9a569-508">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9a569-508">Az.ServiceFabric</span></span>
* <span data-ttu-id="9a569-509">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="9a569-509">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="9a569-510">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="9a569-510">Fix some error messages.</span></span>
* <span data-ttu-id="9a569-511">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="9a569-511">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="9a569-512">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="9a569-512">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="9a569-513">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="9a569-513">Az.SignalR</span></span>
* <span data-ttu-id="9a569-514">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="9a569-514">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="9a569-515">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9a569-515">Az.Sql</span></span>
* <span data-ttu-id="9a569-516">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="9a569-516">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9a569-517">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="9a569-517">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="9a569-518">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="9a569-518">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="9a569-519">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="9a569-519">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9a569-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9a569-520">Az.Storage</span></span>
* <span data-ttu-id="9a569-521">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="9a569-521">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9a569-522">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="9a569-522">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="9a569-523">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="9a569-523">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="9a569-524">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="9a569-524">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="9a569-525">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="9a569-525">Az.TrafficManager</span></span>
* <span data-ttu-id="9a569-526">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="9a569-526">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9a569-527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9a569-527">Az.Websites</span></span>
* <span data-ttu-id="9a569-528">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="9a569-528">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9a569-529">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="9a569-529">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="9a569-530">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="9a569-530">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="9a569-531">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="9a569-531">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9a569-532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9a569-532">Az.Accounts</span></span>
* <span data-ttu-id="9a569-533">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="9a569-533">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9a569-534">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9a569-534">Az.Compute</span></span>
* <span data-ttu-id="9a569-535">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="9a569-535">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="9a569-536">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="9a569-536">Updated the description of ID in help files</span></span>
* <span data-ttu-id="9a569-537">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="9a569-537">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9a569-538">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9a569-538">Az.DataLakeStore</span></span>
* <span data-ttu-id="9a569-539">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="9a569-539">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="9a569-540">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="9a569-540">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="9a569-541">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="9a569-541">Az.EventGrid</span></span>
* <span data-ttu-id="9a569-542">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="9a569-542">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="9a569-543">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="9a569-543">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="9a569-544">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="9a569-544">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="9a569-545">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="9a569-545">Event Time-To-Live,</span></span>
        - <span data-ttu-id="9a569-546">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="9a569-546">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="9a569-547">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="9a569-547">Dead letter endpoint.</span></span>
    - <span data-ttu-id="9a569-548">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="9a569-548">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="9a569-549">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="9a569-549">Event Time-To-Live,</span></span>
        - <span data-ttu-id="9a569-550">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="9a569-550">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="9a569-551">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="9a569-551">Dead letter endpoint.</span></span>
* <span data-ttu-id="9a569-552">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="9a569-552">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="9a569-553">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="9a569-553">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="9a569-554">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="9a569-554">Az.IotHub</span></span>
* <span data-ttu-id="9a569-555">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="9a569-555">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="9a569-556">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9a569-556">Az.LogicApp</span></span>
* <span data-ttu-id="9a569-557">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="9a569-557">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="9a569-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9a569-558">Az.Resources</span></span>
* <span data-ttu-id="9a569-559">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="9a569-559">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="9a569-560">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="9a569-560">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="9a569-561">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="9a569-561">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="9a569-562">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="9a569-562">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="9a569-563">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="9a569-563">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="9a569-564">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="9a569-564">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="9a569-565">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="9a569-565">Az.SignalR</span></span>
* <span data-ttu-id="9a569-566">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="9a569-566">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="9a569-567">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9a569-567">Az.Sql</span></span>
* <span data-ttu-id="9a569-568">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="9a569-568">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9a569-569">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9a569-569">Az.Storage</span></span>
* <span data-ttu-id="9a569-570">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="9a569-570">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="9a569-571">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="9a569-571">New-AzStorageContext</span></span>
* <span data-ttu-id="9a569-572">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="9a569-572">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="9a569-573">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="9a569-573">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9a569-574">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9a569-574">Az.Websites</span></span>
* <span data-ttu-id="9a569-575">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="9a569-575">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="9a569-576">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="9a569-576">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="9a569-577">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="9a569-577">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="9a569-578">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="9a569-578">General</span></span>

- <span data-ttu-id="9a569-579">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="9a569-579">General Availability of Az Module</span></span>
- <span data-ttu-id="9a569-580">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="9a569-580">Online help for each module</span></span>
- <span data-ttu-id="9a569-581">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="9a569-581">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="9a569-582">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="9a569-582">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="9a569-583">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9a569-583">Az.Accounts</span></span>
- <span data-ttu-id="9a569-584">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="9a569-584">Changed from Az.Profile</span></span>
- <span data-ttu-id="9a569-585">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="9a569-585">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="9a569-586">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9a569-586">Az.ApiManagement</span></span>
- <span data-ttu-id="9a569-587">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="9a569-587">Fixes for #7002</span></span>
- <span data-ttu-id="9a569-588">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="9a569-588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="9a569-589">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="9a569-589">Az.Batch</span></span>
- <span data-ttu-id="9a569-590">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="9a569-590">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="9a569-591">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="9a569-591">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="9a569-592">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="9a569-592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="9a569-593">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="9a569-593">Az.Billing</span></span>
- <span data-ttu-id="9a569-594">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="9a569-594">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="9a569-595">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="9a569-595">Az.CognitivServices</span></span>
- <span data-ttu-id="9a569-596">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="9a569-596">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="9a569-597">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="9a569-597">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="9a569-598">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9a569-598">Az.ContainerInstance</span></span>
- <span data-ttu-id="9a569-599">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="9a569-599">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="9a569-600">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="9a569-600">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="9a569-601">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="9a569-601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="9a569-602">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9a569-602">Az.DataLakeStore</span></span>
- <span data-ttu-id="9a569-603">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="9a569-603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="9a569-604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9a569-604">Az.Monitor</span></span>
- <span data-ttu-id="9a569-605">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="9a569-605">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="9a569-606">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9a569-606">Az.KeyVault</span></span>
- <span data-ttu-id="9a569-607">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="9a569-607">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="9a569-608">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="9a569-608">Az.MachineLearning</span></span>
- <span data-ttu-id="9a569-609">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="9a569-609">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="9a569-610">Az.Media</span><span class="sxs-lookup"><span data-stu-id="9a569-610">Az.Media</span></span>
- <span data-ttu-id="9a569-611">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="9a569-611">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="9a569-612">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9a569-612">Az.Network</span></span>
<span data-ttu-id="9a569-613">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="9a569-613">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="9a569-614">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="9a569-614">New cmdlets added:</span></span>
        - <span data-ttu-id="9a569-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a569-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9a569-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a569-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9a569-617">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a569-617">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9a569-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a569-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9a569-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a569-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9a569-620">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="9a569-620">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="9a569-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="9a569-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="9a569-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a569-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="9a569-623">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9a569-623">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="9a569-624">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9a569-624">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="9a569-625">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9a569-625">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="9a569-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9a569-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="9a569-627">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a569-627">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="9a569-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9a569-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="9a569-629">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="9a569-629">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="9a569-630">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9a569-630">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="9a569-631">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9a569-631">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="9a569-632">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9a569-632">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="9a569-633">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9a569-633">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="9a569-634">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="9a569-634">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="9a569-635">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="9a569-635">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="9a569-636">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9a569-636">Az.OperationalInsights</span></span>
- <span data-ttu-id="9a569-637">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="9a569-637">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="9a569-638">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9a569-638">Az.Profile</span></span>
- <span data-ttu-id="9a569-639">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9a569-639">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="9a569-640">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9a569-640">Az.RecoveryServices</span></span>
- <span data-ttu-id="9a569-641">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="9a569-641">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="9a569-642">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9a569-642">Az.Resources</span></span>
- <span data-ttu-id="9a569-643">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="9a569-643">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="9a569-644">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9a569-644">Az.ServiceFabric</span></span>
- <span data-ttu-id="9a569-645">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="9a569-645">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="9a569-646">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="9a569-646">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="9a569-647">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="9a569-647">Az.SIgnalR</span></span>
- <span data-ttu-id="9a569-648">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="9a569-648">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="9a569-649">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9a569-649">Az.Sql</span></span>
- <span data-ttu-id="9a569-650">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="9a569-650">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="9a569-651">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="9a569-651">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="9a569-652">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="9a569-652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="9a569-653">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9a569-653">Az.Storage</span></span>
- <span data-ttu-id="9a569-654">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="9a569-654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="9a569-655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9a569-655">Az.Websites</span></span>
- <span data-ttu-id="9a569-656">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="9a569-656">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="9a569-657">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="9a569-657">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="9a569-658">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="9a569-658">General</span></span>

* <span data-ttu-id="9a569-659">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="9a569-659">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="9a569-660">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9a569-660">Az.Compute</span></span>

* <span data-ttu-id="9a569-661">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="9a569-661">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="9a569-662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9a569-662">Az.DataLakeStore</span></span>

* <span data-ttu-id="9a569-663">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="9a569-663">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="9a569-664">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="9a569-664">Az.FrontDoor</span></span>

* <span data-ttu-id="9a569-665">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="9a569-665">Fixed some broken links</span></span>
    - <span data-ttu-id="9a569-666">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="9a569-666">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="9a569-667">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="9a569-667">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="9a569-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9a569-668">Az.RecoveryServices</span></span>

* <span data-ttu-id="9a569-669">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="9a569-669">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="9a569-670">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="9a569-670">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="9a569-671">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9a569-671">Az.Resources</span></span>

* <span data-ttu-id="9a569-672">https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="9a569-672">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="9a569-673">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="9a569-673">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="9a569-674">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9a569-674">Az.Sql</span></span>

* <span data-ttu-id="9a569-675">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="9a569-675">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="9a569-676">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="9a569-676">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="9a569-677">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="9a569-677">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="9a569-678">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9a569-678">Az.Storage</span></span>

* <span data-ttu-id="9a569-679">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="9a569-679">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="9a569-680">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="9a569-680">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="9a569-681">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9a569-681">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="9a569-682">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="9a569-682">Support Static Website configuration</span></span>
    - <span data-ttu-id="9a569-683">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="9a569-683">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="9a569-684">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="9a569-684">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="9a569-685">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9a569-685">Az.Websites</span></span>

* <span data-ttu-id="9a569-686">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9a569-686">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="9a569-687">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="9a569-687">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="9a569-688">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="9a569-688">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="9a569-689">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="9a569-689">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="9a569-690">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9a569-690">Az.ApiManagement</span></span>
* <span data-ttu-id="9a569-691">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="9a569-691">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="9a569-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9a569-692">Az.Automation</span></span>
* <span data-ttu-id="9a569-693">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="9a569-693">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="9a569-694">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="9a569-694">Added Update Management cmdlets</span></span>
* <span data-ttu-id="9a569-695">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="9a569-695">Added Source Control cmdlets</span></span>
* <span data-ttu-id="9a569-696">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="9a569-696">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="9a569-697">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="9a569-697">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="9a569-698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9a569-698">Az.Compute</span></span>
* <span data-ttu-id="9a569-699">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="9a569-699">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="9a569-700">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="9a569-700">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="9a569-701">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9a569-701">Az.ContainerInstance</span></span>
* <span data-ttu-id="9a569-702">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="9a569-702">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="9a569-703">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="9a569-703">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="9a569-704">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="9a569-704">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="9a569-705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9a569-705">Az.Network</span></span>
* <span data-ttu-id="9a569-706">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="9a569-706">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="9a569-707">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="9a569-707">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="9a569-708">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="9a569-708">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="9a569-709">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="9a569-709">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="9a569-710">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="9a569-710">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="9a569-711">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="9a569-711">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="9a569-712">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="9a569-712">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="9a569-713">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="9a569-713">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="9a569-714">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="9a569-714">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="9a569-715">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="9a569-715">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="9a569-716">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="9a569-716">Az.Relay</span></span>
* <span data-ttu-id="9a569-717">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="9a569-717">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="9a569-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9a569-718">Az.Resources</span></span>
* <span data-ttu-id="9a569-719">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="9a569-719">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="9a569-720">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="9a569-720">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="9a569-721">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="9a569-721">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="9a569-722">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9a569-722">Az.ServiceFabric</span></span>
* <span data-ttu-id="9a569-723">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="9a569-723">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="9a569-724">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9a569-724">Az.Sql</span></span>
* <span data-ttu-id="9a569-725">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="9a569-725">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="9a569-726">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9a569-726">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9a569-727">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9a569-727">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9a569-728">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9a569-728">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9a569-729">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9a569-729">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9a569-730">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9a569-730">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="9a569-731">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9a569-731">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="9a569-732">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9a569-732">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="9a569-733">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9a569-733">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="9a569-734">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="9a569-734">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="9a569-735">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="9a569-735">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="9a569-736">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="9a569-736">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="9a569-737">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="9a569-737">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="9a569-738">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="9a569-738">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="9a569-739">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="9a569-739">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="9a569-740">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="9a569-740">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="9a569-741">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="9a569-741">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="9a569-742">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="9a569-742">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="9a569-743">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="9a569-743">General</span></span>
* <span data-ttu-id="9a569-744">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="9a569-744">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="9a569-745">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9a569-745">Az.Profile</span></span>
* <span data-ttu-id="9a569-746">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="9a569-746">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="9a569-747">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="9a569-747">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="9a569-748">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="9a569-748">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="9a569-749">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="9a569-749">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="9a569-750">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="9a569-750">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="9a569-751">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="9a569-751">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="9a569-752">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="9a569-752">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="9a569-753">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9a569-753">Az.CognitiveServices</span></span>
* <span data-ttu-id="9a569-754">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="9a569-754">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9a569-755">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9a569-755">Az.Compute</span></span>
* <span data-ttu-id="9a569-756">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="9a569-756">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="9a569-757">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="9a569-757">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="9a569-758">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="9a569-758">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9a569-759">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9a569-759">Az.DataLakeStore</span></span>
* <span data-ttu-id="9a569-760">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="9a569-760">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="9a569-761">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="9a569-761">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="9a569-762">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="9a569-762">Az.Insights</span></span>
* <span data-ttu-id="9a569-763">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="9a569-763">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="9a569-764">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="9a569-764">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="9a569-765">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="9a569-765">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="9a569-766">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="9a569-766">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9a569-767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9a569-767">Az.Network</span></span>
* <span data-ttu-id="9a569-768">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="9a569-768">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="9a569-769">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="9a569-769">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="9a569-770">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="9a569-770">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="9a569-771">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="9a569-771">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="9a569-772">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="9a569-772">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="9a569-773">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="9a569-773">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="9a569-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="9a569-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="9a569-775">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="9a569-775">Az.PolicyInsights</span></span>
* <span data-ttu-id="9a569-776">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="9a569-776">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="9a569-777">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9a569-777">Az.Resources</span></span>
* <span data-ttu-id="9a569-778">https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="9a569-778">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="9a569-779">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="9a569-779">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="9a569-780">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9a569-780">Az.ServiceBus</span></span>
* <span data-ttu-id="9a569-781">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="9a569-781">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="9a569-782">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9a569-782">Az.ServiceFabric</span></span>
* <span data-ttu-id="9a569-783">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="9a569-783">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="9a569-784">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="9a569-784">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="9a569-785">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="9a569-785">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="9a569-786">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="9a569-786">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="9a569-787">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="9a569-787">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="9a569-788">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="9a569-788">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="9a569-789">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9a569-789">Az.Profile</span></span>
* <span data-ttu-id="9a569-790">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="9a569-790">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="9a569-791">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="9a569-791">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9a569-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9a569-792">Az.Compute</span></span>
* <span data-ttu-id="9a569-793">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="9a569-793">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="9a569-794">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="9a569-794">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9a569-795">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9a569-795">Az.DataLakeStore</span></span>
* <span data-ttu-id="9a569-796">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="9a569-796">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="9a569-797">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="9a569-797">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="9a569-798">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="9a569-798">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="9a569-799">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="9a569-799">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="9a569-800">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="9a569-800">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9a569-801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9a569-801">Az.Network</span></span>
* <span data-ttu-id="9a569-802">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="9a569-802">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="9a569-803">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="9a569-803">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="9a569-804">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9a569-804">Az.Resources</span></span>
* <span data-ttu-id="9a569-805">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="9a569-805">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="9a569-806">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="9a569-806">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="9a569-807">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="9a569-807">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="9a569-808">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="9a569-808">Azure.Storage</span></span>
* <span data-ttu-id="9a569-809">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="9a569-809">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="9a569-810">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="9a569-810">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="9a569-811">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9a569-811">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="9a569-812">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="9a569-812">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="9a569-813">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="9a569-813">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="9a569-814">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9a569-814">Az.CognitiveServices</span></span>
* <span data-ttu-id="9a569-815">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="9a569-815">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9a569-816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9a569-816">Az.Compute</span></span>
* <span data-ttu-id="9a569-817">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="9a569-817">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="9a569-818">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="9a569-818">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="9a569-819">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="9a569-819">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="9a569-820">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9a569-820">Az.DataFactoryV2</span></span>
* <span data-ttu-id="9a569-821">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="9a569-821">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9a569-822">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9a569-822">Az.Network</span></span>
* <span data-ttu-id="9a569-823">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="9a569-823">Added NetworkProfile functionality.</span></span> <span data-ttu-id="9a569-824">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="9a569-824">new cmdlets added</span></span>
    - <span data-ttu-id="9a569-825">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9a569-825">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="9a569-826">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9a569-826">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="9a569-827">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9a569-827">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="9a569-828">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9a569-828">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="9a569-829">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="9a569-829">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="9a569-830">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="9a569-830">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="9a569-831">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="9a569-831">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="9a569-832">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="9a569-832">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="9a569-833">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="9a569-833">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="9a569-834">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="9a569-834">Az.RedisCache</span></span>
* <span data-ttu-id="9a569-835">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="9a569-835">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="9a569-836">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="9a569-836">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="9a569-837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9a569-837">Az.Resources</span></span>
* <span data-ttu-id="9a569-838">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="9a569-838">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="9a569-839">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="9a569-839">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="9a569-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9a569-840">Az.Sql</span></span>
* <span data-ttu-id="9a569-841">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="9a569-841">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9a569-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9a569-842">Az.Websites</span></span>
* <span data-ttu-id="9a569-843">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="9a569-843">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="9a569-844">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="9a569-844">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="9a569-845">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="9a569-845">0.2.0 - September 2018</span></span>
 <span data-ttu-id="9a569-846">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="9a569-846">Initial Release</span></span>