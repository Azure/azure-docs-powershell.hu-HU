## <a name="100---december-2018"></a><span data-ttu-id="31a62-101">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="31a62-101">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="31a62-102">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="31a62-102">General</span></span>

- <span data-ttu-id="31a62-103">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="31a62-103">General Availability of Az Module</span></span>
- <span data-ttu-id="31a62-104">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="31a62-104">Online help for each module</span></span>
- <span data-ttu-id="31a62-105">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="31a62-105">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="31a62-106">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31a62-106">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="31a62-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31a62-107">Az.Accounts</span></span>
- <span data-ttu-id="31a62-108">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="31a62-108">Changed from Az.Profile</span></span>
- <span data-ttu-id="31a62-109">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="31a62-109">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="31a62-110">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31a62-110">Az.ApiManagement</span></span>
- <span data-ttu-id="31a62-111">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="31a62-111">Fixes for #7002</span></span>
- <span data-ttu-id="31a62-112">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31a62-112">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="31a62-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="31a62-113">Az.Batch</span></span>
- <span data-ttu-id="31a62-114">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="31a62-114">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="31a62-115">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="31a62-115">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="31a62-116">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31a62-116">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="31a62-117">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="31a62-117">Az.Billing</span></span>
- <span data-ttu-id="31a62-118">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="31a62-118">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="31a62-119">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="31a62-119">Az.CognitivServices</span></span>
- <span data-ttu-id="31a62-120">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="31a62-120">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="31a62-121">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="31a62-121">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="31a62-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="31a62-122">Az.ContainerInstance</span></span>
- <span data-ttu-id="31a62-123">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="31a62-123">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="31a62-124">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="31a62-124">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="31a62-125">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31a62-125">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="31a62-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31a62-126">Az.DataLakeStore</span></span>
- <span data-ttu-id="31a62-127">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31a62-127">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="31a62-128">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="31a62-128">Az.Monitor</span></span>
- <span data-ttu-id="31a62-129">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31a62-129">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="31a62-130">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31a62-130">Az.KeyVault</span></span>
- <span data-ttu-id="31a62-131">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="31a62-131">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="31a62-132">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="31a62-132">Az.MachineLearning</span></span>
- <span data-ttu-id="31a62-133">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="31a62-133">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="31a62-134">Az.Media</span><span class="sxs-lookup"><span data-stu-id="31a62-134">Az.Media</span></span>
- <span data-ttu-id="31a62-135">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="31a62-135">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="31a62-136">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31a62-136">Az.Network</span></span>
<span data-ttu-id="31a62-137">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="31a62-137">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="31a62-138">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="31a62-138">New cmdlets added:</span></span>
        - <span data-ttu-id="31a62-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31a62-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="31a62-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31a62-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="31a62-141">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31a62-141">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="31a62-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31a62-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="31a62-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="31a62-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="31a62-144">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="31a62-144">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="31a62-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="31a62-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="31a62-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="31a62-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="31a62-147">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="31a62-147">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="31a62-148">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31a62-148">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="31a62-149">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="31a62-149">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="31a62-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="31a62-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="31a62-151">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31a62-151">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="31a62-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="31a62-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="31a62-153">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="31a62-153">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="31a62-154">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="31a62-154">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="31a62-155">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="31a62-155">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="31a62-156">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="31a62-156">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="31a62-157">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="31a62-157">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="31a62-158">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="31a62-158">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="31a62-159">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31a62-159">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="31a62-160">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="31a62-160">Az.OperationalInsights</span></span>
- <span data-ttu-id="31a62-161">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31a62-161">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="31a62-162">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="31a62-162">Az.Profile</span></span>
- <span data-ttu-id="31a62-163">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="31a62-163">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="31a62-164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31a62-164">Az.RecoveryServices</span></span>
- <span data-ttu-id="31a62-165">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31a62-165">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="31a62-166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31a62-166">Az.Resources</span></span>
- <span data-ttu-id="31a62-167">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31a62-167">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="31a62-168">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31a62-168">Az.ServiceFabric</span></span>
- <span data-ttu-id="31a62-169">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="31a62-169">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="31a62-170">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31a62-170">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="31a62-171">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="31a62-171">Az.SIgnalR</span></span>
- <span data-ttu-id="31a62-172">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="31a62-172">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="31a62-173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31a62-173">Az.Sql</span></span>
- <span data-ttu-id="31a62-174">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="31a62-174">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="31a62-175">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="31a62-175">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="31a62-176">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31a62-176">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="31a62-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31a62-177">Az.Storage</span></span>
- <span data-ttu-id="31a62-178">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31a62-178">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="31a62-179">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31a62-179">Az.Websites</span></span>
- <span data-ttu-id="31a62-180">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="31a62-180">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="31a62-181">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="31a62-181">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="31a62-182">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="31a62-182">General</span></span>

* <span data-ttu-id="31a62-183">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="31a62-183">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="31a62-184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31a62-184">Az.Compute</span></span>

* <span data-ttu-id="31a62-185">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="31a62-185">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="31a62-186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31a62-186">Az.DataLakeStore</span></span>

* <span data-ttu-id="31a62-187">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="31a62-187">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="31a62-188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="31a62-188">Az.FrontDoor</span></span>

* <span data-ttu-id="31a62-189">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="31a62-189">Fixed some broken links</span></span>
    - <span data-ttu-id="31a62-190">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="31a62-190">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="31a62-191">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="31a62-191">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="31a62-192">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31a62-192">Az.RecoveryServices</span></span>

* <span data-ttu-id="31a62-193">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="31a62-193">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="31a62-194">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="31a62-194">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="31a62-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31a62-195">Az.Resources</span></span>

* <span data-ttu-id="31a62-196"> https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="31a62-196">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="31a62-197">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="31a62-197">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="31a62-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31a62-198">Az.Sql</span></span>

* <span data-ttu-id="31a62-199">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="31a62-199">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="31a62-200">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="31a62-200">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="31a62-201">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="31a62-201">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="31a62-202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31a62-202">Az.Storage</span></span>

* <span data-ttu-id="31a62-203">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="31a62-203">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="31a62-204">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="31a62-204">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="31a62-205">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="31a62-205">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="31a62-206">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="31a62-206">Support Static Website configuration</span></span>
    - <span data-ttu-id="31a62-207">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="31a62-207">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="31a62-208">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="31a62-208">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="31a62-209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31a62-209">Az.Websites</span></span>

* <span data-ttu-id="31a62-210">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="31a62-210">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="31a62-211">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="31a62-211">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="31a62-212">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="31a62-212">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="31a62-213">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="31a62-213">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="31a62-214">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31a62-214">Az.ApiManagement</span></span>
* <span data-ttu-id="31a62-215">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="31a62-215">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="31a62-216">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="31a62-216">Az.Automation</span></span>
* <span data-ttu-id="31a62-217">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="31a62-217">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="31a62-218">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="31a62-218">Added Update Management cmdlets</span></span>
* <span data-ttu-id="31a62-219">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="31a62-219">Added Source Control cmdlets</span></span>
* <span data-ttu-id="31a62-220">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="31a62-220">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="31a62-221">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="31a62-221">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="31a62-222">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31a62-222">Az.Compute</span></span>
* <span data-ttu-id="31a62-223">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="31a62-223">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="31a62-224">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="31a62-224">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="31a62-225">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="31a62-225">Az.ContainerInstance</span></span>
* <span data-ttu-id="31a62-226">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="31a62-226">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="31a62-227">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="31a62-227">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="31a62-228">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="31a62-228">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="31a62-229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31a62-229">Az.Network</span></span>
* <span data-ttu-id="31a62-230">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="31a62-230">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="31a62-231">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="31a62-231">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="31a62-232">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="31a62-232">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="31a62-233">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="31a62-233">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="31a62-234">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="31a62-234">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="31a62-235">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="31a62-235">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="31a62-236">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="31a62-236">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="31a62-237">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="31a62-237">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="31a62-238">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="31a62-238">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="31a62-239">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="31a62-239">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="31a62-240">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="31a62-240">Az.Relay</span></span>
* <span data-ttu-id="31a62-241">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="31a62-241">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="31a62-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31a62-242">Az.Resources</span></span>
* <span data-ttu-id="31a62-243">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="31a62-243">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="31a62-244">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="31a62-244">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="31a62-245">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="31a62-245">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="31a62-246">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31a62-246">Az.ServiceFabric</span></span>
* <span data-ttu-id="31a62-247">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="31a62-247">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="31a62-248">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31a62-248">Az.Sql</span></span>
* <span data-ttu-id="31a62-249">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="31a62-249">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="31a62-250">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="31a62-250">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="31a62-251">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="31a62-251">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="31a62-252">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="31a62-252">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="31a62-253">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="31a62-253">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="31a62-254">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="31a62-254">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="31a62-255">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="31a62-255">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="31a62-256">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="31a62-256">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="31a62-257">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="31a62-257">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="31a62-258">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="31a62-258">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="31a62-259">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="31a62-259">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="31a62-260">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="31a62-260">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="31a62-261">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="31a62-261">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="31a62-262">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="31a62-262">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="31a62-263">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="31a62-263">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="31a62-264">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="31a62-264">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="31a62-265">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="31a62-265">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="31a62-266">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="31a62-266">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="31a62-267">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="31a62-267">General</span></span>
* <span data-ttu-id="31a62-268">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="31a62-268">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="31a62-269">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="31a62-269">Az.Profile</span></span>
* <span data-ttu-id="31a62-270">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="31a62-270">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="31a62-271">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="31a62-271">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="31a62-272">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="31a62-272">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="31a62-273">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="31a62-273">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="31a62-274">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="31a62-274">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="31a62-275">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="31a62-275">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="31a62-276">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="31a62-276">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="31a62-277">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31a62-277">Az.CognitiveServices</span></span>
* <span data-ttu-id="31a62-278">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="31a62-278">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31a62-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31a62-279">Az.Compute</span></span>
* <span data-ttu-id="31a62-280">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="31a62-280">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="31a62-281">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="31a62-281">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="31a62-282">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="31a62-282">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31a62-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31a62-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="31a62-284">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="31a62-284">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="31a62-285">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="31a62-285">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="31a62-286">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="31a62-286">Az.Insights</span></span>
* <span data-ttu-id="31a62-287">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="31a62-287">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="31a62-288">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="31a62-288">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="31a62-289">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="31a62-289">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="31a62-290">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="31a62-290">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31a62-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31a62-291">Az.Network</span></span>
* <span data-ttu-id="31a62-292">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="31a62-292">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="31a62-293">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="31a62-293">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="31a62-294">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="31a62-294">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="31a62-295">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="31a62-295">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="31a62-296">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="31a62-296">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="31a62-297">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="31a62-297">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="31a62-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="31a62-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="31a62-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="31a62-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="31a62-300">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="31a62-300">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="31a62-301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31a62-301">Az.Resources</span></span>
* <span data-ttu-id="31a62-302"> https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="31a62-302">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="31a62-303">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="31a62-303">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="31a62-304">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31a62-304">Az.ServiceBus</span></span>
* <span data-ttu-id="31a62-305">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="31a62-305">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="31a62-306">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31a62-306">Az.ServiceFabric</span></span>
* <span data-ttu-id="31a62-307">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="31a62-307">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="31a62-308">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="31a62-308">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="31a62-309">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="31a62-309">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="31a62-310">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="31a62-310">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="31a62-311">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="31a62-311">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="31a62-312">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="31a62-312">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="31a62-313">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="31a62-313">Az.Profile</span></span>
* <span data-ttu-id="31a62-314">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="31a62-314">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="31a62-315">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="31a62-315">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31a62-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31a62-316">Az.Compute</span></span>
* <span data-ttu-id="31a62-317">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="31a62-317">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="31a62-318">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="31a62-318">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="31a62-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31a62-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="31a62-320">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="31a62-320">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="31a62-321">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="31a62-321">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="31a62-322">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="31a62-322">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="31a62-323">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="31a62-323">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="31a62-324">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="31a62-324">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31a62-325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31a62-325">Az.Network</span></span>
* <span data-ttu-id="31a62-326">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="31a62-326">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="31a62-327">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="31a62-327">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="31a62-328">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31a62-328">Az.Resources</span></span>
* <span data-ttu-id="31a62-329">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="31a62-329">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="31a62-330">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="31a62-330">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="31a62-331">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="31a62-331">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="31a62-332">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="31a62-332">Azure.Storage</span></span>
* <span data-ttu-id="31a62-333">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="31a62-333">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="31a62-334">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="31a62-334">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="31a62-335">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="31a62-335">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="31a62-336">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="31a62-336">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="31a62-337">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="31a62-337">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="31a62-338">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31a62-338">Az.CognitiveServices</span></span>
* <span data-ttu-id="31a62-339">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="31a62-339">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="31a62-340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31a62-340">Az.Compute</span></span>
* <span data-ttu-id="31a62-341">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="31a62-341">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="31a62-342">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="31a62-342">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="31a62-343">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="31a62-343">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="31a62-344">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="31a62-344">Az.DataFactoryV2</span></span>
* <span data-ttu-id="31a62-345">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="31a62-345">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="31a62-346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="31a62-346">Az.Network</span></span>
* <span data-ttu-id="31a62-347">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="31a62-347">Added NetworkProfile functionality.</span></span> <span data-ttu-id="31a62-348">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="31a62-348">new cmdlets added</span></span>
    - <span data-ttu-id="31a62-349">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31a62-349">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="31a62-350">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31a62-350">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="31a62-351">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31a62-351">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="31a62-352">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31a62-352">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="31a62-353">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="31a62-353">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="31a62-354">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="31a62-354">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="31a62-355">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="31a62-355">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="31a62-356">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="31a62-356">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="31a62-357">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="31a62-357">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="31a62-358">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="31a62-358">Az.RedisCache</span></span>
* <span data-ttu-id="31a62-359">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="31a62-359">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="31a62-360">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="31a62-360">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="31a62-361">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="31a62-361">Az.Resources</span></span>
* <span data-ttu-id="31a62-362">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="31a62-362">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="31a62-363">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="31a62-363">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="31a62-364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="31a62-364">Az.Sql</span></span>
* <span data-ttu-id="31a62-365">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="31a62-365">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="31a62-366">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="31a62-366">Az.Websites</span></span>
* <span data-ttu-id="31a62-367">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="31a62-367">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="31a62-368">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="31a62-368">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="31a62-369">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="31a62-369">0.2.0 - September 2018</span></span>
 <span data-ttu-id="31a62-370">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="31a62-370">Initial Release</span></span>