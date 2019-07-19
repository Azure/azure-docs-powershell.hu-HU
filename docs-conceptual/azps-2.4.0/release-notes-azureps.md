---
ms.openlocfilehash: f357a17f698d68c1a29dcb78f83671973fd6ecad
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863742"
---
## <a name="240---july-2019"></a><span data-ttu-id="90c89-101">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="90c89-101">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="90c89-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="90c89-102">Az.Accounts</span></span>
* <span data-ttu-id="90c89-103">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="90c89-103">Add support for profile cmdlets</span></span>
* <span data-ttu-id="90c89-104">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="90c89-104">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="90c89-105">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="90c89-105">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="90c89-106">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="90c89-106">Az.Advisor</span></span>
* <span data-ttu-id="90c89-107">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="90c89-107">GA release of Az.Advisor</span></span>
* <span data-ttu-id="90c89-108">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="90c89-108">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="90c89-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="90c89-109">Az.ApiManagement</span></span>
* <span data-ttu-id="90c89-110">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="90c89-110">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="90c89-111">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="90c89-111">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="90c89-112">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="90c89-112">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="90c89-113">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="90c89-113">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="90c89-114">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="90c89-114">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="90c89-115">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="90c89-115">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="90c89-116">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="90c89-116">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="90c89-117">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="90c89-117">Az.Automation</span></span>
* <span data-ttu-id="90c89-118">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="90c89-118">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-119">Az.Compute</span></span>
* <span data-ttu-id="90c89-120">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="90c89-120">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="90c89-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="90c89-121">Az.DataFactory</span></span>
* <span data-ttu-id="90c89-122">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="90c89-122">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="90c89-123">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="90c89-123">Az.EventGrid</span></span>
* <span data-ttu-id="90c89-124">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="90c89-124">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="90c89-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="90c89-125">Az.IotHub</span></span>
* <span data-ttu-id="90c89-126">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="90c89-126">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="90c89-127">Az.Network</span><span class="sxs-lookup"><span data-stu-id="90c89-127">Az.Network</span></span>
* <span data-ttu-id="90c89-128">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="90c89-128">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="90c89-129">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="90c89-129">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="90c89-130">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="90c89-130">Az.PolicyInsights</span></span>
* <span data-ttu-id="90c89-131">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="90c89-131">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="90c89-132">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="90c89-132">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="90c89-133">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="90c89-133">Az.OperationalInsights</span></span>
* <span data-ttu-id="90c89-134">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="90c89-134">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="90c89-135">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90c89-135">Az.RecoveryServices</span></span>
* <span data-ttu-id="90c89-136">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="90c89-136">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="90c89-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-137">Az.Resources</span></span>
    - <span data-ttu-id="90c89-138">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="90c89-138">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="90c89-139">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="90c89-139">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="90c89-140">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="90c89-140">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="90c89-141">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-141">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="90c89-142">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="90c89-142">Az.ServiceBus</span></span>
* <span data-ttu-id="90c89-143">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="90c89-143">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="90c89-144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-144">Az.Sql</span></span>
* <span data-ttu-id="90c89-145">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="90c89-145">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="90c89-146">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="90c89-146">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="90c89-147">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="90c89-147">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="90c89-148">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="90c89-148">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="90c89-149">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="90c89-149">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="90c89-150">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="90c89-150">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="90c89-151">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="90c89-151">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="90c89-152">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="90c89-152">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="90c89-153">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="90c89-153">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="90c89-154">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="90c89-154">Az.Storage</span></span>
* <span data-ttu-id="90c89-155">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="90c89-155">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="90c89-156">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="90c89-156">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="90c89-157">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="90c89-157">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="90c89-158">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="90c89-158">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="90c89-159">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="90c89-159">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="90c89-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="90c89-160">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="90c89-161">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="90c89-161">Set-AzStorageAccount</span></span>
* <span data-ttu-id="90c89-162">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="90c89-162">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="90c89-163">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="90c89-163">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="90c89-164">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="90c89-164">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="90c89-165">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="90c89-165">Az.StorageSync</span></span>
* <span data-ttu-id="90c89-166">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="90c89-166">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="90c89-167">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="90c89-167">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="90c89-168">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="90c89-168">Az.Accounts</span></span>
* <span data-ttu-id="90c89-169">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-169">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="90c89-170">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="90c89-170">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="90c89-171">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-171">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="90c89-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="90c89-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="90c89-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="90c89-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-174">Az.Compute</span></span>
* <span data-ttu-id="90c89-175">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="90c89-175">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="90c89-176">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="90c89-176">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="90c89-177">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="90c89-177">Az.Dns</span></span>
* <span data-ttu-id="90c89-178">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="90c89-178">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="90c89-179">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="90c89-179">Az.EventGrid</span></span>
* <span data-ttu-id="90c89-180">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="90c89-180">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="90c89-181">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="90c89-181">New cmdlets:</span></span>
    - <span data-ttu-id="90c89-182">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="90c89-182">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="90c89-183">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="90c89-183">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="90c89-184">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="90c89-184">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="90c89-185">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="90c89-185">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="90c89-186">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="90c89-186">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="90c89-187">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="90c89-187">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="90c89-188">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="90c89-188">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="90c89-189">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="90c89-189">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="90c89-190">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="90c89-190">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="90c89-191">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="90c89-191">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="90c89-192">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="90c89-192">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="90c89-193">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="90c89-193">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="90c89-194">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="90c89-194">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="90c89-195">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="90c89-195">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="90c89-196">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="90c89-196">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="90c89-197">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="90c89-197">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="90c89-198">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="90c89-198">Updated cmdlets:</span></span>
    - <span data-ttu-id="90c89-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="90c89-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="90c89-200">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="90c89-200">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="90c89-201">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="90c89-201">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="90c89-202">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="90c89-202">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="90c89-203">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="90c89-203">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="90c89-204">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="90c89-204">Event subscription expiration date,</span></span>
            - <span data-ttu-id="90c89-205">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="90c89-205">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="90c89-206">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="90c89-206">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="90c89-207">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="90c89-207">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="90c89-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="90c89-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="90c89-209">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="90c89-209">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="90c89-210">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="90c89-210">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="90c89-211">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="90c89-211">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="90c89-212">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="90c89-212">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="90c89-213">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="90c89-213">Az.FrontDoor</span></span>
* <span data-ttu-id="90c89-214">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="90c89-214">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="90c89-215">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="90c89-215">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="90c89-216">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="90c89-216">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="90c89-217">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="90c89-217">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="90c89-218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="90c89-218">Az.Network</span></span>
* <span data-ttu-id="90c89-219">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="90c89-219">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="90c89-220">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="90c89-220">New cmdlets</span></span>
        - <span data-ttu-id="90c89-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="90c89-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="90c89-222">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="90c89-222">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="90c89-223">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="90c89-223">New cmdlets</span></span> 
        - <span data-ttu-id="90c89-224">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="90c89-224">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="90c89-225">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="90c89-225">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="90c89-226">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="90c89-226">New cmdlets</span></span> 
        - <span data-ttu-id="90c89-227">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="90c89-227">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="90c89-228">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="90c89-228">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="90c89-229">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="90c89-229">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="90c89-230">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="90c89-230">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="90c89-231">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="90c89-231">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="90c89-232">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="90c89-232">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="90c89-233">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="90c89-233">New cmdlets</span></span>
        - <span data-ttu-id="90c89-234">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="90c89-234">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="90c89-235">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="90c89-235">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="90c89-236">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="90c89-236">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="90c89-237">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="90c89-237">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="90c89-238">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="90c89-238">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="90c89-239">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="90c89-239">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="90c89-240">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="90c89-240">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="90c89-241">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="90c89-241">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="90c89-242">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="90c89-242">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="90c89-243">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="90c89-243">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="90c89-244">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="90c89-244">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="90c89-245">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="90c89-245">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="90c89-246">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-246">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="90c89-247">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="90c89-247">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="90c89-248">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-248">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="90c89-249">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-249">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="90c89-250">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="90c89-250">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="90c89-251">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-251">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="90c89-252">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="90c89-252">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="90c89-253">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="90c89-253">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="90c89-254">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="90c89-254">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="90c89-255">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="90c89-255">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="90c89-256">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="90c89-256">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="90c89-257">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="90c89-257">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="90c89-258">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="90c89-258">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="90c89-259">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="90c89-259">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="90c89-260">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="90c89-260">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="90c89-261">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="90c89-261">Az.OperationalInsights</span></span>
* <span data-ttu-id="90c89-262">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-262">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="90c89-263">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-263">Az.Resources</span></span>
* <span data-ttu-id="90c89-264">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="90c89-264">Support for additional Template Export options</span></span>
    - <span data-ttu-id="90c89-265">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-265">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="90c89-266">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-266">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="90c89-267">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="90c89-267">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="90c89-268">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="90c89-268">Az.ServiceFabric</span></span>
* <span data-ttu-id="90c89-269">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="90c89-269">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="90c89-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-270">Az.Sql</span></span>
* <span data-ttu-id="90c89-271">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="90c89-271">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="90c89-272">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="90c89-272">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="90c89-273">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-273">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="90c89-274">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="90c89-274">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="90c89-275">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="90c89-275">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="90c89-276">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="90c89-276">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="90c89-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="90c89-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="90c89-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="90c89-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="90c89-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="90c89-279">Az.Storage</span></span>
* <span data-ttu-id="90c89-280">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="90c89-280">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="90c89-281">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="90c89-281">New-AzStorageAccount</span></span>
* <span data-ttu-id="90c89-282">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="90c89-282">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="90c89-283">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="90c89-283">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="90c89-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="90c89-284">Az.Websites</span></span>
* <span data-ttu-id="90c89-285">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="90c89-285">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="90c89-286">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="90c89-286">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="90c89-287">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="90c89-287">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="90c89-288">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="90c89-288">Az.Cdn</span></span>
* <span data-ttu-id="90c89-289">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="90c89-289">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-290">Az.Compute</span></span>
* <span data-ttu-id="90c89-291">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="90c89-291">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="90c89-292">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="90c89-292">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="90c89-293">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="90c89-293">Az.EventHub</span></span>
* <span data-ttu-id="90c89-294">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="90c89-294">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="90c89-295">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="90c89-295">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="90c89-296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="90c89-296">Az.Network</span></span>
* <span data-ttu-id="90c89-297">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="90c89-297">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="90c89-298">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="90c89-298">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="90c89-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="90c89-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="90c89-300">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="90c89-300">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="90c89-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90c89-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="90c89-302">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="90c89-302">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="90c89-303">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="90c89-303">Az.ServiceBus</span></span>
* <span data-ttu-id="90c89-304">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="90c89-304">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="90c89-305">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="90c89-305">Az.ServiceFabric</span></span>
* <span data-ttu-id="90c89-306">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="90c89-306">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="90c89-307">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="90c89-307">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="90c89-308">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-308">Az.Sql</span></span>
* <span data-ttu-id="90c89-309">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="90c89-309">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="90c89-310">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="90c89-310">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="90c89-311">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="90c89-311">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="90c89-312">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="90c89-312">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="90c89-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="90c89-313">Az.Websites</span></span>
* <span data-ttu-id="90c89-314">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="90c89-314">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="90c89-315">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="90c89-315">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="90c89-316">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="90c89-316">Az.ApiManagement</span></span>
* <span data-ttu-id="90c89-317">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="90c89-317">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="90c89-318">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="90c89-318">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="90c89-319">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="90c89-319">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="90c89-320">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="90c89-320">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="90c89-321">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="90c89-321">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="90c89-322">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-322">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="90c89-323">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="90c89-323">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="90c89-324">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="90c89-324">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="90c89-325">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="90c89-325">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="90c89-326">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="90c89-326">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="90c89-327">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="90c89-327">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="90c89-328">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="90c89-328">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="90c89-329">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-329">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="90c89-330">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="90c89-330">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="90c89-331">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="90c89-331">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="90c89-332">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="90c89-332">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="90c89-333">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="90c89-333">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="90c89-334">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-334">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="90c89-335">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="90c89-335">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="90c89-336">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="90c89-336">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="90c89-337">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="90c89-337">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="90c89-338">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="90c89-338">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="90c89-339">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="90c89-339">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="90c89-340">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="90c89-340">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="90c89-341">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="90c89-341">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="90c89-342">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="90c89-342">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="90c89-343">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="90c89-343">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="90c89-344">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="90c89-344">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="90c89-345">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="90c89-345">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="90c89-346">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="90c89-346">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="90c89-347">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="90c89-347">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="90c89-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="90c89-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="90c89-349">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="90c89-349">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="90c89-350">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-350">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="90c89-351">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="90c89-351">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="90c89-352">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="90c89-352">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="90c89-353">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="90c89-353">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="90c89-354">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="90c89-354">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="90c89-355">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="90c89-355">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="90c89-356">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-356">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="90c89-357">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="90c89-357">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="90c89-358">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="90c89-358">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="90c89-359">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="90c89-359">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="90c89-360">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="90c89-360">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="90c89-361">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-361">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="90c89-362">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="90c89-362">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="90c89-363">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="90c89-363">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="90c89-364">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="90c89-364">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="90c89-365">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-365">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="90c89-366">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="90c89-366">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="90c89-367">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="90c89-367">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="90c89-368">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="90c89-368">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="90c89-369">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="90c89-369">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="90c89-370">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-370">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="90c89-371">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="90c89-371">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="90c89-372">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="90c89-372">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="90c89-373">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-373">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="90c89-374">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="90c89-374">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="90c89-375">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="90c89-375">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="90c89-376">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="90c89-376">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="90c89-377">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-377">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="90c89-378">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="90c89-378">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="90c89-379">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="90c89-379">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="90c89-380">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="90c89-380">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="90c89-381">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="90c89-381">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="90c89-382">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="90c89-382">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="90c89-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="90c89-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="90c89-384">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="90c89-384">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="90c89-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="90c89-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="90c89-386">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="90c89-386">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="90c89-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="90c89-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="90c89-388">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="90c89-388">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="90c89-389">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="90c89-389">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="90c89-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="90c89-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="90c89-391">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="90c89-391">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="90c89-392">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="90c89-392">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="90c89-393">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="90c89-393">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="90c89-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="90c89-394">Az.Automation</span></span>
* <span data-ttu-id="90c89-395">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="90c89-395">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="90c89-396">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="90c89-396">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="90c89-397">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="90c89-397">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="90c89-398">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="90c89-398">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="90c89-399">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="90c89-399">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="90c89-400">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="90c89-400">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="90c89-401">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="90c89-401">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-402">Az.Compute</span></span>
* <span data-ttu-id="90c89-403">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="90c89-403">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="90c89-404">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="90c89-404">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="90c89-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="90c89-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="90c89-406">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="90c89-406">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="90c89-407">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="90c89-407">Az.Monitor</span></span>
* <span data-ttu-id="90c89-408">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="90c89-408">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="90c89-409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="90c89-409">Az.Network</span></span>
* <span data-ttu-id="90c89-410">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="90c89-410">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="90c89-411">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="90c89-411">Updated cmdlet:</span></span>
        - <span data-ttu-id="90c89-412">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="90c89-412">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="90c89-413">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="90c89-413">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="90c89-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-414">Az.Resources</span></span>
* <span data-ttu-id="90c89-415">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="90c89-415">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="90c89-416">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-416">Az.Sql</span></span>
* <span data-ttu-id="90c89-417">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="90c89-417">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="90c89-418">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="90c89-418">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="90c89-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="90c89-419">Az.Accounts</span></span>
* <span data-ttu-id="90c89-420">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="90c89-420">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="90c89-421">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="90c89-421">Az.CognitiveServices</span></span>
* <span data-ttu-id="90c89-422">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="90c89-422">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="90c89-423">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="90c89-423">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-424">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-424">Az.Compute</span></span>
* <span data-ttu-id="90c89-425">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="90c89-425">Proximity placement group feature.</span></span>
    - <span data-ttu-id="90c89-426">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="90c89-426">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="90c89-427">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="90c89-427">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="90c89-428">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="90c89-428">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="90c89-429">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="90c89-429">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="90c89-430">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-430">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="90c89-431">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="90c89-431">Breaking changes</span></span>
    - <span data-ttu-id="90c89-432">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="90c89-432">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="90c89-433">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="90c89-433">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="90c89-434">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="90c89-434">Az.DeploymentManager</span></span>
* <span data-ttu-id="90c89-435">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="90c89-435">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="90c89-436">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="90c89-436">Az.Dns</span></span>
* <span data-ttu-id="90c89-437">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="90c89-437">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="90c89-438">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-438">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="90c89-439">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="90c89-439">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="90c89-440">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="90c89-440">Az.FrontDoor</span></span>
* <span data-ttu-id="90c89-441">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="90c89-441">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="90c89-442">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="90c89-442">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="90c89-443">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="90c89-443">Az.HDInsight</span></span>
* <span data-ttu-id="90c89-444">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="90c89-444">Removed two cmdlets:</span></span>
    - <span data-ttu-id="90c89-445">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="90c89-445">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="90c89-446">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="90c89-446">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="90c89-447">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="90c89-447">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="90c89-448">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="90c89-448">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="90c89-449">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="90c89-449">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="90c89-450">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="90c89-450">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="90c89-451">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="90c89-451">Az.Monitor</span></span>
* <span data-ttu-id="90c89-452">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="90c89-452">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="90c89-453">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="90c89-453">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="90c89-454">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="90c89-454">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="90c89-455">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="90c89-455">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="90c89-456">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="90c89-456">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="90c89-457">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="90c89-457">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="90c89-458">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="90c89-458">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="90c89-459">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="90c89-459">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="90c89-460">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="90c89-460">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="90c89-461">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="90c89-461">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="90c89-462">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="90c89-462">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="90c89-463">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="90c89-463">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="90c89-464">[További](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="90c89-464">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="90c89-465">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="90c89-465">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="90c89-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="90c89-466">Az.Network</span></span>
* <span data-ttu-id="90c89-467">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="90c89-467">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="90c89-468">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="90c89-468">New cmdlets</span></span>
        - <span data-ttu-id="90c89-469">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="90c89-469">New-AzNatGateway</span></span>
        - <span data-ttu-id="90c89-470">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="90c89-470">Get-AzNatGateway</span></span>
        - <span data-ttu-id="90c89-471">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="90c89-471">Set-AzNatGateway</span></span>
        - <span data-ttu-id="90c89-472">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="90c89-472">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="90c89-473">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="90c89-473">Updated cmdlets</span></span>
        - <span data-ttu-id="90c89-474">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="90c89-474">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="90c89-475">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="90c89-475">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="90c89-476">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="90c89-476">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="90c89-477">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="90c89-477">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="90c89-478">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="90c89-478">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="90c89-479">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="90c89-479">Az.PolicyInsights</span></span>
* <span data-ttu-id="90c89-480">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="90c89-480">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="90c89-481">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="90c89-481">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="90c89-482">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="90c89-482">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="90c89-483">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90c89-483">Az.RecoveryServices</span></span>
* <span data-ttu-id="90c89-484">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="90c89-484">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="90c89-485">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="90c89-485">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="90c89-486">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="90c89-486">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="90c89-487">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="90c89-487">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="90c89-488">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="90c89-488">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="90c89-489">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="90c89-489">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="90c89-490">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="90c89-490">Az.Relay</span></span>
* <span data-ttu-id="90c89-491">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="90c89-491">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="90c89-492">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="90c89-492">Az.ServiceBus</span></span>
* <span data-ttu-id="90c89-493">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="90c89-493">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="90c89-494">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="90c89-494">Az.Storage</span></span>
* <span data-ttu-id="90c89-495">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="90c89-495">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="90c89-496">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="90c89-496">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="90c89-497">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="90c89-497">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="90c89-498">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="90c89-498">New-AzStorageAccount</span></span>
* <span data-ttu-id="90c89-499">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="90c89-499">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="90c89-500">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="90c89-500">New-AzStorageAccount</span></span>
    - <span data-ttu-id="90c89-501">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="90c89-501">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="90c89-502">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="90c89-502">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="90c89-503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="90c89-503">Az.Websites</span></span>
* <span data-ttu-id="90c89-504">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-504">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="90c89-505">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="90c89-505">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="90c89-506">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="90c89-506">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="90c89-507">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="90c89-507">Highlights since the last major release</span></span>
* <span data-ttu-id="90c89-508">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="90c89-508">General availability of `Az` module</span></span>
* <span data-ttu-id="90c89-509">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="90c89-509">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="90c89-510">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="90c89-510">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="90c89-511">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-511">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="90c89-512">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-512">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="90c89-513">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-513">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="90c89-514">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-514">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="90c89-515">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="90c89-515">Az.Accounts</span></span>
* <span data-ttu-id="90c89-516">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-516">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="90c89-517">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="90c89-517">Az.Batch</span></span>
* <span data-ttu-id="90c89-518">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-518">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="90c89-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="90c89-519">Az.Cdn</span></span>
* <span data-ttu-id="90c89-520">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="90c89-521">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="90c89-521">Az.CognitiveServices</span></span>
* <span data-ttu-id="90c89-522">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-522">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-523">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-523">Az.Compute</span></span>
* <span data-ttu-id="90c89-524">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="90c89-524">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="90c89-525">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-525">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="90c89-526">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="90c89-526">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="90c89-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="90c89-527">Az.DataFactory</span></span>
* <span data-ttu-id="90c89-528">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="90c89-528">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="90c89-529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="90c89-529">Az.DataLakeStore</span></span>
* <span data-ttu-id="90c89-530">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-530">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="90c89-531">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="90c89-531">Az.EventGrid</span></span>
* <span data-ttu-id="90c89-532">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="90c89-532">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="90c89-533">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="90c89-533">Az.EventHub</span></span>
* <span data-ttu-id="90c89-534">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="90c89-534">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="90c89-535">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="90c89-535">Az.HDInsight</span></span>
* <span data-ttu-id="90c89-536">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-536">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="90c89-537">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="90c89-537">Az.IotHub</span></span>
* <span data-ttu-id="90c89-538">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-538">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="90c89-539">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="90c89-539">Az.KeyVault</span></span>
* <span data-ttu-id="90c89-540">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-540">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="90c89-541">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="90c89-541">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="90c89-542">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="90c89-542">Az.MachineLearning</span></span>
* <span data-ttu-id="90c89-543">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-543">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="90c89-544">Az.Media</span><span class="sxs-lookup"><span data-stu-id="90c89-544">Az.Media</span></span>
* <span data-ttu-id="90c89-545">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-545">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="90c89-546">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="90c89-546">Az.Monitor</span></span>
  * <span data-ttu-id="90c89-547">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="90c89-547">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="90c89-548">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="90c89-548">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="90c89-549">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="90c89-549">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="90c89-550">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="90c89-550">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="90c89-551">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="90c89-551">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="90c89-552">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="90c89-552">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="90c89-553">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="90c89-553">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="90c89-554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="90c89-554">Az.Network</span></span>
* <span data-ttu-id="90c89-555">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-555">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="90c89-556">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="90c89-556">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="90c89-557">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="90c89-557">Az.NotificationHubs</span></span>
* <span data-ttu-id="90c89-558">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-558">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="90c89-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="90c89-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="90c89-560">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-560">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="90c89-561">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="90c89-561">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="90c89-562">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-562">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="90c89-563">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90c89-563">Az.RecoveryServices</span></span>
* <span data-ttu-id="90c89-564">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-564">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="90c89-565">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="90c89-565">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="90c89-566">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="90c89-566">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="90c89-567">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="90c89-567">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="90c89-568">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="90c89-568">Az.RedisCache</span></span>
* <span data-ttu-id="90c89-569">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="90c89-570">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-570">Az.Resources</span></span>
* <span data-ttu-id="90c89-571">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="90c89-571">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="90c89-572">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-572">Az.Sql</span></span>
* <span data-ttu-id="90c89-573">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="90c89-573">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="90c89-574">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="90c89-575">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="90c89-575">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="90c89-576">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="90c89-576">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="90c89-577">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="90c89-577">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="90c89-578">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="90c89-578">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="90c89-579">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="90c89-579">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="90c89-580">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="90c89-580">Az.Websites</span></span>
* <span data-ttu-id="90c89-581">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="90c89-581">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="90c89-582">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="90c89-582">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="90c89-583">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="90c89-583">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="90c89-584">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="90c89-584">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="90c89-585">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="90c89-585">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="90c89-586">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="90c89-586">Highlights since the last major release</span></span>
* <span data-ttu-id="90c89-587">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="90c89-587">General availability of `Az` module</span></span>
* <span data-ttu-id="90c89-588">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="90c89-588">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="90c89-589">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="90c89-589">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="90c89-590">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-590">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="90c89-591">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-591">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="90c89-592">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-592">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="90c89-593">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-593">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="90c89-594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="90c89-594">Az.Accounts</span></span>
* <span data-ttu-id="90c89-595">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="90c89-595">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="90c89-596">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="90c89-596">Az.AnalysisServices</span></span>
* <span data-ttu-id="90c89-597">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="90c89-597">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="90c89-598">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="90c89-598">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="90c89-599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="90c89-599">Az.Automation</span></span>
* <span data-ttu-id="90c89-600">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="90c89-600">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="90c89-601">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="90c89-601">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="90c89-602">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-602">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-603">Az.Compute</span></span>
* <span data-ttu-id="90c89-604">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-604">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="90c89-605">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="90c89-605">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="90c89-606">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="90c89-606">Az.ContainerInstance</span></span>
* <span data-ttu-id="90c89-607">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="90c89-607">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="90c89-608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="90c89-608">Az.DataFactory</span></span>
* <span data-ttu-id="90c89-609">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="90c89-609">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="90c89-610">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="90c89-610">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="90c89-611">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-611">Az.Resources</span></span>
* <span data-ttu-id="90c89-612">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="90c89-612">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="90c89-613">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-613">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="90c89-614">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="90c89-614">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="90c89-615">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="90c89-615">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="90c89-616">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="90c89-616">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="90c89-617">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="90c89-617">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="90c89-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-618">Az.Sql</span></span>
* <span data-ttu-id="90c89-619">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="90c89-619">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="90c89-620">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="90c89-620">Az.Storage</span></span>
* <span data-ttu-id="90c89-621">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="90c89-621">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="90c89-622">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="90c89-622">New-AzStorageContext</span></span>
* <span data-ttu-id="90c89-623">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="90c89-623">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="90c89-624">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="90c89-624">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="90c89-625">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="90c89-625">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="90c89-626">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="90c89-626">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="90c89-627">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="90c89-627">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="90c89-628">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="90c89-628">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="90c89-629">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="90c89-629">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="90c89-630">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="90c89-630">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="90c89-631">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="90c89-631">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="90c89-632">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="90c89-632">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="90c89-633">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="90c89-633">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="90c89-634">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="90c89-634">Highlights since the last major release</span></span>
* <span data-ttu-id="90c89-635">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="90c89-635">General availability of `Az` module</span></span>
* <span data-ttu-id="90c89-636">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="90c89-636">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="90c89-637">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="90c89-637">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="90c89-638">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-638">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="90c89-639">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-639">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="90c89-640">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-640">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="90c89-641">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-641">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="90c89-642">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="90c89-642">Az.Automation</span></span>
* <span data-ttu-id="90c89-643">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="90c89-643">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="90c89-644">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="90c89-644">Dynamic grouping</span></span>
    * <span data-ttu-id="90c89-645">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="90c89-645">Pre-Post script</span></span>
    * <span data-ttu-id="90c89-646">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="90c89-646">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-647">Az.Compute</span></span>
* <span data-ttu-id="90c89-648">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-648">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="90c89-649">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="90c89-649">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="90c89-650">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="90c89-650">Az.KeyVault</span></span>
* <span data-ttu-id="90c89-651">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-651">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="90c89-652">Az.Network</span><span class="sxs-lookup"><span data-stu-id="90c89-652">Az.Network</span></span>
* <span data-ttu-id="90c89-653">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-653">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="90c89-654">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="90c89-654">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="90c89-655">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90c89-655">Az.RecoveryServices</span></span>
* <span data-ttu-id="90c89-656">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="90c89-656">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="90c89-657">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-657">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="90c89-658">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-658">Az.Resources</span></span>
* <span data-ttu-id="90c89-659">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-659">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="90c89-660">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-660">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="90c89-661">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-661">Az.Sql</span></span>
* <span data-ttu-id="90c89-662">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="90c89-662">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="90c89-663">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="90c89-663">Az.Storage</span></span>
* <span data-ttu-id="90c89-664">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="90c89-664">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="90c89-665">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="90c89-665">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="90c89-666">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="90c89-666">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="90c89-667">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="90c89-667">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="90c89-668">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="90c89-668">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="90c89-669">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="90c89-669">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="90c89-670">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="90c89-670">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="90c89-671">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="90c89-671">Az.Websites</span></span>
* <span data-ttu-id="90c89-672">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="90c89-672">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="90c89-673">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="90c89-673">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="90c89-674">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="90c89-674">Az.Accounts</span></span>
* <span data-ttu-id="90c89-675">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="90c89-675">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="90c89-676">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-676">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="90c89-677">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="90c89-677">Az.Automation</span></span>
* <span data-ttu-id="90c89-678">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-678">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="90c89-679">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="90c89-679">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="90c89-680">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="90c89-680">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="90c89-681">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="90c89-681">Az.Cdn</span></span>
* <span data-ttu-id="90c89-682">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="90c89-682">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-683">Az.Compute</span></span>
* <span data-ttu-id="90c89-684">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-684">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="90c89-685">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="90c89-685">Az.DataFactory</span></span>
* <span data-ttu-id="90c89-686">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="90c89-686">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="90c89-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="90c89-687">Az.LogicApp</span></span>
* <span data-ttu-id="90c89-688">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="90c89-688">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="90c89-689">Az.Network</span><span class="sxs-lookup"><span data-stu-id="90c89-689">Az.Network</span></span>
* <span data-ttu-id="90c89-690">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-690">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="90c89-691">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90c89-691">Az.RecoveryServices</span></span>
* <span data-ttu-id="90c89-692">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="90c89-692">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="90c89-693">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="90c89-693">SDK Update</span></span>
* <span data-ttu-id="90c89-694">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="90c89-694">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="90c89-695">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="90c89-695">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="90c89-696">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-696">Az.Resources</span></span>
* <span data-ttu-id="90c89-697">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-697">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="90c89-698">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="90c89-698">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="90c89-699">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="90c89-699">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="90c89-700">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="90c89-700">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="90c89-701">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="90c89-701">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="90c89-702">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="90c89-702">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="90c89-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-703">Az.Sql</span></span>
* <span data-ttu-id="90c89-704">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="90c89-704">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="90c89-705">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="90c89-705">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="90c89-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="90c89-706">Az.Storage</span></span>
* <span data-ttu-id="90c89-707">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="90c89-707">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="90c89-708">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="90c89-708">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="90c89-709">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="90c89-709">Az.AnalysisServices</span></span>
* <span data-ttu-id="90c89-710">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="90c89-710">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="90c89-711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="90c89-711">Az.Automation</span></span>
* <span data-ttu-id="90c89-712">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-712">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="90c89-713">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="90c89-713">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="90c89-714">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-714">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="90c89-715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="90c89-715">Az.CognitiveServices</span></span>
* <span data-ttu-id="90c89-716">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="90c89-716">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-717">Az.Compute</span></span>
* <span data-ttu-id="90c89-718">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="90c89-718">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="90c89-719">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="90c89-719">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="90c89-720">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="90c89-720">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="90c89-721">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="90c89-721">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="90c89-722">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="90c89-722">Az.DataLakeStore</span></span>
* <span data-ttu-id="90c89-723">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="90c89-723">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="90c89-724">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="90c89-724">Az.EventHub</span></span>
* <span data-ttu-id="90c89-725">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="90c89-725">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="90c89-726">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="90c89-726">Az.KeyVault</span></span>
* <span data-ttu-id="90c89-727">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="90c89-727">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="90c89-728">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="90c89-728">Az.LogicApp</span></span>
* <span data-ttu-id="90c89-729">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="90c89-729">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="90c89-730">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="90c89-730">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="90c89-731">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="90c89-731">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="90c89-732">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="90c89-732">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="90c89-733">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="90c89-733">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="90c89-734">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="90c89-734">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="90c89-735">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="90c89-735">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="90c89-736">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="90c89-736">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="90c89-737">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="90c89-737">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="90c89-738">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="90c89-738">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="90c89-739">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="90c89-739">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="90c89-740">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="90c89-740">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="90c89-741">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="90c89-741">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="90c89-742">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="90c89-742">Az.Monitor</span></span>
* <span data-ttu-id="90c89-743">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-743">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="90c89-744">Az.Network</span><span class="sxs-lookup"><span data-stu-id="90c89-744">Az.Network</span></span>
* <span data-ttu-id="90c89-745">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="90c89-745">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="90c89-746">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="90c89-746">Az.OperationalInsights</span></span>
* <span data-ttu-id="90c89-747">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="90c89-747">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="90c89-748">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="90c89-748">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="90c89-749">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="90c89-749">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="90c89-750">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-750">Az.Resources</span></span>
* <span data-ttu-id="90c89-751">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="90c89-751">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="90c89-752">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="90c89-752">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="90c89-753">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="90c89-753">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="90c89-754">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="90c89-754">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="90c89-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-755">Az.Sql</span></span>
* <span data-ttu-id="90c89-756">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="90c89-756">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="90c89-757">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="90c89-757">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="90c89-758">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="90c89-758">Az.Websites</span></span>
* <span data-ttu-id="90c89-759">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="90c89-759">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="90c89-760">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="90c89-760">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="90c89-761">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="90c89-761">Az.Accounts</span></span>
* <span data-ttu-id="90c89-762">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="90c89-762">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="90c89-763">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="90c89-763">Az.AnalysisServices</span></span>
<span data-ttu-id="90c89-764">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="90c89-764">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-765">Az.Compute</span></span>
* <span data-ttu-id="90c89-766">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="90c89-766">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="90c89-767">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="90c89-767">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="90c89-768">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="90c89-768">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="90c89-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90c89-769">Az.RecoveryServices</span></span>
<span data-ttu-id="90c89-770">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="90c89-770">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="90c89-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-771">Az.Resources</span></span>
* <span data-ttu-id="90c89-772">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="90c89-772">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="90c89-773">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="90c89-773">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="90c89-774">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="90c89-774">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="90c89-775">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="90c89-775">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="90c89-776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-776">Az.Sql</span></span>
* <span data-ttu-id="90c89-777">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="90c89-777">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="90c89-778">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="90c89-778">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="90c89-779">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="90c89-779">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="90c89-780">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="90c89-780">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="90c89-781">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="90c89-781">Az.Accounts</span></span>
* <span data-ttu-id="90c89-782">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="90c89-782">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="90c89-783">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="90c89-783">Az.AnalysisServices</span></span>
* <span data-ttu-id="90c89-784">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="90c89-784">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="90c89-785">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90c89-785">Az.RecoveryServices</span></span>
* <span data-ttu-id="90c89-786">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="90c89-786">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="90c89-787">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="90c89-787">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="90c89-788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="90c89-788">Az.Accounts</span></span>
* <span data-ttu-id="90c89-789">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-789">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="90c89-790">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="90c89-790">Update incorrect online help URLs</span></span>
* <span data-ttu-id="90c89-791">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="90c89-791">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="90c89-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="90c89-792">Az.Aks</span></span>
* <span data-ttu-id="90c89-793">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="90c89-793">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="90c89-794">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="90c89-794">Az.Automation</span></span>
* <span data-ttu-id="90c89-795">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="90c89-795">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="90c89-796">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="90c89-796">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="90c89-797">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="90c89-797">Az.Cdn</span></span>
* <span data-ttu-id="90c89-798">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="90c89-798">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-799">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-799">Az.Compute</span></span>
* <span data-ttu-id="90c89-800">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="90c89-800">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="90c89-801">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="90c89-801">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="90c89-802">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="90c89-802">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="90c89-803">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="90c89-803">Az.ContainerRegistry</span></span>
* <span data-ttu-id="90c89-804">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="90c89-804">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="90c89-805">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="90c89-805">Az.DataFactory</span></span>
* <span data-ttu-id="90c89-806">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="90c89-806">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="90c89-807">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="90c89-807">Az.DataLakeStore</span></span>
* <span data-ttu-id="90c89-808">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="90c89-808">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="90c89-809">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="90c89-809">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="90c89-810">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="90c89-810">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="90c89-811">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="90c89-811">Az.IotHub</span></span>
* <span data-ttu-id="90c89-812">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="90c89-812">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="90c89-813">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="90c89-813">Az.KeyVault</span></span>
* <span data-ttu-id="90c89-814">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="90c89-814">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="90c89-815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="90c89-815">Az.Network</span></span>
* <span data-ttu-id="90c89-816">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="90c89-816">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="90c89-817">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-817">Az.Resources</span></span>
* <span data-ttu-id="90c89-818">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="90c89-818">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="90c89-819">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="90c89-819">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="90c89-820">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="90c89-820">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="90c89-821">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="90c89-821">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="90c89-822">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="90c89-822">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="90c89-823">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="90c89-823">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="90c89-824">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="90c89-824">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="90c89-825">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="90c89-825">Az.ServiceFabric</span></span>
* <span data-ttu-id="90c89-826">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="90c89-826">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="90c89-827">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="90c89-827">Fix some error messages.</span></span>
* <span data-ttu-id="90c89-828">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="90c89-828">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="90c89-829">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="90c89-829">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="90c89-830">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="90c89-830">Az.SignalR</span></span>
* <span data-ttu-id="90c89-831">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="90c89-831">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="90c89-832">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-832">Az.Sql</span></span>
* <span data-ttu-id="90c89-833">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="90c89-833">Update incorrect online help URLs</span></span>
* <span data-ttu-id="90c89-834">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="90c89-834">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="90c89-835">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="90c89-835">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="90c89-836">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="90c89-836">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="90c89-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="90c89-837">Az.Storage</span></span>
* <span data-ttu-id="90c89-838">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="90c89-838">Update incorrect online help URLs</span></span>
* <span data-ttu-id="90c89-839">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="90c89-839">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="90c89-840">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="90c89-840">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="90c89-841">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="90c89-841">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="90c89-842">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="90c89-842">Az.TrafficManager</span></span>
* <span data-ttu-id="90c89-843">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="90c89-843">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="90c89-844">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="90c89-844">Az.Websites</span></span>
* <span data-ttu-id="90c89-845">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="90c89-845">Update incorrect online help URLs</span></span>
* <span data-ttu-id="90c89-846">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="90c89-846">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="90c89-847">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="90c89-847">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="90c89-848">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="90c89-848">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="90c89-849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="90c89-849">Az.Accounts</span></span>
* <span data-ttu-id="90c89-850">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="90c89-850">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-851">Az.Compute</span></span>
* <span data-ttu-id="90c89-852">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="90c89-852">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="90c89-853">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="90c89-853">Updated the description of ID in help files</span></span>
* <span data-ttu-id="90c89-854">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="90c89-854">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="90c89-855">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="90c89-855">Az.DataLakeStore</span></span>
* <span data-ttu-id="90c89-856">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="90c89-856">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="90c89-857">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="90c89-857">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="90c89-858">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="90c89-858">Az.EventGrid</span></span>
* <span data-ttu-id="90c89-859">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="90c89-859">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="90c89-860">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="90c89-860">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="90c89-861">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="90c89-861">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="90c89-862">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="90c89-862">Event Time-To-Live,</span></span>
        - <span data-ttu-id="90c89-863">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="90c89-863">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="90c89-864">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="90c89-864">Dead letter endpoint.</span></span>
    - <span data-ttu-id="90c89-865">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="90c89-865">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="90c89-866">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="90c89-866">Event Time-To-Live,</span></span>
        - <span data-ttu-id="90c89-867">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="90c89-867">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="90c89-868">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="90c89-868">Dead letter endpoint.</span></span>
* <span data-ttu-id="90c89-869">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="90c89-869">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="90c89-870">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="90c89-870">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="90c89-871">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="90c89-871">Az.IotHub</span></span>
* <span data-ttu-id="90c89-872">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="90c89-872">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="90c89-873">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="90c89-873">Az.LogicApp</span></span>
* <span data-ttu-id="90c89-874">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="90c89-874">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="90c89-875">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-875">Az.Resources</span></span>
* <span data-ttu-id="90c89-876">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="90c89-876">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="90c89-877">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="90c89-877">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="90c89-878">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="90c89-878">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="90c89-879">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="90c89-879">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="90c89-880">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="90c89-880">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="90c89-881">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="90c89-881">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="90c89-882">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="90c89-882">Az.SignalR</span></span>
* <span data-ttu-id="90c89-883">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="90c89-883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="90c89-884">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-884">Az.Sql</span></span>
* <span data-ttu-id="90c89-885">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="90c89-885">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="90c89-886">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="90c89-886">Az.Storage</span></span>
* <span data-ttu-id="90c89-887">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="90c89-887">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="90c89-888">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="90c89-888">New-AzStorageContext</span></span>
* <span data-ttu-id="90c89-889">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="90c89-889">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="90c89-890">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="90c89-890">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="90c89-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="90c89-891">Az.Websites</span></span>
* <span data-ttu-id="90c89-892">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="90c89-892">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="90c89-893">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="90c89-893">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="90c89-894">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="90c89-894">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="90c89-895">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="90c89-895">General</span></span>

- <span data-ttu-id="90c89-896">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="90c89-896">General Availability of Az Module</span></span>
- <span data-ttu-id="90c89-897">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-897">Online help for each module</span></span>
- <span data-ttu-id="90c89-898">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="90c89-898">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="90c89-899">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="90c89-899">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="90c89-900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="90c89-900">Az.Accounts</span></span>
- <span data-ttu-id="90c89-901">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="90c89-901">Changed from Az.Profile</span></span>
- <span data-ttu-id="90c89-902">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-902">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="90c89-903">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="90c89-903">Az.ApiManagement</span></span>
- <span data-ttu-id="90c89-904">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="90c89-904">Fixes for #7002</span></span>
- <span data-ttu-id="90c89-905">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="90c89-905">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="90c89-906">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="90c89-906">Az.Batch</span></span>
- <span data-ttu-id="90c89-907">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="90c89-907">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="90c89-908">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="90c89-908">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="90c89-909">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="90c89-909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="90c89-910">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="90c89-910">Az.Billing</span></span>
- <span data-ttu-id="90c89-911">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="90c89-911">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="90c89-912">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="90c89-912">Az.CognitivServices</span></span>
- <span data-ttu-id="90c89-913">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="90c89-913">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="90c89-914">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="90c89-914">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="90c89-915">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="90c89-915">Az.ContainerInstance</span></span>
- <span data-ttu-id="90c89-916">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="90c89-916">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="90c89-917">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="90c89-917">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="90c89-918">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="90c89-918">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="90c89-919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="90c89-919">Az.DataLakeStore</span></span>
- <span data-ttu-id="90c89-920">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="90c89-920">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="90c89-921">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="90c89-921">Az.Monitor</span></span>
- <span data-ttu-id="90c89-922">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="90c89-922">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="90c89-923">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="90c89-923">Az.KeyVault</span></span>
- <span data-ttu-id="90c89-924">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="90c89-924">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="90c89-925">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="90c89-925">Az.MachineLearning</span></span>
- <span data-ttu-id="90c89-926">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="90c89-926">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="90c89-927">Az.Media</span><span class="sxs-lookup"><span data-stu-id="90c89-927">Az.Media</span></span>
- <span data-ttu-id="90c89-928">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="90c89-928">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="90c89-929">Az.Network</span><span class="sxs-lookup"><span data-stu-id="90c89-929">Az.Network</span></span>
<span data-ttu-id="90c89-930">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="90c89-930">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="90c89-931">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="90c89-931">New cmdlets added:</span></span>
        - <span data-ttu-id="90c89-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="90c89-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="90c89-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="90c89-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="90c89-934">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="90c89-934">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="90c89-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="90c89-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="90c89-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="90c89-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="90c89-937">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="90c89-937">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="90c89-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="90c89-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="90c89-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="90c89-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="90c89-940">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="90c89-940">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="90c89-941">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90c89-941">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="90c89-942">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90c89-942">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="90c89-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90c89-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="90c89-944">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90c89-944">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="90c89-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="90c89-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="90c89-946">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="90c89-946">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="90c89-947">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="90c89-947">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="90c89-948">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="90c89-948">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="90c89-949">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="90c89-949">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="90c89-950">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="90c89-950">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="90c89-951">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="90c89-951">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="90c89-952">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="90c89-952">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="90c89-953">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="90c89-953">Az.OperationalInsights</span></span>
- <span data-ttu-id="90c89-954">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="90c89-954">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="90c89-955">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="90c89-955">Az.Profile</span></span>
- <span data-ttu-id="90c89-956">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="90c89-956">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="90c89-957">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90c89-957">Az.RecoveryServices</span></span>
- <span data-ttu-id="90c89-958">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="90c89-958">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="90c89-959">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-959">Az.Resources</span></span>
- <span data-ttu-id="90c89-960">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="90c89-960">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="90c89-961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="90c89-961">Az.ServiceFabric</span></span>
- <span data-ttu-id="90c89-962">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="90c89-962">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="90c89-963">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="90c89-963">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="90c89-964">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="90c89-964">Az.SIgnalR</span></span>
- <span data-ttu-id="90c89-965">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="90c89-965">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="90c89-966">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-966">Az.Sql</span></span>
- <span data-ttu-id="90c89-967">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="90c89-967">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="90c89-968">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="90c89-968">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="90c89-969">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="90c89-969">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="90c89-970">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="90c89-970">Az.Storage</span></span>
- <span data-ttu-id="90c89-971">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="90c89-971">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="90c89-972">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="90c89-972">Az.Websites</span></span>
- <span data-ttu-id="90c89-973">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="90c89-973">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="90c89-974">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="90c89-974">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="90c89-975">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="90c89-975">General</span></span>

* <span data-ttu-id="90c89-976">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="90c89-976">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="90c89-977">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-977">Az.Compute</span></span>

* <span data-ttu-id="90c89-978">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="90c89-978">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="90c89-979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="90c89-979">Az.DataLakeStore</span></span>

* <span data-ttu-id="90c89-980">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="90c89-980">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="90c89-981">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="90c89-981">Az.FrontDoor</span></span>

* <span data-ttu-id="90c89-982">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="90c89-982">Fixed some broken links</span></span>
    - <span data-ttu-id="90c89-983">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="90c89-983">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="90c89-984">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="90c89-984">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="90c89-985">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="90c89-985">Az.RecoveryServices</span></span>

* <span data-ttu-id="90c89-986">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="90c89-986">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="90c89-987">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="90c89-987">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="90c89-988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-988">Az.Resources</span></span>

* <span data-ttu-id="90c89-989">https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="90c89-989">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="90c89-990">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="90c89-990">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="90c89-991">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-991">Az.Sql</span></span>

* <span data-ttu-id="90c89-992">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="90c89-992">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="90c89-993">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="90c89-993">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="90c89-994">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="90c89-994">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="90c89-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="90c89-995">Az.Storage</span></span>

* <span data-ttu-id="90c89-996">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="90c89-996">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="90c89-997">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="90c89-997">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="90c89-998">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="90c89-998">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="90c89-999">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="90c89-999">Support Static Website configuration</span></span>
    - <span data-ttu-id="90c89-1000">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="90c89-1000">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="90c89-1001">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="90c89-1001">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="90c89-1002">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="90c89-1002">Az.Websites</span></span>

* <span data-ttu-id="90c89-1003">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="90c89-1003">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="90c89-1004">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="90c89-1004">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="90c89-1005">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="90c89-1005">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="90c89-1006">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="90c89-1006">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="90c89-1007">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="90c89-1007">Az.ApiManagement</span></span>
* <span data-ttu-id="90c89-1008">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="90c89-1008">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="90c89-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="90c89-1009">Az.Automation</span></span>
* <span data-ttu-id="90c89-1010">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="90c89-1010">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="90c89-1011">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="90c89-1011">Added Update Management cmdlets</span></span>
* <span data-ttu-id="90c89-1012">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="90c89-1012">Added Source Control cmdlets</span></span>
* <span data-ttu-id="90c89-1013">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="90c89-1013">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="90c89-1014">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="90c89-1014">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="90c89-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-1015">Az.Compute</span></span>
* <span data-ttu-id="90c89-1016">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="90c89-1016">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="90c89-1017">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="90c89-1017">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="90c89-1018">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="90c89-1018">Az.ContainerInstance</span></span>
* <span data-ttu-id="90c89-1019">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="90c89-1019">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="90c89-1020">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="90c89-1020">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="90c89-1021">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="90c89-1021">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="90c89-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="90c89-1022">Az.Network</span></span>
* <span data-ttu-id="90c89-1023">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="90c89-1023">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="90c89-1024">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="90c89-1024">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="90c89-1025">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="90c89-1025">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="90c89-1026">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="90c89-1026">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="90c89-1027">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="90c89-1027">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="90c89-1028">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="90c89-1028">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="90c89-1029">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="90c89-1029">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="90c89-1030">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="90c89-1030">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="90c89-1031">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="90c89-1031">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="90c89-1032">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="90c89-1032">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="90c89-1033">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="90c89-1033">Az.Relay</span></span>
* <span data-ttu-id="90c89-1034">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="90c89-1034">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="90c89-1035">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-1035">Az.Resources</span></span>
* <span data-ttu-id="90c89-1036">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="90c89-1036">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="90c89-1037">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="90c89-1037">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="90c89-1038">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="90c89-1038">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="90c89-1039">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="90c89-1039">Az.ServiceFabric</span></span>
* <span data-ttu-id="90c89-1040">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="90c89-1040">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="90c89-1041">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-1041">Az.Sql</span></span>
* <span data-ttu-id="90c89-1042">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="90c89-1042">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="90c89-1043">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="90c89-1043">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="90c89-1044">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="90c89-1044">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="90c89-1045">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="90c89-1045">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="90c89-1046">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="90c89-1046">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="90c89-1047">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="90c89-1047">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="90c89-1048">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="90c89-1048">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="90c89-1049">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="90c89-1049">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="90c89-1050">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="90c89-1050">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="90c89-1051">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="90c89-1051">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="90c89-1052">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="90c89-1052">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="90c89-1053">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="90c89-1053">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="90c89-1054">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="90c89-1054">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="90c89-1055">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="90c89-1055">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="90c89-1056">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="90c89-1056">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="90c89-1057">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="90c89-1057">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="90c89-1058">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="90c89-1058">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="90c89-1059">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="90c89-1059">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="90c89-1060">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="90c89-1060">General</span></span>
* <span data-ttu-id="90c89-1061">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="90c89-1061">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="90c89-1062">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="90c89-1062">Az.Profile</span></span>
* <span data-ttu-id="90c89-1063">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="90c89-1063">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="90c89-1064">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="90c89-1064">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="90c89-1065">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="90c89-1065">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="90c89-1066">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="90c89-1066">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="90c89-1067">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="90c89-1067">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="90c89-1068">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="90c89-1068">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="90c89-1069">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="90c89-1069">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="90c89-1070">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="90c89-1070">Az.CognitiveServices</span></span>
* <span data-ttu-id="90c89-1071">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="90c89-1071">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-1072">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-1072">Az.Compute</span></span>
* <span data-ttu-id="90c89-1073">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="90c89-1073">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="90c89-1074">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="90c89-1074">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="90c89-1075">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="90c89-1075">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="90c89-1076">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="90c89-1076">Az.DataLakeStore</span></span>
* <span data-ttu-id="90c89-1077">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="90c89-1077">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="90c89-1078">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="90c89-1078">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="90c89-1079">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="90c89-1079">Az.Insights</span></span>
* <span data-ttu-id="90c89-1080">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="90c89-1080">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="90c89-1081">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="90c89-1081">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="90c89-1082">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="90c89-1082">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="90c89-1083">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="90c89-1083">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="90c89-1084">Az.Network</span><span class="sxs-lookup"><span data-stu-id="90c89-1084">Az.Network</span></span>
* <span data-ttu-id="90c89-1085">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="90c89-1085">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="90c89-1086">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="90c89-1086">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="90c89-1087">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="90c89-1087">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="90c89-1088">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="90c89-1088">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="90c89-1089">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="90c89-1089">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="90c89-1090">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="90c89-1090">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="90c89-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="90c89-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="90c89-1092">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="90c89-1092">Az.PolicyInsights</span></span>
* <span data-ttu-id="90c89-1093">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="90c89-1093">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="90c89-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-1094">Az.Resources</span></span>
* <span data-ttu-id="90c89-1095">https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="90c89-1095">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="90c89-1096">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="90c89-1096">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="90c89-1097">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="90c89-1097">Az.ServiceBus</span></span>
* <span data-ttu-id="90c89-1098">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="90c89-1098">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="90c89-1099">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="90c89-1099">Az.ServiceFabric</span></span>
* <span data-ttu-id="90c89-1100">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="90c89-1100">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="90c89-1101">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="90c89-1101">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="90c89-1102">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="90c89-1102">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="90c89-1103">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="90c89-1103">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="90c89-1104">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="90c89-1104">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="90c89-1105">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="90c89-1105">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="90c89-1106">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="90c89-1106">Az.Profile</span></span>
* <span data-ttu-id="90c89-1107">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="90c89-1107">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="90c89-1108">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="90c89-1108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-1109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-1109">Az.Compute</span></span>
* <span data-ttu-id="90c89-1110">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="90c89-1110">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="90c89-1111">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="90c89-1111">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="90c89-1112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="90c89-1112">Az.DataLakeStore</span></span>
* <span data-ttu-id="90c89-1113">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="90c89-1113">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="90c89-1114">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="90c89-1114">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="90c89-1115">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="90c89-1115">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="90c89-1116">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="90c89-1116">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="90c89-1117">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="90c89-1117">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="90c89-1118">Az.Network</span><span class="sxs-lookup"><span data-stu-id="90c89-1118">Az.Network</span></span>
* <span data-ttu-id="90c89-1119">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="90c89-1119">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="90c89-1120">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="90c89-1120">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="90c89-1121">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-1121">Az.Resources</span></span>
* <span data-ttu-id="90c89-1122">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="90c89-1122">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="90c89-1123">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="90c89-1123">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="90c89-1124">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="90c89-1124">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="90c89-1125">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="90c89-1125">Azure.Storage</span></span>
* <span data-ttu-id="90c89-1126">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="90c89-1126">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="90c89-1127">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="90c89-1127">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="90c89-1128">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="90c89-1128">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="90c89-1129">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="90c89-1129">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="90c89-1130">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="90c89-1130">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="90c89-1131">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="90c89-1131">Az.CognitiveServices</span></span>
* <span data-ttu-id="90c89-1132">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="90c89-1132">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="90c89-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="90c89-1133">Az.Compute</span></span>
* <span data-ttu-id="90c89-1134">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="90c89-1134">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="90c89-1135">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="90c89-1135">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="90c89-1136">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="90c89-1136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="90c89-1137">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="90c89-1137">Az.DataFactoryV2</span></span>
* <span data-ttu-id="90c89-1138">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="90c89-1138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="90c89-1139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="90c89-1139">Az.Network</span></span>
* <span data-ttu-id="90c89-1140">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="90c89-1140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="90c89-1141">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="90c89-1141">new cmdlets added</span></span>
    - <span data-ttu-id="90c89-1142">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="90c89-1142">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="90c89-1143">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="90c89-1143">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="90c89-1144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="90c89-1144">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="90c89-1145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="90c89-1145">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="90c89-1146">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="90c89-1146">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="90c89-1147">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="90c89-1147">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="90c89-1148">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="90c89-1148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="90c89-1149">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="90c89-1149">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="90c89-1150">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="90c89-1150">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="90c89-1151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="90c89-1151">Az.RedisCache</span></span>
* <span data-ttu-id="90c89-1152">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="90c89-1152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="90c89-1153">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="90c89-1153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="90c89-1154">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="90c89-1154">Az.Resources</span></span>
* <span data-ttu-id="90c89-1155">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="90c89-1155">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="90c89-1156">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="90c89-1156">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="90c89-1157">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="90c89-1157">Az.Sql</span></span>
* <span data-ttu-id="90c89-1158">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="90c89-1158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="90c89-1159">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="90c89-1159">Az.Websites</span></span>
* <span data-ttu-id="90c89-1160">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="90c89-1160">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="90c89-1161">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="90c89-1161">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="90c89-1162">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="90c89-1162">0.2.0 - September 2018</span></span>
 <span data-ttu-id="90c89-1163">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="90c89-1163">Initial Release</span></span>