---
ms.openlocfilehash: f89d13d6bbedaea29b62287942d8c7a509abe32b
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052634"
---
## <a name="260---august-2019"></a><span data-ttu-id="67dc6-101">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="67dc6-101">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="67dc6-102">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="67dc6-102">General</span></span>
* <span data-ttu-id="67dc6-103">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="67dc6-103">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="67dc6-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="67dc6-104">Az.Accounts</span></span>
* <span data-ttu-id="67dc6-105">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="67dc6-105">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="67dc6-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="67dc6-106">Az.Aks</span></span>
* <span data-ttu-id="67dc6-107">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="67dc6-107">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="67dc6-108">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="67dc6-108">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="67dc6-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="67dc6-109">Az.ApiManagement</span></span>
* <span data-ttu-id="67dc6-110">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="67dc6-110">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="67dc6-111">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="67dc6-111">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="67dc6-112">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="67dc6-112">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="67dc6-113">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="67dc6-113">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="67dc6-114">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="67dc6-114">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="67dc6-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="67dc6-115">Az.Batch</span></span>
* <span data-ttu-id="67dc6-116">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="67dc6-116">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="67dc6-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="67dc6-117">Az.Cdn</span></span>
* <span data-ttu-id="67dc6-118">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="67dc6-118">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-119">Az.Compute</span></span>
* <span data-ttu-id="67dc6-120">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-120">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="67dc6-121">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-121">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="67dc6-122">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-122">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="67dc6-123">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="67dc6-123">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="67dc6-124">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="67dc6-124">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="67dc6-125">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-125">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="67dc6-126">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="67dc6-126">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="67dc6-127">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="67dc6-127">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="67dc6-128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="67dc6-128">Az.DataFactory</span></span>
* <span data-ttu-id="67dc6-129">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="67dc6-129">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="67dc6-130">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="67dc6-130">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="67dc6-131">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="67dc6-131">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="67dc6-132">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="67dc6-132">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="67dc6-133">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="67dc6-133">Az.DataLakeStore</span></span>
* <span data-ttu-id="67dc6-134">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="67dc6-134">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="67dc6-135">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="67dc6-135">Az.EventHub</span></span>
* <span data-ttu-id="67dc6-136">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="67dc6-136">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="67dc6-137">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="67dc6-137">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="67dc6-138">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-138">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="67dc6-139">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="67dc6-139">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="67dc6-140">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="67dc6-140">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="67dc6-141">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="67dc6-141">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="67dc6-142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="67dc6-142">Az.Monitor</span></span>
* <span data-ttu-id="67dc6-143">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="67dc6-143">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="67dc6-144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-144">Az.Network</span></span>
* <span data-ttu-id="67dc6-145">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="67dc6-145">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="67dc6-146">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="67dc6-146">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="67dc6-147">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="67dc6-147">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="67dc6-148">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="67dc6-148">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="67dc6-149">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-149">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="67dc6-150">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="67dc6-150">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="67dc6-151">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="67dc6-151">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="67dc6-152">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="67dc6-152">Az.OperationalInsights</span></span>
* <span data-ttu-id="67dc6-153">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="67dc6-153">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="67dc6-154">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-154">Added example</span></span>
    - <span data-ttu-id="67dc6-155">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="67dc6-155">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="67dc6-156">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-156">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="67dc6-157">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="67dc6-157">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="67dc6-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="67dc6-159">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="67dc6-159">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="67dc6-160">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-160">Az.Resources</span></span>
* <span data-ttu-id="67dc6-161">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="67dc6-161">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="67dc6-162">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-162">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="67dc6-163">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="67dc6-163">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="67dc6-164">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-164">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="67dc6-165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="67dc6-165">Az.ServiceBus</span></span>
* <span data-ttu-id="67dc6-166">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="67dc6-166">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="67dc6-167">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="67dc6-167">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="67dc6-168">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="67dc6-168">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="67dc6-169">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="67dc6-169">Az.ServiceFabric</span></span>
* <span data-ttu-id="67dc6-170">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="67dc6-170">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="67dc6-171">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="67dc6-171">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="67dc6-172">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="67dc6-172">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="67dc6-173">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="67dc6-173">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="67dc6-174">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="67dc6-174">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="67dc6-175">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="67dc6-175">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="67dc6-176">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-176">Az.Sql</span></span>
* <span data-ttu-id="67dc6-177">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="67dc6-177">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="67dc6-178">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="67dc6-178">Az.Storage</span></span>
* <span data-ttu-id="67dc6-179">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="67dc6-179">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="67dc6-180">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-180">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="67dc6-181">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="67dc6-181">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="67dc6-182">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="67dc6-182">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="67dc6-183">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="67dc6-183">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="67dc6-184">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="67dc6-184">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="67dc6-185">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="67dc6-185">Az.Websites</span></span>
* <span data-ttu-id="67dc6-186">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-186">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="67dc6-187">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="67dc6-187">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="67dc6-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="67dc6-188">Az.Accounts</span></span>
* <span data-ttu-id="67dc6-189">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="67dc6-189">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="67dc6-190">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="67dc6-190">Az.ApplicationInsights</span></span>
* <span data-ttu-id="67dc6-191">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-191">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="67dc6-192">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="67dc6-192">Az.Automation</span></span>
* <span data-ttu-id="67dc6-193">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-193">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="67dc6-194">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-194">Az.CognitiveServices</span></span>
* <span data-ttu-id="67dc6-195">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="67dc6-195">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-196">Az.Compute</span></span>
* <span data-ttu-id="67dc6-197">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="67dc6-197">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="67dc6-198">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="67dc6-198">Az.ContainerRegistry</span></span>
* <span data-ttu-id="67dc6-199">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-199">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="67dc6-200">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="67dc6-200">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="67dc6-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="67dc6-201">Az.DataFactory</span></span>
* <span data-ttu-id="67dc6-202">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="67dc6-202">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="67dc6-203">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-203">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="67dc6-204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="67dc6-204">Az.EventHub</span></span>
* <span data-ttu-id="67dc6-205">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="67dc6-205">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="67dc6-206">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="67dc6-206">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="67dc6-207">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="67dc6-207">Az.KeyVault</span></span>
* <span data-ttu-id="67dc6-208">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="67dc6-208">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="67dc6-209">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="67dc6-209">Az.LogicApp</span></span>
* <span data-ttu-id="67dc6-210">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="67dc6-210">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="67dc6-211">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="67dc6-211">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="67dc6-212">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-212">Az.ManagedServices</span></span>
* <span data-ttu-id="67dc6-213">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-213">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="67dc6-214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-214">Az.Network</span></span>
* <span data-ttu-id="67dc6-215">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-215">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="67dc6-216">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="67dc6-216">New cmdlets</span></span>
        - <span data-ttu-id="67dc6-217">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="67dc6-217">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="67dc6-218">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="67dc6-218">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="67dc6-219">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="67dc6-219">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="67dc6-220">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="67dc6-220">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="67dc6-221">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="67dc6-221">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="67dc6-222">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="67dc6-222">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="67dc6-223">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="67dc6-223">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="67dc6-224">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="67dc6-224">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="67dc6-225">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="67dc6-225">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="67dc6-226">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="67dc6-226">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="67dc6-227">-PrivateEndpointNetworkPoliciesFlag opcionális paraméter hozzáadva, amely azt jelzi, hogy az alhálózaton be vagy ki van-e kapcsolva a hálózati szabályok alkalmazása a privát végpontra.</span><span class="sxs-lookup"><span data-stu-id="67dc6-227">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="67dc6-228">-PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter hozzáadva, amely azt jelzi, hogy az alhálózaton be vagy ki van-e kapcsolva a hálózati szabályok alkalmazása a privát kapcsolatszolgáltatásra.</span><span class="sxs-lookup"><span data-stu-id="67dc6-228">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="67dc6-229">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="67dc6-229">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="67dc6-230">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-230">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="67dc6-231">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="67dc6-231">Updated cmdlets</span></span>
        - <span data-ttu-id="67dc6-232">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="67dc6-232">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="67dc6-233">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="67dc6-233">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="67dc6-234">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="67dc6-234">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="67dc6-235">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="67dc6-235">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="67dc6-236">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="67dc6-236">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="67dc6-237">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="67dc6-237">Updated cmdlet:</span></span>
        - <span data-ttu-id="67dc6-238">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="67dc6-238">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="67dc6-239">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="67dc6-239">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="67dc6-240">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="67dc6-240">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="67dc6-241">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="67dc6-241">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="67dc6-242">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="67dc6-242">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="67dc6-243">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="67dc6-243">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="67dc6-244">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="67dc6-244">Az.OperationalInsights</span></span>
* <span data-ttu-id="67dc6-245">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="67dc6-245">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="67dc6-246">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="67dc6-246">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="67dc6-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="67dc6-248">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-248">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="67dc6-249">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-249">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="67dc6-250">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-250">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="67dc6-251">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-251">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="67dc6-252">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-252">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="67dc6-253">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-253">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="67dc6-254">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-254">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="67dc6-255">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-255">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="67dc6-256">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-256">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="67dc6-257">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-257">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="67dc6-258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-258">Az.Resources</span></span>
- <span data-ttu-id="67dc6-259">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-259">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="67dc6-260">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="67dc6-260">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="67dc6-261">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="67dc6-261">Az.ServiceBus</span></span>
* <span data-ttu-id="67dc6-262">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="67dc6-262">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="67dc6-263">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="67dc6-263">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="67dc6-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-264">Az.Sql</span></span>
* <span data-ttu-id="67dc6-265">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-265">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="67dc6-266">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-266">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="67dc6-267">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="67dc6-267">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="67dc6-268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="67dc6-268">Az.Storage</span></span>
* <span data-ttu-id="67dc6-269">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="67dc6-269">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="67dc6-270">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="67dc6-270">Az.StorageSync</span></span>
* <span data-ttu-id="67dc6-271">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="67dc6-271">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="67dc6-272">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="67dc6-272">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="67dc6-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="67dc6-273">Az.Websites</span></span>
* <span data-ttu-id="67dc6-274">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="67dc6-274">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="67dc6-275">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-275">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="67dc6-276">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-276">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="67dc6-277">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="67dc6-277">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="67dc6-278">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="67dc6-278">Az.Accounts</span></span>
* <span data-ttu-id="67dc6-279">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="67dc6-279">Add support for profile cmdlets</span></span>
* <span data-ttu-id="67dc6-280">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="67dc6-280">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="67dc6-281">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="67dc6-281">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="67dc6-282">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="67dc6-282">Az.Advisor</span></span>
* <span data-ttu-id="67dc6-283">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="67dc6-283">GA release of Az.Advisor</span></span>
* <span data-ttu-id="67dc6-284">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="67dc6-284">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="67dc6-285">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="67dc6-285">Az.ApiManagement</span></span>
* <span data-ttu-id="67dc6-286">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="67dc6-286">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="67dc6-287">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="67dc6-287">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="67dc6-288">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-288">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="67dc6-289">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-289">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="67dc6-290">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="67dc6-290">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="67dc6-291">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="67dc6-291">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="67dc6-292">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="67dc6-292">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="67dc6-293">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="67dc6-293">Az.Automation</span></span>
* <span data-ttu-id="67dc6-294">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="67dc6-294">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-295">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-295">Az.Compute</span></span>
* <span data-ttu-id="67dc6-296">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-296">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="67dc6-297">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="67dc6-297">Az.DataFactory</span></span>
* <span data-ttu-id="67dc6-298">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="67dc6-298">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="67dc6-299">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="67dc6-299">Az.EventGrid</span></span>
* <span data-ttu-id="67dc6-300">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="67dc6-300">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="67dc6-301">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="67dc6-301">Az.IotHub</span></span>
* <span data-ttu-id="67dc6-302">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="67dc6-302">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="67dc6-303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-303">Az.Network</span></span>
* <span data-ttu-id="67dc6-304">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-304">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="67dc6-305">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="67dc6-305">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="67dc6-306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="67dc6-306">Az.PolicyInsights</span></span>
* <span data-ttu-id="67dc6-307">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="67dc6-307">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="67dc6-308">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="67dc6-308">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="67dc6-309">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="67dc6-309">Az.OperationalInsights</span></span>
* <span data-ttu-id="67dc6-310">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="67dc6-310">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="67dc6-311">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-311">Az.RecoveryServices</span></span>
* <span data-ttu-id="67dc6-312">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-312">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="67dc6-313">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-313">Az.Resources</span></span>
    - <span data-ttu-id="67dc6-314">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-314">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="67dc6-315">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-315">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="67dc6-316">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-316">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="67dc6-317">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-317">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="67dc6-318">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="67dc6-318">Az.ServiceBus</span></span>
* <span data-ttu-id="67dc6-319">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="67dc6-319">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="67dc6-320">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-320">Az.Sql</span></span>
* <span data-ttu-id="67dc6-321">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-321">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="67dc6-322">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="67dc6-322">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="67dc6-323">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="67dc6-323">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="67dc6-324">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="67dc6-324">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="67dc6-325">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="67dc6-325">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="67dc6-326">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="67dc6-326">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="67dc6-327">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="67dc6-327">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="67dc6-328">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="67dc6-328">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="67dc6-329">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="67dc6-329">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="67dc6-330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="67dc6-330">Az.Storage</span></span>
* <span data-ttu-id="67dc6-331">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="67dc6-331">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="67dc6-332">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="67dc6-332">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="67dc6-333">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="67dc6-333">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="67dc6-334">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="67dc6-334">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="67dc6-335">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="67dc6-335">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="67dc6-336">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67dc6-336">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="67dc6-337">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67dc6-337">Set-AzStorageAccount</span></span>
* <span data-ttu-id="67dc6-338">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="67dc6-338">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="67dc6-339">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="67dc6-339">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="67dc6-340">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="67dc6-340">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="67dc6-341">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="67dc6-341">Az.StorageSync</span></span>
* <span data-ttu-id="67dc6-342">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="67dc6-342">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="67dc6-343">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="67dc6-343">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="67dc6-344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="67dc6-344">Az.Accounts</span></span>
* <span data-ttu-id="67dc6-345">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-345">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="67dc6-346">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="67dc6-346">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="67dc6-347">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-347">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="67dc6-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="67dc6-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="67dc6-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="67dc6-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-350">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-350">Az.Compute</span></span>
* <span data-ttu-id="67dc6-351">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="67dc6-351">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="67dc6-352">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="67dc6-352">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="67dc6-353">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="67dc6-353">Az.Dns</span></span>
* <span data-ttu-id="67dc6-354">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="67dc6-354">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="67dc6-355">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="67dc6-355">Az.EventGrid</span></span>
* <span data-ttu-id="67dc6-356">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="67dc6-356">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="67dc6-357">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="67dc6-357">New cmdlets:</span></span>
    - <span data-ttu-id="67dc6-358">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="67dc6-358">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="67dc6-359">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="67dc6-359">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="67dc6-360">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="67dc6-360">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="67dc6-361">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="67dc6-361">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="67dc6-362">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="67dc6-362">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="67dc6-363">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="67dc6-363">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="67dc6-364">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="67dc6-364">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="67dc6-365">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="67dc6-365">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="67dc6-366">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="67dc6-366">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="67dc6-367">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="67dc6-367">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="67dc6-368">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="67dc6-368">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="67dc6-369">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="67dc6-369">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="67dc6-370">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="67dc6-370">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="67dc6-371">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="67dc6-371">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="67dc6-372">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="67dc6-372">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="67dc6-373">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="67dc6-373">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="67dc6-374">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="67dc6-374">Updated cmdlets:</span></span>
    - <span data-ttu-id="67dc6-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="67dc6-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="67dc6-376">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="67dc6-376">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="67dc6-377">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="67dc6-377">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="67dc6-378">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="67dc6-378">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="67dc6-379">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="67dc6-379">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="67dc6-380">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="67dc6-380">Event subscription expiration date,</span></span>
            - <span data-ttu-id="67dc6-381">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="67dc6-381">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="67dc6-382">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="67dc6-382">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="67dc6-383">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="67dc6-383">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="67dc6-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="67dc6-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="67dc6-385">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="67dc6-385">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="67dc6-386">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="67dc6-386">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="67dc6-387">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="67dc6-387">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="67dc6-388">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="67dc6-388">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="67dc6-389">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="67dc6-389">Az.FrontDoor</span></span>
* <span data-ttu-id="67dc6-390">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="67dc6-390">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="67dc6-391">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="67dc6-391">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="67dc6-392">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="67dc6-392">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="67dc6-393">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="67dc6-393">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="67dc6-394">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-394">Az.Network</span></span>
* <span data-ttu-id="67dc6-395">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-395">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="67dc6-396">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="67dc6-396">New cmdlets</span></span>
        - <span data-ttu-id="67dc6-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="67dc6-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="67dc6-398">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-398">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="67dc6-399">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="67dc6-399">New cmdlets</span></span> 
        - <span data-ttu-id="67dc6-400">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="67dc6-400">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="67dc6-401">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-401">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="67dc6-402">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="67dc6-402">New cmdlets</span></span> 
        - <span data-ttu-id="67dc6-403">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="67dc6-403">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="67dc6-404">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="67dc6-404">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="67dc6-405">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="67dc6-405">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="67dc6-406">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="67dc6-406">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="67dc6-407">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="67dc6-407">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="67dc6-408">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-408">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="67dc6-409">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="67dc6-409">New cmdlets</span></span>
        - <span data-ttu-id="67dc6-410">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="67dc6-410">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="67dc6-411">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="67dc6-411">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="67dc6-412">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="67dc6-412">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="67dc6-413">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="67dc6-413">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="67dc6-414">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="67dc6-414">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="67dc6-415">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="67dc6-415">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="67dc6-416">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="67dc6-416">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="67dc6-417">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="67dc6-417">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="67dc6-418">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="67dc6-418">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="67dc6-419">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="67dc6-419">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="67dc6-420">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="67dc6-420">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="67dc6-421">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="67dc6-421">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="67dc6-422">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-422">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="67dc6-423">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="67dc6-423">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="67dc6-424">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-424">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="67dc6-425">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-425">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="67dc6-426">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="67dc6-426">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="67dc6-427">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-427">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="67dc6-428">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="67dc6-428">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="67dc6-429">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="67dc6-429">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="67dc6-430">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="67dc6-430">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="67dc6-431">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="67dc6-431">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="67dc6-432">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="67dc6-432">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="67dc6-433">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="67dc6-433">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="67dc6-434">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="67dc6-434">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="67dc6-435">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="67dc6-435">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="67dc6-436">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="67dc6-436">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="67dc6-437">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="67dc6-437">Az.OperationalInsights</span></span>
* <span data-ttu-id="67dc6-438">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-438">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="67dc6-439">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-439">Az.Resources</span></span>
* <span data-ttu-id="67dc6-440">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="67dc6-440">Support for additional Template Export options</span></span>
    - <span data-ttu-id="67dc6-441">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-441">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="67dc6-442">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-442">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="67dc6-443">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-443">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="67dc6-444">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="67dc6-444">Az.ServiceFabric</span></span>
* <span data-ttu-id="67dc6-445">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="67dc6-445">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="67dc6-446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-446">Az.Sql</span></span>
* <span data-ttu-id="67dc6-447">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="67dc6-447">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="67dc6-448">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="67dc6-448">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="67dc6-449">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-449">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="67dc6-450">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="67dc6-450">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="67dc6-451">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="67dc6-451">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="67dc6-452">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="67dc6-452">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="67dc6-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="67dc6-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="67dc6-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="67dc6-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="67dc6-455">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="67dc6-455">Az.Storage</span></span>
* <span data-ttu-id="67dc6-456">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="67dc6-456">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="67dc6-457">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67dc6-457">New-AzStorageAccount</span></span>
* <span data-ttu-id="67dc6-458">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="67dc6-458">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="67dc6-459">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="67dc6-459">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="67dc6-460">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="67dc6-460">Az.Websites</span></span>
* <span data-ttu-id="67dc6-461">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="67dc6-461">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="67dc6-462">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-462">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="67dc6-463">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="67dc6-463">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="67dc6-464">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="67dc6-464">Az.Cdn</span></span>
* <span data-ttu-id="67dc6-465">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="67dc6-465">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-466">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-466">Az.Compute</span></span>
* <span data-ttu-id="67dc6-467">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="67dc6-467">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="67dc6-468">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="67dc6-468">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="67dc6-469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="67dc6-469">Az.EventHub</span></span>
* <span data-ttu-id="67dc6-470">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="67dc6-470">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="67dc6-471">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="67dc6-471">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="67dc6-472">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-472">Az.Network</span></span>
* <span data-ttu-id="67dc6-473">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="67dc6-473">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="67dc6-474">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="67dc6-474">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="67dc6-475">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="67dc6-475">Az.PolicyInsights</span></span>
* <span data-ttu-id="67dc6-476">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="67dc6-476">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="67dc6-477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-477">Az.RecoveryServices</span></span>
* <span data-ttu-id="67dc6-478">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="67dc6-478">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="67dc6-479">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="67dc6-479">Az.ServiceBus</span></span>
* <span data-ttu-id="67dc6-480">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="67dc6-480">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="67dc6-481">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="67dc6-481">Az.ServiceFabric</span></span>
* <span data-ttu-id="67dc6-482">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-482">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="67dc6-483">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="67dc6-483">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="67dc6-484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-484">Az.Sql</span></span>
* <span data-ttu-id="67dc6-485">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="67dc6-485">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="67dc6-486">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="67dc6-486">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="67dc6-487">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="67dc6-487">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="67dc6-488">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="67dc6-488">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="67dc6-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="67dc6-489">Az.Websites</span></span>
* <span data-ttu-id="67dc6-490">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="67dc6-490">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="67dc6-491">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="67dc6-491">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="67dc6-492">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="67dc6-492">Az.ApiManagement</span></span>
* <span data-ttu-id="67dc6-493">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="67dc6-493">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="67dc6-494">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="67dc6-494">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="67dc6-495">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="67dc6-495">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="67dc6-496">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="67dc6-496">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="67dc6-497">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="67dc6-497">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="67dc6-498">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-498">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="67dc6-499">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="67dc6-499">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="67dc6-500">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="67dc6-500">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="67dc6-501">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-501">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="67dc6-502">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="67dc6-502">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="67dc6-503">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="67dc6-503">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="67dc6-504">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-504">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="67dc6-505">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-505">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="67dc6-506">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-506">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="67dc6-507">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-507">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="67dc6-508">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="67dc6-508">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="67dc6-509">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-509">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="67dc6-510">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-510">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="67dc6-511">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="67dc6-511">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="67dc6-512">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="67dc6-512">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="67dc6-513">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-513">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="67dc6-514">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="67dc6-514">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="67dc6-515">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="67dc6-515">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="67dc6-516">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-516">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="67dc6-517">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="67dc6-517">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="67dc6-518">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="67dc6-518">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="67dc6-519">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="67dc6-519">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="67dc6-520">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="67dc6-520">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="67dc6-521">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="67dc6-521">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="67dc6-522">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="67dc6-522">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="67dc6-523">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-523">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="67dc6-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="67dc6-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="67dc6-525">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="67dc6-525">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="67dc6-526">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-526">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="67dc6-527">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="67dc6-527">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="67dc6-528">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="67dc6-528">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="67dc6-529">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="67dc6-529">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="67dc6-530">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="67dc6-530">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="67dc6-531">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="67dc6-531">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="67dc6-532">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-532">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="67dc6-533">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="67dc6-533">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="67dc6-534">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="67dc6-534">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="67dc6-535">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="67dc6-535">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="67dc6-536">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="67dc6-536">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="67dc6-537">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-537">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="67dc6-538">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="67dc6-538">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="67dc6-539">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="67dc6-539">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="67dc6-540">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="67dc6-540">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="67dc6-541">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-541">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="67dc6-542">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="67dc6-542">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="67dc6-543">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="67dc6-543">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="67dc6-544">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-544">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="67dc6-545">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="67dc6-545">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="67dc6-546">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-546">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="67dc6-547">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="67dc6-547">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="67dc6-548">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-548">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="67dc6-549">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-549">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="67dc6-550">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-550">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="67dc6-551">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-551">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="67dc6-552">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-552">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="67dc6-553">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-553">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="67dc6-554">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-554">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="67dc6-555">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-555">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="67dc6-556">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-556">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="67dc6-557">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="67dc6-557">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="67dc6-558">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="67dc6-558">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="67dc6-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="67dc6-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="67dc6-560">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="67dc6-560">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="67dc6-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="67dc6-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="67dc6-562">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="67dc6-562">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="67dc6-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="67dc6-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="67dc6-564">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="67dc6-564">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="67dc6-565">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="67dc6-565">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="67dc6-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="67dc6-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="67dc6-567">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="67dc6-567">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="67dc6-568">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="67dc6-568">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="67dc6-569">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="67dc6-569">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="67dc6-570">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="67dc6-570">Az.Automation</span></span>
* <span data-ttu-id="67dc6-571">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-571">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="67dc6-572">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="67dc6-572">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="67dc6-573">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="67dc6-573">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="67dc6-574">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="67dc6-574">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="67dc6-575">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="67dc6-575">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="67dc6-576">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="67dc6-576">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="67dc6-577">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="67dc6-577">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-578">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-578">Az.Compute</span></span>
* <span data-ttu-id="67dc6-579">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-579">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="67dc6-580">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="67dc6-580">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="67dc6-581">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="67dc6-581">Az.DataLakeStore</span></span>
* <span data-ttu-id="67dc6-582">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="67dc6-582">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="67dc6-583">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="67dc6-583">Az.Monitor</span></span>
* <span data-ttu-id="67dc6-584">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="67dc6-584">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="67dc6-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-585">Az.Network</span></span>
* <span data-ttu-id="67dc6-586">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-586">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="67dc6-587">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="67dc6-587">Updated cmdlet:</span></span>
        - <span data-ttu-id="67dc6-588">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="67dc6-588">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="67dc6-589">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="67dc6-589">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="67dc6-590">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-590">Az.Resources</span></span>
* <span data-ttu-id="67dc6-591">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-591">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="67dc6-592">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-592">Az.Sql</span></span>
* <span data-ttu-id="67dc6-593">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="67dc6-593">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="67dc6-594">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="67dc6-594">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="67dc6-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="67dc6-595">Az.Accounts</span></span>
* <span data-ttu-id="67dc6-596">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="67dc6-596">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="67dc6-597">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-597">Az.CognitiveServices</span></span>
* <span data-ttu-id="67dc6-598">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="67dc6-598">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="67dc6-599">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="67dc6-599">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-600">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-600">Az.Compute</span></span>
* <span data-ttu-id="67dc6-601">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="67dc6-601">Proximity placement group feature.</span></span>
    - <span data-ttu-id="67dc6-602">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="67dc6-602">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="67dc6-603">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="67dc6-603">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="67dc6-604">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="67dc6-604">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="67dc6-605">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="67dc6-605">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="67dc6-606">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-606">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="67dc6-607">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="67dc6-607">Breaking changes</span></span>
    - <span data-ttu-id="67dc6-608">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="67dc6-608">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="67dc6-609">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="67dc6-609">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="67dc6-610">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="67dc6-610">Az.DeploymentManager</span></span>
* <span data-ttu-id="67dc6-611">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="67dc6-611">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="67dc6-612">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="67dc6-612">Az.Dns</span></span>
* <span data-ttu-id="67dc6-613">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="67dc6-613">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="67dc6-614">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-614">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="67dc6-615">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="67dc6-615">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="67dc6-616">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="67dc6-616">Az.FrontDoor</span></span>
* <span data-ttu-id="67dc6-617">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="67dc6-617">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="67dc6-618">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="67dc6-618">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="67dc6-619">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="67dc6-619">Az.HDInsight</span></span>
* <span data-ttu-id="67dc6-620">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="67dc6-620">Removed two cmdlets:</span></span>
    - <span data-ttu-id="67dc6-621">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="67dc6-621">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="67dc6-622">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="67dc6-622">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="67dc6-623">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="67dc6-623">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="67dc6-624">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="67dc6-624">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="67dc6-625">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="67dc6-625">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="67dc6-626">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="67dc6-626">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="67dc6-627">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="67dc6-627">Az.Monitor</span></span>
* <span data-ttu-id="67dc6-628">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="67dc6-628">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="67dc6-629">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="67dc6-629">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="67dc6-630">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="67dc6-630">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="67dc6-631">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="67dc6-631">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="67dc6-632">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="67dc6-632">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="67dc6-633">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="67dc6-633">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="67dc6-634">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="67dc6-634">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="67dc6-635">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="67dc6-635">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="67dc6-636">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="67dc6-636">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="67dc6-637">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="67dc6-637">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="67dc6-638">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="67dc6-638">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="67dc6-639">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="67dc6-639">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="67dc6-640">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="67dc6-640">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="67dc6-641">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="67dc6-641">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="67dc6-642">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-642">Az.Network</span></span>
* <span data-ttu-id="67dc6-643">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-643">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="67dc6-644">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="67dc6-644">New cmdlets</span></span>
        - <span data-ttu-id="67dc6-645">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="67dc6-645">New-AzNatGateway</span></span>
        - <span data-ttu-id="67dc6-646">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="67dc6-646">Get-AzNatGateway</span></span>
        - <span data-ttu-id="67dc6-647">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="67dc6-647">Set-AzNatGateway</span></span>
        - <span data-ttu-id="67dc6-648">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="67dc6-648">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="67dc6-649">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="67dc6-649">Updated cmdlets</span></span>
        - <span data-ttu-id="67dc6-650">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="67dc6-650">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="67dc6-651">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="67dc6-651">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="67dc6-652">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="67dc6-652">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="67dc6-653">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="67dc6-653">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="67dc6-654">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="67dc6-654">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="67dc6-655">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="67dc6-655">Az.PolicyInsights</span></span>
* <span data-ttu-id="67dc6-656">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="67dc6-656">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="67dc6-657">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="67dc6-657">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="67dc6-658">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="67dc6-658">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="67dc6-659">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-659">Az.RecoveryServices</span></span>
* <span data-ttu-id="67dc6-660">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="67dc6-660">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="67dc6-661">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="67dc6-661">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="67dc6-662">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="67dc6-662">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="67dc6-663">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="67dc6-663">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="67dc6-664">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="67dc6-664">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="67dc6-665">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="67dc6-665">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="67dc6-666">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="67dc6-666">Az.Relay</span></span>
* <span data-ttu-id="67dc6-667">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="67dc6-667">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="67dc6-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="67dc6-668">Az.ServiceBus</span></span>
* <span data-ttu-id="67dc6-669">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="67dc6-669">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="67dc6-670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="67dc6-670">Az.Storage</span></span>
* <span data-ttu-id="67dc6-671">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="67dc6-671">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="67dc6-672">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="67dc6-672">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="67dc6-673">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="67dc6-673">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="67dc6-674">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67dc6-674">New-AzStorageAccount</span></span>
* <span data-ttu-id="67dc6-675">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="67dc6-675">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="67dc6-676">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67dc6-676">New-AzStorageAccount</span></span>
    - <span data-ttu-id="67dc6-677">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67dc6-677">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="67dc6-678">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67dc6-678">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="67dc6-679">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="67dc6-679">Az.Websites</span></span>
* <span data-ttu-id="67dc6-680">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-680">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="67dc6-681">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="67dc6-681">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="67dc6-682">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="67dc6-682">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="67dc6-683">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="67dc6-683">Highlights since the last major release</span></span>
* <span data-ttu-id="67dc6-684">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="67dc6-684">General availability of `Az` module</span></span>
* <span data-ttu-id="67dc6-685">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="67dc6-685">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="67dc6-686">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="67dc6-686">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="67dc6-687">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-687">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="67dc6-688">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-688">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="67dc6-689">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-689">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="67dc6-690">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-690">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="67dc6-691">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="67dc6-691">Az.Accounts</span></span>
* <span data-ttu-id="67dc6-692">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-692">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="67dc6-693">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="67dc6-693">Az.Batch</span></span>
* <span data-ttu-id="67dc6-694">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="67dc6-695">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="67dc6-695">Az.Cdn</span></span>
* <span data-ttu-id="67dc6-696">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-696">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="67dc6-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="67dc6-698">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-698">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-699">Az.Compute</span></span>
* <span data-ttu-id="67dc6-700">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="67dc6-700">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="67dc6-701">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-701">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="67dc6-702">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="67dc6-702">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="67dc6-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="67dc6-703">Az.DataFactory</span></span>
* <span data-ttu-id="67dc6-704">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="67dc6-704">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="67dc6-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="67dc6-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="67dc6-706">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-706">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="67dc6-707">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="67dc6-707">Az.EventGrid</span></span>
* <span data-ttu-id="67dc6-708">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="67dc6-708">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="67dc6-709">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="67dc6-709">Az.EventHub</span></span>
* <span data-ttu-id="67dc6-710">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="67dc6-710">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="67dc6-711">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="67dc6-711">Az.HDInsight</span></span>
* <span data-ttu-id="67dc6-712">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-712">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="67dc6-713">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="67dc6-713">Az.IotHub</span></span>
* <span data-ttu-id="67dc6-714">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-714">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="67dc6-715">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="67dc6-715">Az.KeyVault</span></span>
* <span data-ttu-id="67dc6-716">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-716">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="67dc6-717">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="67dc6-717">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="67dc6-718">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="67dc6-718">Az.MachineLearning</span></span>
* <span data-ttu-id="67dc6-719">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-719">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="67dc6-720">Az.Media</span><span class="sxs-lookup"><span data-stu-id="67dc6-720">Az.Media</span></span>
* <span data-ttu-id="67dc6-721">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-721">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="67dc6-722">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="67dc6-722">Az.Monitor</span></span>
  * <span data-ttu-id="67dc6-723">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="67dc6-723">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="67dc6-724">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="67dc6-724">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="67dc6-725">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="67dc6-725">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="67dc6-726">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="67dc6-726">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="67dc6-727">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="67dc6-727">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="67dc6-728">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="67dc6-728">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="67dc6-729">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="67dc6-729">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="67dc6-730">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-730">Az.Network</span></span>
* <span data-ttu-id="67dc6-731">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-731">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="67dc6-732">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="67dc6-732">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="67dc6-733">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="67dc6-733">Az.NotificationHubs</span></span>
* <span data-ttu-id="67dc6-734">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-734">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="67dc6-735">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="67dc6-735">Az.OperationalInsights</span></span>
* <span data-ttu-id="67dc6-736">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-736">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="67dc6-737">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="67dc6-737">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="67dc6-738">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-738">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="67dc6-739">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-739">Az.RecoveryServices</span></span>
* <span data-ttu-id="67dc6-740">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-740">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="67dc6-741">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="67dc6-741">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="67dc6-742">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="67dc6-742">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="67dc6-743">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="67dc6-743">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="67dc6-744">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="67dc6-744">Az.RedisCache</span></span>
* <span data-ttu-id="67dc6-745">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-745">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="67dc6-746">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-746">Az.Resources</span></span>
* <span data-ttu-id="67dc6-747">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="67dc6-747">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="67dc6-748">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-748">Az.Sql</span></span>
* <span data-ttu-id="67dc6-749">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="67dc6-749">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="67dc6-750">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-750">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="67dc6-751">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="67dc6-751">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="67dc6-752">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="67dc6-752">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="67dc6-753">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="67dc6-753">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="67dc6-754">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="67dc6-754">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="67dc6-755">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="67dc6-755">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="67dc6-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="67dc6-756">Az.Websites</span></span>
* <span data-ttu-id="67dc6-757">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="67dc6-757">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="67dc6-758">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-758">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="67dc6-759">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="67dc6-759">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="67dc6-760">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="67dc6-760">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="67dc6-761">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="67dc6-761">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="67dc6-762">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="67dc6-762">Highlights since the last major release</span></span>
* <span data-ttu-id="67dc6-763">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="67dc6-763">General availability of `Az` module</span></span>
* <span data-ttu-id="67dc6-764">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="67dc6-764">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="67dc6-765">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="67dc6-765">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="67dc6-766">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-766">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="67dc6-767">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-767">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="67dc6-768">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-768">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="67dc6-769">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-769">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="67dc6-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="67dc6-770">Az.Accounts</span></span>
* <span data-ttu-id="67dc6-771">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="67dc6-771">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="67dc6-772">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-772">Az.AnalysisServices</span></span>
* <span data-ttu-id="67dc6-773">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-773">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="67dc6-774">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-774">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="67dc6-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="67dc6-775">Az.Automation</span></span>
* <span data-ttu-id="67dc6-776">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="67dc6-776">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="67dc6-777">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="67dc6-777">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="67dc6-778">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-778">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-779">Az.Compute</span></span>
* <span data-ttu-id="67dc6-780">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-780">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="67dc6-781">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="67dc6-781">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="67dc6-782">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="67dc6-782">Az.ContainerInstance</span></span>
* <span data-ttu-id="67dc6-783">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="67dc6-783">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="67dc6-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="67dc6-784">Az.DataFactory</span></span>
* <span data-ttu-id="67dc6-785">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="67dc6-785">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="67dc6-786">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="67dc6-786">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="67dc6-787">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-787">Az.Resources</span></span>
* <span data-ttu-id="67dc6-788">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="67dc6-788">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="67dc6-789">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-789">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="67dc6-790">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="67dc6-790">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="67dc6-791">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="67dc6-791">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="67dc6-792">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-792">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="67dc6-793">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="67dc6-793">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="67dc6-794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-794">Az.Sql</span></span>
* <span data-ttu-id="67dc6-795">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="67dc6-795">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="67dc6-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="67dc6-796">Az.Storage</span></span>
* <span data-ttu-id="67dc6-797">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="67dc6-797">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="67dc6-798">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="67dc6-798">New-AzStorageContext</span></span>
* <span data-ttu-id="67dc6-799">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="67dc6-799">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="67dc6-800">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="67dc6-800">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="67dc6-801">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="67dc6-801">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="67dc6-802">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="67dc6-802">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="67dc6-803">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="67dc6-803">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="67dc6-804">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-804">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="67dc6-805">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="67dc6-805">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="67dc6-806">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="67dc6-806">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="67dc6-807">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="67dc6-807">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="67dc6-808">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="67dc6-808">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="67dc6-809">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="67dc6-809">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="67dc6-810">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="67dc6-810">Highlights since the last major release</span></span>
* <span data-ttu-id="67dc6-811">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="67dc6-811">General availability of `Az` module</span></span>
* <span data-ttu-id="67dc6-812">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="67dc6-812">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="67dc6-813">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="67dc6-813">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="67dc6-814">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-814">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="67dc6-815">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-815">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="67dc6-816">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-816">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="67dc6-817">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-817">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="67dc6-818">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="67dc6-818">Az.Automation</span></span>
* <span data-ttu-id="67dc6-819">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="67dc6-819">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="67dc6-820">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="67dc6-820">Dynamic grouping</span></span>
    * <span data-ttu-id="67dc6-821">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="67dc6-821">Pre-Post script</span></span>
    * <span data-ttu-id="67dc6-822">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="67dc6-822">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-823">Az.Compute</span></span>
* <span data-ttu-id="67dc6-824">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-824">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="67dc6-825">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="67dc6-825">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="67dc6-826">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="67dc6-826">Az.KeyVault</span></span>
* <span data-ttu-id="67dc6-827">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-827">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="67dc6-828">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-828">Az.Network</span></span>
* <span data-ttu-id="67dc6-829">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-829">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="67dc6-830">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-830">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="67dc6-831">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-831">Az.RecoveryServices</span></span>
* <span data-ttu-id="67dc6-832">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="67dc6-832">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="67dc6-833">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-833">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="67dc6-834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-834">Az.Resources</span></span>
* <span data-ttu-id="67dc6-835">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-835">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="67dc6-836">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-836">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="67dc6-837">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-837">Az.Sql</span></span>
* <span data-ttu-id="67dc6-838">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="67dc6-838">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="67dc6-839">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="67dc6-839">Az.Storage</span></span>
* <span data-ttu-id="67dc6-840">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="67dc6-840">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="67dc6-841">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="67dc6-841">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="67dc6-842">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="67dc6-842">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="67dc6-843">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="67dc6-843">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="67dc6-844">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="67dc6-844">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="67dc6-845">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="67dc6-845">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="67dc6-846">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="67dc6-846">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="67dc6-847">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="67dc6-847">Az.Websites</span></span>
* <span data-ttu-id="67dc6-848">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="67dc6-848">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="67dc6-849">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="67dc6-849">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="67dc6-850">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="67dc6-850">Az.Accounts</span></span>
* <span data-ttu-id="67dc6-851">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="67dc6-851">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="67dc6-852">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-852">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="67dc6-853">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="67dc6-853">Az.Automation</span></span>
* <span data-ttu-id="67dc6-854">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-854">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="67dc6-855">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="67dc6-855">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="67dc6-856">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="67dc6-856">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="67dc6-857">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="67dc6-857">Az.Cdn</span></span>
* <span data-ttu-id="67dc6-858">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="67dc6-858">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-859">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-859">Az.Compute</span></span>
* <span data-ttu-id="67dc6-860">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-860">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="67dc6-861">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="67dc6-861">Az.DataFactory</span></span>
* <span data-ttu-id="67dc6-862">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="67dc6-862">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="67dc6-863">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="67dc6-863">Az.LogicApp</span></span>
* <span data-ttu-id="67dc6-864">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="67dc6-864">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="67dc6-865">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-865">Az.Network</span></span>
* <span data-ttu-id="67dc6-866">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-866">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="67dc6-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="67dc6-868">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="67dc6-868">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="67dc6-869">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="67dc6-869">SDK Update</span></span>
* <span data-ttu-id="67dc6-870">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="67dc6-870">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="67dc6-871">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-871">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="67dc6-872">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-872">Az.Resources</span></span>
* <span data-ttu-id="67dc6-873">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-873">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="67dc6-874">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="67dc6-874">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="67dc6-875">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="67dc6-875">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="67dc6-876">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="67dc6-876">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="67dc6-877">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="67dc6-877">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="67dc6-878">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="67dc6-878">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="67dc6-879">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-879">Az.Sql</span></span>
* <span data-ttu-id="67dc6-880">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="67dc6-880">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="67dc6-881">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="67dc6-881">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="67dc6-882">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="67dc6-882">Az.Storage</span></span>
* <span data-ttu-id="67dc6-883">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67dc6-883">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="67dc6-884">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="67dc6-884">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="67dc6-885">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-885">Az.AnalysisServices</span></span>
* <span data-ttu-id="67dc6-886">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="67dc6-886">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="67dc6-887">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="67dc6-887">Az.Automation</span></span>
* <span data-ttu-id="67dc6-888">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-888">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="67dc6-889">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-889">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="67dc6-890">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-890">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="67dc6-891">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-891">Az.CognitiveServices</span></span>
* <span data-ttu-id="67dc6-892">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="67dc6-892">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-893">Az.Compute</span></span>
* <span data-ttu-id="67dc6-894">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="67dc6-894">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="67dc6-895">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-895">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="67dc6-896">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-896">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="67dc6-897">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="67dc6-897">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="67dc6-898">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="67dc6-898">Az.DataLakeStore</span></span>
* <span data-ttu-id="67dc6-899">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="67dc6-899">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="67dc6-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="67dc6-900">Az.EventHub</span></span>
* <span data-ttu-id="67dc6-901">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="67dc6-901">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="67dc6-902">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="67dc6-902">Az.KeyVault</span></span>
* <span data-ttu-id="67dc6-903">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-903">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="67dc6-904">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="67dc6-904">Az.LogicApp</span></span>
* <span data-ttu-id="67dc6-905">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="67dc6-905">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="67dc6-906">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="67dc6-906">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="67dc6-907">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="67dc6-907">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="67dc6-908">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="67dc6-908">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="67dc6-909">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="67dc6-909">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="67dc6-910">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="67dc6-910">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="67dc6-911">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="67dc6-911">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="67dc6-912">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="67dc6-912">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="67dc6-913">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="67dc6-913">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="67dc6-914">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="67dc6-914">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="67dc6-915">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="67dc6-915">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="67dc6-916">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="67dc6-916">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="67dc6-917">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="67dc6-917">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="67dc6-918">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="67dc6-918">Az.Monitor</span></span>
* <span data-ttu-id="67dc6-919">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-919">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="67dc6-920">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-920">Az.Network</span></span>
* <span data-ttu-id="67dc6-921">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="67dc6-921">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="67dc6-922">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="67dc6-922">Az.OperationalInsights</span></span>
* <span data-ttu-id="67dc6-923">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="67dc6-923">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="67dc6-924">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="67dc6-924">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="67dc6-925">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="67dc6-925">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="67dc6-926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-926">Az.Resources</span></span>
* <span data-ttu-id="67dc6-927">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="67dc6-927">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="67dc6-928">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="67dc6-928">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="67dc6-929">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="67dc6-929">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="67dc6-930">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="67dc6-930">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="67dc6-931">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-931">Az.Sql</span></span>
* <span data-ttu-id="67dc6-932">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-932">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="67dc6-933">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="67dc6-933">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="67dc6-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="67dc6-934">Az.Websites</span></span>
* <span data-ttu-id="67dc6-935">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-935">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="67dc6-936">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="67dc6-936">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="67dc6-937">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="67dc6-937">Az.Accounts</span></span>
* <span data-ttu-id="67dc6-938">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="67dc6-938">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="67dc6-939">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-939">Az.AnalysisServices</span></span>
<span data-ttu-id="67dc6-940">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="67dc6-940">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-941">Az.Compute</span></span>
* <span data-ttu-id="67dc6-942">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="67dc6-942">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="67dc6-943">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="67dc6-943">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="67dc6-944">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="67dc6-944">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="67dc6-945">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-945">Az.RecoveryServices</span></span>
<span data-ttu-id="67dc6-946">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="67dc6-946">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="67dc6-947">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-947">Az.Resources</span></span>
* <span data-ttu-id="67dc6-948">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="67dc6-948">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="67dc6-949">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="67dc6-949">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="67dc6-950">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="67dc6-950">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="67dc6-951">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="67dc6-951">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="67dc6-952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-952">Az.Sql</span></span>
* <span data-ttu-id="67dc6-953">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-953">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="67dc6-954">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="67dc6-954">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="67dc6-955">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="67dc6-955">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="67dc6-956">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="67dc6-956">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="67dc6-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="67dc6-957">Az.Accounts</span></span>
* <span data-ttu-id="67dc6-958">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="67dc6-958">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="67dc6-959">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-959">Az.AnalysisServices</span></span>
* <span data-ttu-id="67dc6-960">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="67dc6-960">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="67dc6-961">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-961">Az.RecoveryServices</span></span>
* <span data-ttu-id="67dc6-962">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="67dc6-962">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="67dc6-963">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="67dc6-963">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="67dc6-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="67dc6-964">Az.Accounts</span></span>
* <span data-ttu-id="67dc6-965">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-965">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="67dc6-966">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="67dc6-966">Update incorrect online help URLs</span></span>
* <span data-ttu-id="67dc6-967">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="67dc6-967">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="67dc6-968">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="67dc6-968">Az.Aks</span></span>
* <span data-ttu-id="67dc6-969">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="67dc6-969">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="67dc6-970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="67dc6-970">Az.Automation</span></span>
* <span data-ttu-id="67dc6-971">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="67dc6-971">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="67dc6-972">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="67dc6-972">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="67dc6-973">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="67dc6-973">Az.Cdn</span></span>
* <span data-ttu-id="67dc6-974">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="67dc6-974">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-975">Az.Compute</span></span>
* <span data-ttu-id="67dc6-976">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="67dc6-976">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="67dc6-977">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="67dc6-977">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="67dc6-978">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="67dc6-978">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="67dc6-979">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="67dc6-979">Az.ContainerRegistry</span></span>
* <span data-ttu-id="67dc6-980">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="67dc6-980">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="67dc6-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="67dc6-981">Az.DataFactory</span></span>
* <span data-ttu-id="67dc6-982">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="67dc6-982">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="67dc6-983">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="67dc6-983">Az.DataLakeStore</span></span>
* <span data-ttu-id="67dc6-984">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="67dc6-984">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="67dc6-985">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="67dc6-985">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="67dc6-986">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="67dc6-986">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="67dc6-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="67dc6-987">Az.IotHub</span></span>
* <span data-ttu-id="67dc6-988">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="67dc6-988">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="67dc6-989">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="67dc6-989">Az.KeyVault</span></span>
* <span data-ttu-id="67dc6-990">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="67dc6-990">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="67dc6-991">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-991">Az.Network</span></span>
* <span data-ttu-id="67dc6-992">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="67dc6-992">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="67dc6-993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-993">Az.Resources</span></span>
* <span data-ttu-id="67dc6-994">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="67dc6-994">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="67dc6-995">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="67dc6-995">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="67dc6-996">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="67dc6-996">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="67dc6-997">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="67dc6-997">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="67dc6-998">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="67dc6-998">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="67dc6-999">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="67dc6-999">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="67dc6-1000">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="67dc6-1000">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="67dc6-1001">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="67dc6-1001">Az.ServiceFabric</span></span>
* <span data-ttu-id="67dc6-1002">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1002">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="67dc6-1003">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1003">Fix some error messages.</span></span>
* <span data-ttu-id="67dc6-1004">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1004">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="67dc6-1005">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1005">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="67dc6-1006">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="67dc6-1006">Az.SignalR</span></span>
* <span data-ttu-id="67dc6-1007">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1007">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="67dc6-1008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-1008">Az.Sql</span></span>
* <span data-ttu-id="67dc6-1009">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1009">Update incorrect online help URLs</span></span>
* <span data-ttu-id="67dc6-1010">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1010">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="67dc6-1011">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1011">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="67dc6-1012">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="67dc6-1012">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="67dc6-1013">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="67dc6-1013">Az.Storage</span></span>
* <span data-ttu-id="67dc6-1014">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1014">Update incorrect online help URLs</span></span>
* <span data-ttu-id="67dc6-1015">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1015">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="67dc6-1016">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="67dc6-1016">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="67dc6-1017">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="67dc6-1017">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="67dc6-1018">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="67dc6-1018">Az.TrafficManager</span></span>
* <span data-ttu-id="67dc6-1019">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1019">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="67dc6-1020">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="67dc6-1020">Az.Websites</span></span>
* <span data-ttu-id="67dc6-1021">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1021">Update incorrect online help URLs</span></span>
* <span data-ttu-id="67dc6-1022">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1022">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="67dc6-1023">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1023">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="67dc6-1024">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="67dc6-1024">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="67dc6-1025">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="67dc6-1025">Az.Accounts</span></span>
* <span data-ttu-id="67dc6-1026">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-1026">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-1027">Az.Compute</span></span>
* <span data-ttu-id="67dc6-1028">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="67dc6-1028">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="67dc6-1029">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="67dc6-1029">Updated the description of ID in help files</span></span>
* <span data-ttu-id="67dc6-1030">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="67dc6-1030">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="67dc6-1031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="67dc6-1031">Az.DataLakeStore</span></span>
* <span data-ttu-id="67dc6-1032">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1032">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="67dc6-1033">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="67dc6-1033">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="67dc6-1034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="67dc6-1034">Az.EventGrid</span></span>
* <span data-ttu-id="67dc6-1035">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1035">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="67dc6-1036">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="67dc6-1036">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="67dc6-1037">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="67dc6-1037">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="67dc6-1038">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="67dc6-1038">Event Time-To-Live,</span></span>
        - <span data-ttu-id="67dc6-1039">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="67dc6-1039">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="67dc6-1040">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1040">Dead letter endpoint.</span></span>
    - <span data-ttu-id="67dc6-1041">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="67dc6-1041">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="67dc6-1042">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="67dc6-1042">Event Time-To-Live,</span></span>
        - <span data-ttu-id="67dc6-1043">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="67dc6-1043">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="67dc6-1044">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1044">Dead letter endpoint.</span></span>
* <span data-ttu-id="67dc6-1045">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1045">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="67dc6-1046">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1046">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="67dc6-1047">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="67dc6-1047">Az.IotHub</span></span>
* <span data-ttu-id="67dc6-1048">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="67dc6-1048">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="67dc6-1049">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="67dc6-1049">Az.LogicApp</span></span>
* <span data-ttu-id="67dc6-1050">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="67dc6-1050">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="67dc6-1051">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-1051">Az.Resources</span></span>
* <span data-ttu-id="67dc6-1052">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="67dc6-1052">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="67dc6-1053">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="67dc6-1053">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="67dc6-1054">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="67dc6-1054">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="67dc6-1055">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="67dc6-1055">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="67dc6-1056">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-1056">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="67dc6-1057">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="67dc6-1057">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="67dc6-1058">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="67dc6-1058">Az.SignalR</span></span>
* <span data-ttu-id="67dc6-1059">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="67dc6-1059">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="67dc6-1060">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-1060">Az.Sql</span></span>
* <span data-ttu-id="67dc6-1061">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1061">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="67dc6-1062">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="67dc6-1062">Az.Storage</span></span>
* <span data-ttu-id="67dc6-1063">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="67dc6-1063">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="67dc6-1064">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="67dc6-1064">New-AzStorageContext</span></span>
* <span data-ttu-id="67dc6-1065">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="67dc6-1065">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="67dc6-1066">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="67dc6-1066">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="67dc6-1067">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="67dc6-1067">Az.Websites</span></span>
* <span data-ttu-id="67dc6-1068">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="67dc6-1068">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="67dc6-1069">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="67dc6-1069">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="67dc6-1070">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="67dc6-1070">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="67dc6-1071">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="67dc6-1071">General</span></span>

- <span data-ttu-id="67dc6-1072">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="67dc6-1072">General Availability of Az Module</span></span>
- <span data-ttu-id="67dc6-1073">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-1073">Online help for each module</span></span>
- <span data-ttu-id="67dc6-1074">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1074">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="67dc6-1075">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1075">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="67dc6-1076">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="67dc6-1076">Az.Accounts</span></span>
- <span data-ttu-id="67dc6-1077">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="67dc6-1077">Changed from Az.Profile</span></span>
- <span data-ttu-id="67dc6-1078">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-1078">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="67dc6-1079">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="67dc6-1079">Az.ApiManagement</span></span>
- <span data-ttu-id="67dc6-1080">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="67dc6-1080">Fixes for #7002</span></span>
- <span data-ttu-id="67dc6-1081">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="67dc6-1082">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="67dc6-1082">Az.Batch</span></span>
- <span data-ttu-id="67dc6-1083">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1083">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="67dc6-1084">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1084">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="67dc6-1085">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="67dc6-1086">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="67dc6-1086">Az.Billing</span></span>
- <span data-ttu-id="67dc6-1087">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1087">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="67dc6-1088">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-1088">Az.CognitivServices</span></span>
- <span data-ttu-id="67dc6-1089">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1089">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="67dc6-1090">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1090">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="67dc6-1091">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="67dc6-1091">Az.ContainerInstance</span></span>
- <span data-ttu-id="67dc6-1092">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="67dc6-1092">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="67dc6-1093">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="67dc6-1093">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="67dc6-1094">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1094">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="67dc6-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="67dc6-1095">Az.DataLakeStore</span></span>
- <span data-ttu-id="67dc6-1096">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1096">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="67dc6-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="67dc6-1097">Az.Monitor</span></span>
- <span data-ttu-id="67dc6-1098">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1098">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="67dc6-1099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="67dc6-1099">Az.KeyVault</span></span>
- <span data-ttu-id="67dc6-1100">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1100">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="67dc6-1101">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="67dc6-1101">Az.MachineLearning</span></span>
- <span data-ttu-id="67dc6-1102">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="67dc6-1102">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="67dc6-1103">Az.Media</span><span class="sxs-lookup"><span data-stu-id="67dc6-1103">Az.Media</span></span>
- <span data-ttu-id="67dc6-1104">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="67dc6-1104">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="67dc6-1105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-1105">Az.Network</span></span>
<span data-ttu-id="67dc6-1106">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1106">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="67dc6-1107">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="67dc6-1107">New cmdlets added:</span></span>
        - <span data-ttu-id="67dc6-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="67dc6-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="67dc6-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="67dc6-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="67dc6-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="67dc6-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="67dc6-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="67dc6-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="67dc6-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="67dc6-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="67dc6-1113">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="67dc6-1113">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="67dc6-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="67dc6-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="67dc6-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="67dc6-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="67dc6-1116">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="67dc6-1116">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="67dc6-1117">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67dc6-1117">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="67dc6-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="67dc6-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="67dc6-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="67dc6-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="67dc6-1120">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="67dc6-1120">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="67dc6-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="67dc6-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="67dc6-1122">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1122">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="67dc6-1123">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="67dc6-1123">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="67dc6-1124">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="67dc6-1124">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="67dc6-1125">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="67dc6-1125">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="67dc6-1126">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="67dc6-1126">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="67dc6-1127">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="67dc6-1127">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="67dc6-1128">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1128">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="67dc6-1129">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="67dc6-1129">Az.OperationalInsights</span></span>
- <span data-ttu-id="67dc6-1130">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1130">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="67dc6-1131">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="67dc6-1131">Az.Profile</span></span>
- <span data-ttu-id="67dc6-1132">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="67dc6-1132">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="67dc6-1133">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-1133">Az.RecoveryServices</span></span>
- <span data-ttu-id="67dc6-1134">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1134">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="67dc6-1135">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-1135">Az.Resources</span></span>
- <span data-ttu-id="67dc6-1136">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1136">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="67dc6-1137">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="67dc6-1137">Az.ServiceFabric</span></span>
- <span data-ttu-id="67dc6-1138">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="67dc6-1138">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="67dc6-1139">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1139">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="67dc6-1140">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="67dc6-1140">Az.SIgnalR</span></span>
- <span data-ttu-id="67dc6-1141">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="67dc6-1141">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="67dc6-1142">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-1142">Az.Sql</span></span>
- <span data-ttu-id="67dc6-1143">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-1143">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="67dc6-1144">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="67dc6-1144">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="67dc6-1145">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1145">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="67dc6-1146">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="67dc6-1146">Az.Storage</span></span>
- <span data-ttu-id="67dc6-1147">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1147">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="67dc6-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="67dc6-1148">Az.Websites</span></span>
- <span data-ttu-id="67dc6-1149">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1149">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="67dc6-1150">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="67dc6-1150">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="67dc6-1151">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="67dc6-1151">General</span></span>

* <span data-ttu-id="67dc6-1152">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-1152">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="67dc6-1153">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-1153">Az.Compute</span></span>

* <span data-ttu-id="67dc6-1154">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1154">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="67dc6-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="67dc6-1155">Az.DataLakeStore</span></span>

* <span data-ttu-id="67dc6-1156">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="67dc6-1156">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="67dc6-1157">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="67dc6-1157">Az.FrontDoor</span></span>

* <span data-ttu-id="67dc6-1158">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-1158">Fixed some broken links</span></span>
    - <span data-ttu-id="67dc6-1159">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1159">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="67dc6-1160">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1160">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="67dc6-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-1161">Az.RecoveryServices</span></span>

* <span data-ttu-id="67dc6-1162">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1162">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="67dc6-1163">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1163">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="67dc6-1164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-1164">Az.Resources</span></span>

* <span data-ttu-id="67dc6-1165">https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-1165">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="67dc6-1166">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1166">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="67dc6-1167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-1167">Az.Sql</span></span>

* <span data-ttu-id="67dc6-1168">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-1168">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="67dc6-1169">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="67dc6-1169">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="67dc6-1170">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1170">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="67dc6-1171">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="67dc6-1171">Az.Storage</span></span>

* <span data-ttu-id="67dc6-1172">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-1172">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="67dc6-1173">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1173">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="67dc6-1174">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="67dc6-1174">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="67dc6-1175">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="67dc6-1175">Support Static Website configuration</span></span>
    - <span data-ttu-id="67dc6-1176">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="67dc6-1176">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="67dc6-1177">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="67dc6-1177">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="67dc6-1178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="67dc6-1178">Az.Websites</span></span>

* <span data-ttu-id="67dc6-1179">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="67dc6-1179">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="67dc6-1180">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1180">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="67dc6-1181">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1181">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="67dc6-1182">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="67dc6-1182">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="67dc6-1183">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="67dc6-1183">Az.ApiManagement</span></span>
* <span data-ttu-id="67dc6-1184">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1184">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="67dc6-1185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="67dc6-1185">Az.Automation</span></span>
* <span data-ttu-id="67dc6-1186">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1186">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="67dc6-1187">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1187">Added Update Management cmdlets</span></span>
* <span data-ttu-id="67dc6-1188">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1188">Added Source Control cmdlets</span></span>
* <span data-ttu-id="67dc6-1189">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1189">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="67dc6-1190">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1190">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="67dc6-1191">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-1191">Az.Compute</span></span>
* <span data-ttu-id="67dc6-1192">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1192">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="67dc6-1193">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1193">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="67dc6-1194">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="67dc6-1194">Az.ContainerInstance</span></span>
* <span data-ttu-id="67dc6-1195">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1195">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="67dc6-1196">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="67dc6-1196">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="67dc6-1197">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1197">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="67dc6-1198">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-1198">Az.Network</span></span>
* <span data-ttu-id="67dc6-1199">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1199">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="67dc6-1200">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1200">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="67dc6-1201">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1201">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="67dc6-1202">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1202">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="67dc6-1203">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="67dc6-1203">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="67dc6-1204">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1204">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="67dc6-1205">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1205">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="67dc6-1206">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="67dc6-1206">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="67dc6-1207">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1207">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="67dc6-1208">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1208">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="67dc6-1209">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="67dc6-1209">Az.Relay</span></span>
* <span data-ttu-id="67dc6-1210">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1210">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="67dc6-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-1211">Az.Resources</span></span>
* <span data-ttu-id="67dc6-1212">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1212">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="67dc6-1213">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1213">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="67dc6-1214">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1214">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="67dc6-1215">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="67dc6-1215">Az.ServiceFabric</span></span>
* <span data-ttu-id="67dc6-1216">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1216">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="67dc6-1217">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-1217">Az.Sql</span></span>
* <span data-ttu-id="67dc6-1218">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1218">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="67dc6-1219">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="67dc6-1219">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="67dc6-1220">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="67dc6-1220">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="67dc6-1221">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="67dc6-1221">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="67dc6-1222">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="67dc6-1222">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="67dc6-1223">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="67dc6-1223">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="67dc6-1224">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="67dc6-1224">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="67dc6-1225">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="67dc6-1225">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="67dc6-1226">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="67dc6-1226">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="67dc6-1227">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1227">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="67dc6-1228">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1228">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="67dc6-1229">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1229">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="67dc6-1230">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1230">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="67dc6-1231">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1231">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="67dc6-1232">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1232">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="67dc6-1233">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1233">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="67dc6-1234">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1234">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="67dc6-1235">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="67dc6-1235">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="67dc6-1236">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="67dc6-1236">General</span></span>
* <span data-ttu-id="67dc6-1237">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1237">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="67dc6-1238">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="67dc6-1238">Az.Profile</span></span>
* <span data-ttu-id="67dc6-1239">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1239">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="67dc6-1240">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="67dc6-1240">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="67dc6-1241">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="67dc6-1241">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="67dc6-1242">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="67dc6-1242">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="67dc6-1243">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="67dc6-1243">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="67dc6-1244">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="67dc6-1244">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="67dc6-1245">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="67dc6-1245">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="67dc6-1246">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-1246">Az.CognitiveServices</span></span>
* <span data-ttu-id="67dc6-1247">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1247">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-1248">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-1248">Az.Compute</span></span>
* <span data-ttu-id="67dc6-1249">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="67dc6-1249">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="67dc6-1250">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="67dc6-1250">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="67dc6-1251">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1251">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="67dc6-1252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="67dc6-1252">Az.DataLakeStore</span></span>
* <span data-ttu-id="67dc6-1253">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1253">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="67dc6-1254">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1254">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="67dc6-1255">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="67dc6-1255">Az.Insights</span></span>
* <span data-ttu-id="67dc6-1256">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="67dc6-1256">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="67dc6-1257">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1257">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="67dc6-1258">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="67dc6-1258">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="67dc6-1259">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="67dc6-1259">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="67dc6-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-1260">Az.Network</span></span>
* <span data-ttu-id="67dc6-1261">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="67dc6-1261">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="67dc6-1262">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="67dc6-1262">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="67dc6-1263">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="67dc6-1263">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="67dc6-1264">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="67dc6-1264">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="67dc6-1265">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="67dc6-1265">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="67dc6-1266">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="67dc6-1266">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="67dc6-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="67dc6-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="67dc6-1268">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="67dc6-1268">Az.PolicyInsights</span></span>
* <span data-ttu-id="67dc6-1269">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-1269">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="67dc6-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-1270">Az.Resources</span></span>
* <span data-ttu-id="67dc6-1271">https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="67dc6-1271">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="67dc6-1272">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="67dc6-1272">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="67dc6-1273">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="67dc6-1273">Az.ServiceBus</span></span>
* <span data-ttu-id="67dc6-1274">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1274">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="67dc6-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="67dc6-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="67dc6-1276">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1276">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="67dc6-1277">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="67dc6-1277">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="67dc6-1278">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1278">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="67dc6-1279">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1279">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="67dc6-1280">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1280">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="67dc6-1281">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="67dc6-1281">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="67dc6-1282">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="67dc6-1282">Az.Profile</span></span>
* <span data-ttu-id="67dc6-1283">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1283">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="67dc6-1284">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1284">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-1285">Az.Compute</span></span>
* <span data-ttu-id="67dc6-1286">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1286">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="67dc6-1287">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1287">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="67dc6-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="67dc6-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="67dc6-1289">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="67dc6-1289">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="67dc6-1290">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1290">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="67dc6-1291">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1291">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="67dc6-1292">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1292">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="67dc6-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="67dc6-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-1294">Az.Network</span></span>
* <span data-ttu-id="67dc6-1295">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1295">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="67dc6-1296">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1296">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="67dc6-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-1297">Az.Resources</span></span>
* <span data-ttu-id="67dc6-1298">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="67dc6-1298">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="67dc6-1299">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1299">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="67dc6-1300">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="67dc6-1300">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="67dc6-1301">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="67dc6-1301">Azure.Storage</span></span>
* <span data-ttu-id="67dc6-1302">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="67dc6-1302">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="67dc6-1303">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="67dc6-1303">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="67dc6-1304">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="67dc6-1304">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="67dc6-1305">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1305">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="67dc6-1306">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="67dc6-1306">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="67dc6-1307">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="67dc6-1307">Az.CognitiveServices</span></span>
* <span data-ttu-id="67dc6-1308">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1308">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="67dc6-1309">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="67dc6-1309">Az.Compute</span></span>
* <span data-ttu-id="67dc6-1310">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1310">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="67dc6-1311">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1311">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="67dc6-1312">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="67dc6-1312">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="67dc6-1313">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="67dc6-1313">Az.DataFactoryV2</span></span>
* <span data-ttu-id="67dc6-1314">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1314">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="67dc6-1315">Az.Network</span><span class="sxs-lookup"><span data-stu-id="67dc6-1315">Az.Network</span></span>
* <span data-ttu-id="67dc6-1316">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1316">Added NetworkProfile functionality.</span></span> <span data-ttu-id="67dc6-1317">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="67dc6-1317">new cmdlets added</span></span>
    - <span data-ttu-id="67dc6-1318">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="67dc6-1318">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="67dc6-1319">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="67dc6-1319">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="67dc6-1320">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="67dc6-1320">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="67dc6-1321">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="67dc6-1321">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="67dc6-1322">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="67dc6-1322">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="67dc6-1323">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="67dc6-1323">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="67dc6-1324">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="67dc6-1324">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="67dc6-1325">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="67dc6-1325">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="67dc6-1326">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="67dc6-1326">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="67dc6-1327">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="67dc6-1327">Az.RedisCache</span></span>
* <span data-ttu-id="67dc6-1328">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="67dc6-1328">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="67dc6-1329">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-1329">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="67dc6-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="67dc6-1330">Az.Resources</span></span>
* <span data-ttu-id="67dc6-1331">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="67dc6-1331">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="67dc6-1332">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="67dc6-1332">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="67dc6-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="67dc6-1333">Az.Sql</span></span>
* <span data-ttu-id="67dc6-1334">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="67dc6-1334">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="67dc6-1335">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="67dc6-1335">Az.Websites</span></span>
* <span data-ttu-id="67dc6-1336">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="67dc6-1336">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="67dc6-1337">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="67dc6-1337">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="67dc6-1338">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="67dc6-1338">0.2.0 - September 2018</span></span>
 <span data-ttu-id="67dc6-1339">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="67dc6-1339">Initial Release</span></span>