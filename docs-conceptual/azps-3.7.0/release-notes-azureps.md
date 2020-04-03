---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 9e60e76206127922902804112e0b3f837cf03d76
ms.sourcegitcommit: eeb720e053939a68873ae3973bc81d5826358c9f
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/31/2020
ms.locfileid: "80440503"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="d1720-103">Az Azure PowerShell kibocsátási megjegyzései</span><span class="sxs-lookup"><span data-stu-id="d1720-103">Azure PowerShell release notes</span></span>
## <a name="370---march-2020"></a><span data-ttu-id="d1720-104">3.7.0 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="d1720-104">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d1720-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-105">Az.Accounts</span></span>
* <span data-ttu-id="d1720-106">Ki lett javítva az a hiba, hogy a Get-AzTenant/Get-AzDefault/Set-AzDefault parancs NullReferenceException hibát ad vissza kijelentkezett állapotban [#10292]</span><span class="sxs-lookup"><span data-stu-id="d1720-106">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-107">Az.Compute</span></span>
* <span data-ttu-id="d1720-108">A következő paraméterek lettek hozzáadva a New-AzDiskConfig parancsmaghoz:</span><span class="sxs-lookup"><span data-stu-id="d1720-108">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="d1720-109">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="d1720-109">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="d1720-110">Engedélyezve lett a New-AzGalleryImageVersion parancsmag célparaméterének titkosítási tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="d1720-110">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="d1720-111">Ki lett javítva a tempDisk hibája a Set-AzVmss -Reimage és az Invoke-AzVMReimage parancsmag esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-111">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="d1720-112">[#11354]</span><span class="sxs-lookup"><span data-stu-id="d1720-112">[#11354]</span></span>
* <span data-ttu-id="d1720-113">Az alábbi parancsmagok mostantól támogatottak az új SAP-bővítmény esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-113">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="d1720-114">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d1720-114">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="d1720-115">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d1720-115">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="d1720-116">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d1720-116">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="d1720-117">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d1720-117">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="d1720-118">Ki lettek javítva a súgódokumentáció példáinak hibái</span><span class="sxs-lookup"><span data-stu-id="d1720-118">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="d1720-119">Táblázatos formátumban jelenítette meg a sztring pontos értékét a PowerState virtuális gép esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-119">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="d1720-120">New-AzVmssConfig: ki lett javítva az AutomaticRepairs tulajdonság szerializálása a SinglePlacementGroup letiltott állapota esetén.</span><span class="sxs-lookup"><span data-stu-id="d1720-120">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="d1720-121">[#11257]</span><span class="sxs-lookup"><span data-stu-id="d1720-121">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d1720-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1720-122">Az.DataFactory</span></span>
* <span data-ttu-id="d1720-123">Az ADF .Net SDK a 4.8.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d1720-123">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="d1720-124">Opcionális paraméterek lettek hozzáadva az Invoke-AzDataFactoryV2Pipeline parancshoz az újrafuttatás támogatásához</span><span class="sxs-lookup"><span data-stu-id="d1720-124">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d1720-125">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1720-125">Az.DataLakeStore</span></span>
* <span data-ttu-id="d1720-126">Hozzá lett adva a kompatibilitástörő változás leírása az Export-AzDataLakeStoreItem és az Import-AzDataLakeStoreItem parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-126">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="d1720-127">A bájtkódolási lehetőség hozzá lett adva a New-AzDataLakeStoreItem, az Add-AzDAtaLakeStoreItemContent és a Get-AzDAtaLakeStoreItemContent parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-127">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d1720-128">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d1720-128">Az.HDInsight</span></span>
* <span data-ttu-id="d1720-129">Fürt létrehozásakor a minimálisan támogatott TLS-verzió megadása támogatott.</span><span class="sxs-lookup"><span data-stu-id="d1720-129">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d1720-130">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d1720-130">Az.IotHub</span></span>
* <span data-ttu-id="d1720-131">Hozzá lett adva az elosztott beállítások eszközönkénti felügyeletének támogatása.</span><span class="sxs-lookup"><span data-stu-id="d1720-131">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="d1720-132">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="d1720-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="d1720-133">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="d1720-133">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="d1720-134">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="d1720-134">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d1720-135">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d1720-135">Az.KeyVault</span></span>
* <span data-ttu-id="d1720-136">Kompatibilitástörő változást okozó attribútumok lettek hozzáadva a New-AzKeyVault parancshoz</span><span class="sxs-lookup"><span data-stu-id="d1720-136">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d1720-137">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d1720-137">Az.Monitor</span></span>
* <span data-ttu-id="d1720-138">Frissült a New-AzScheduledQueryRuleLogMetricTrigger dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d1720-138">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-139">Az.Network</span></span>
* <span data-ttu-id="d1720-140">Frissültek a parancsmagok a több-bérlős VirtualHubVnetConnections engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-140">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="d1720-141">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-141">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="d1720-142">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-142">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="d1720-143">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d1720-143">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="d1720-144">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d1720-144">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="d1720-145">Az SQL Management SDK-függőség el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="d1720-145">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d1720-146">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d1720-146">Az.PolicyInsights</span></span>
* <span data-ttu-id="d1720-147">Továbbfejlesztett hibaüzenetek</span><span class="sxs-lookup"><span data-stu-id="d1720-147">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-148">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-149">Hozzá lett adva az Azure Site Recovery-támogatás az Azure Diskkel titkosított virtuális gépek védelmének újbóli beállítása és frissített virtuálisgép-tulajdonságai esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-149">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="d1720-150">Hozzá lett adva az Azure Site Recovery VmwareToAzure tulajdonságainak vészhelyreállítási monitorozása</span><span class="sxs-lookup"><span data-stu-id="d1720-150">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="d1720-151">Hozzá lett adva az Azure Backup-támogatás a sikertelen elemekre vonatkozó szabályzatfrissítés újbóli végrehajtása esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-151">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="d1720-152">Hozzá lett adva az Azure Backup-támogatás a lemezkizárási beállításokhoz a biztonsági mentés és a visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="d1720-152">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="d1720-153">Hozzá lett adva az Azure Backup-támogatás több fájl/mappa visszaállításához az AzureFileShare-ben</span><span class="sxs-lookup"><span data-stu-id="d1720-153">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="d1720-154">Hozzá lett adva az Azure Backup-támogatás a felhasználó által megadott erőforráscsoport támogatásához az IaasVM-szabályzat frissítésekor</span><span class="sxs-lookup"><span data-stu-id="d1720-154">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-155">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-155">Az.Resources</span></span>
* <span data-ttu-id="d1720-156">Ki lett javítva a Get-AzResource-ResourceGroupName-Name-ExpandProperties-ResourceType parancs, hogy ezentúl az erőforrások aktuális API-verzióját használja az alapértelmezett verzió helyett [#11267]</span><span class="sxs-lookup"><span data-stu-id="d1720-156">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="d1720-157">Hozzá lett adva a CorrelationId-naplózás a hibaforgatókönyvek esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-157">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="d1720-158">A Get-AzResourceLock dokumentációjában kisebb módosítás történt.</span><span class="sxs-lookup"><span data-stu-id="d1720-158">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="d1720-159">Példa hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="d1720-159">Added example.</span></span>
* <span data-ttu-id="d1720-160">A szimpla idézőjel fel lett oldva a Get-AzADUser paraméterértékében [#11317]</span><span class="sxs-lookup"><span data-stu-id="d1720-160">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="d1720-161">Új parancsmagok lettek hozzáadva az üzembehelyezési szkriptekhez (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript)</span><span class="sxs-lookup"><span data-stu-id="d1720-161">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-162">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-162">Az.Sql</span></span>
* <span data-ttu-id="d1720-163">Olvasható másodlagos paraméter lett hozzáadva az Invoke-AzSqlDatabaseFailover parancshoz</span><span class="sxs-lookup"><span data-stu-id="d1720-163">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="d1720-164">A Disable-AzSqlServerActiveDirectoryOnlyAuthentication parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d1720-164">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="d1720-165">Az érzékenységi besorolás mentése megtörténik az adatbázis oszlopainak osztályozásakor.</span><span class="sxs-lookup"><span data-stu-id="d1720-165">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="d1720-166">Az.Support</span><span class="sxs-lookup"><span data-stu-id="d1720-166">Az.Support</span></span>
* <span data-ttu-id="d1720-167">Az Az.Support modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="d1720-167">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-168">Az.Websites</span></span>
* <span data-ttu-id="d1720-169">Mostantól támogatott a webalkalmazások forgalom-útválasztási szabályainak az alábbi új parancsmagokkal történő használata</span><span class="sxs-lookup"><span data-stu-id="d1720-169">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="d1720-170">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d1720-170">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="d1720-171">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d1720-171">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="d1720-172">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d1720-172">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="d1720-173">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d1720-173">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="d1720-174">3.6.1 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="d1720-174">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d1720-175">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-175">Az.Accounts</span></span>
* <span data-ttu-id="d1720-176">Azure PowerShell felmérési oldal megnyitása itt: Send-Feedback [#11020]</span><span class="sxs-lookup"><span data-stu-id="d1720-176">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="d1720-177">Azure PowerShell-felmérés URL-címének megjelenítése itt: Resolve-Error [#11021]</span><span class="sxs-lookup"><span data-stu-id="d1720-177">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="d1720-178">Az-verzió hozzáadva az UserAgenthez</span><span class="sxs-lookup"><span data-stu-id="d1720-178">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d1720-179">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d1720-179">Az.ApiManagement</span></span>
* <span data-ttu-id="d1720-180">Mostantól támogatott az egyéni tartomány lekérése és konfigurálása a DeveloperPortal végpontján [#11007]</span><span class="sxs-lookup"><span data-stu-id="d1720-180">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="d1720-181">Export-AzApiManagementAPi – Mostantól támogatott az Api-definíció Json formátumban való letöltése [#9987]</span><span class="sxs-lookup"><span data-stu-id="d1720-181">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="d1720-182">Import-AzApiManagementApi – Az OpenAPI 3.0-definíció Json-dokumentumokból való importálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="d1720-182">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="d1720-183">New-AzApiManagementIdentityProvider és Set-AzApiManagementIdentityProvider – A Signin Tenant konfigurálása az AAD B2C-szolgáltató esetében mostantól támogatott. [#9784]</span><span class="sxs-lookup"><span data-stu-id="d1720-183">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d1720-184">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1720-184">Az.DataLakeStore</span></span>
* <span data-ttu-id="d1720-185">A System.Buffershez hivatkozásának explicit hozzáadása a következőkben: csproj és psd1</span><span class="sxs-lookup"><span data-stu-id="d1720-185">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d1720-186">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d1720-186">Az.IotHub</span></span>
* <span data-ttu-id="d1720-187">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="d1720-187">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="d1720-188">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="d1720-188">New Cmdlets are:</span></span>
    - <span data-ttu-id="d1720-189">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d1720-189">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d1720-190">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d1720-190">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d1720-191">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d1720-191">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d1720-192">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d1720-192">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="d1720-193">A cél IoT-eszközökön lévő modulok IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="d1720-193">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="d1720-194">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="d1720-194">New Cmdlets are:</span></span>
    - <span data-ttu-id="d1720-195">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="d1720-195">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="d1720-196">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="d1720-196">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="d1720-197">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="d1720-197">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="d1720-198">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="d1720-198">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="d1720-199">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-199">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="d1720-200">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz modulja kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-200">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="d1720-201">Az IoT-eszközök szülő eszközének lekérése/beállítása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="d1720-201">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="d1720-202">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="d1720-202">New Cmdlets are:</span></span>
    - <span data-ttu-id="d1720-203">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="d1720-203">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="d1720-204">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d1720-204">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="d1720-205">Az eszközök szülő-gyermek kapcsolatainak kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="d1720-205">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d1720-206">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d1720-206">Az.Monitor</span></span>
* <span data-ttu-id="d1720-207">A Get-AzMetricDefinition kimeneti értéke javítva [#9714]</span><span class="sxs-lookup"><span data-stu-id="d1720-207">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-208">Az.Network</span></span>
* <span data-ttu-id="d1720-209">SQL Management SDK frissítve.</span><span class="sxs-lookup"><span data-stu-id="d1720-209">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="d1720-210">Kijavítottuk a PrivateLinkServiceConnectionState osztály eltérő elnevezéssel kapcsolatos hibáját.</span><span class="sxs-lookup"><span data-stu-id="d1720-210">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="d1720-211">Az ActionsRequired mező leképezése a követezőre: ActionRequired</span><span class="sxs-lookup"><span data-stu-id="d1720-211">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="d1720-212">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="d1720-212">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-213">Az.Resources</span></span>
* <span data-ttu-id="d1720-214">A Get-AzRoleAssignment null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="d1720-214">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="d1720-215">A -Force és a -PassThru kapcsoló nem kötelezőként lett megjelölve a Remove-AzADGroup esetében [#10849]</span><span class="sxs-lookup"><span data-stu-id="d1720-215">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="d1720-216">Javítva a hiba, amely miatt a MailNickname nem lett visszaadva Remove-AzADGroup esetében [#11167]</span><span class="sxs-lookup"><span data-stu-id="d1720-216">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="d1720-217">A Remove-AzADGroup folyamatművelet működési hibája kijavítva [#11171]</span><span class="sxs-lookup"><span data-stu-id="d1720-217">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="d1720-218">A GetAzureRoleAssignmentCommand null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="d1720-218">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="d1720-219">Kompatibilitástörő változás hozzáadva a szabályzati parancsmagok soron következő változásaihoz</span><span class="sxs-lookup"><span data-stu-id="d1720-219">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="d1720-220">Frissült a Get-AzResourceGroup az erőforráscsoport-címke kiszolgálóoldali szűrésének elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-220">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="d1720-221">A címkeparancsmagok kiterjesztése a -ResourceID elfogadása érdekében</span><span class="sxs-lookup"><span data-stu-id="d1720-221">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="d1720-222">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1720-222">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="d1720-223">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1720-223">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="d1720-224">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1720-224">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="d1720-225">Új címkeparancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-225">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="d1720-226">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1720-226">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="d1720-227">A ScopedDeployment áthozva az SDK 3.3.0-ból</span><span class="sxs-lookup"><span data-stu-id="d1720-227">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-228">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-228">Az.Sql</span></span>
* <span data-ttu-id="d1720-229">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="d1720-229">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="d1720-230">Támogatás hozzáadva a biztonsági másolatok hosszú távú megőrzési konfigurációjához a felügyelt adatbázisok esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-230">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="d1720-231">LTR-szabályzat lekérése/beállítása felügyelt adatbázison</span><span class="sxs-lookup"><span data-stu-id="d1720-231">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="d1720-232">LTR biztonsági másolat(ok) lekérése felügyelt adatbázis, felügyelt példány vagy hely szerint</span><span class="sxs-lookup"><span data-stu-id="d1720-232">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="d1720-233">LTR biztonsági másolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d1720-233">Remove an LTR backup</span></span>
    - <span data-ttu-id="d1720-234">LTR biztonsági másolat visszaállítása új felügyelt adatbázis létrehozásához</span><span class="sxs-lookup"><span data-stu-id="d1720-234">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="d1720-235">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="d1720-235">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="d1720-236">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlInstance és Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d1720-236">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="d1720-237">Az SQL SDK-verzió felléptetése a következőhöz: AZ.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-237">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-238">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-238">Az.Storage</span></span>
* <span data-ttu-id="d1720-239">Támogatott AllowProtectedAppendWrite a következőben: ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d1720-239">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="d1720-240">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d1720-240">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="d1720-241">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet az AzureStorageTable típusának módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="d1720-241">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="d1720-242">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="d1720-242">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="d1720-243">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="d1720-243">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-244">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-244">Az.Websites</span></span>
* <span data-ttu-id="d1720-245">Címke paraméter hozzáadva a következőkhöz: New-AzAppServicePlan és Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d1720-245">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="d1720-246">A parancsmag végrehajtásának leállítása, ha egy egyéni tartomány webhelyhez történő hozzáadásakor a rendszer kivételt ad vissza</span><span class="sxs-lookup"><span data-stu-id="d1720-246">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="d1720-247">Támogatás hozzáadva az olyan App Services műveletek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag</span><span class="sxs-lookup"><span data-stu-id="d1720-247">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="d1720-248">Hozzáférési korlátozás alkalmazva a különböző erőforráscsoportokban lévő webalkalmazásokra/függvényekre</span><span class="sxs-lookup"><span data-stu-id="d1720-248">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="d1720-249">Az egyéni WebAppSlots-gazdanevek beállítására vonatkozó hiba kijavítva</span><span class="sxs-lookup"><span data-stu-id="d1720-249">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="d1720-250">3.5.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="d1720-250">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d1720-251">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="d1720-251">Highlights since the last major release</span></span>
* <span data-ttu-id="d1720-252">Frissült az ügyféloldali telemetria.</span><span class="sxs-lookup"><span data-stu-id="d1720-252">Updated client side telemetry.</span></span>
* <span data-ttu-id="d1720-253">Az.IotHub: parancsmagok hozzáadva az eszközkezelés támogatásához.</span><span class="sxs-lookup"><span data-stu-id="d1720-253">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="d1720-254">Az.SqlVirtualMachine: parancsmagok hozzáadva a rendelkezésreállási csoport figyelőjéhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-254">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d1720-255">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-255">Az.Accounts</span></span>
* <span data-ttu-id="d1720-256">A SubscriptionId, a TenantId és a végrehajtási idő hozzáadva az ügyféloldali telemetria adataihoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-256">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d1720-257">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d1720-257">Az.Automation</span></span>
* <span data-ttu-id="d1720-258">Ki lett javítva a „New-AzAutomationSoftwareUpdateConfiguration” referenciadokumentációjának 1. példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="d1720-258">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d1720-259">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d1720-259">Az.CognitiveServices</span></span>
* <span data-ttu-id="d1720-260">Az SDK a 7.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d1720-260">Updated SDK to 7.0</span></span>
* <span data-ttu-id="d1720-261">Tovább lett fejlesztve a hibaüzenet, amely akkor jelenik meg, ha a kiszolgáló üres törzset ad vissza válaszként</span><span class="sxs-lookup"><span data-stu-id="d1720-261">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-262">Az.Compute</span></span>
* <span data-ttu-id="d1720-263">A ProximityPlacementGroupId mostantól üres értékkel is rendelkezhet a frissítés során</span><span class="sxs-lookup"><span data-stu-id="d1720-263">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d1720-264">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d1720-264">Az.FrontDoor</span></span>
* <span data-ttu-id="d1720-265">Új parancsmag hozzáadva a WAF-ban használható felügyelt szabálydefiníciók lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-265">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d1720-266">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d1720-266">Az.IotHub</span></span>
* <span data-ttu-id="d1720-267">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="d1720-267">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="d1720-268">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="d1720-268">New Cmdlets are:</span></span>
    - <span data-ttu-id="d1720-269">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d1720-269">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d1720-270">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d1720-270">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d1720-271">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d1720-271">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d1720-272">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="d1720-272">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d1720-273">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d1720-273">Az.KeyVault</span></span>
* <span data-ttu-id="d1720-274">Ki lett javítva az Add-AzKeyVaultKey.md duplikált szövege</span><span class="sxs-lookup"><span data-stu-id="d1720-274">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d1720-275">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d1720-275">Az.Monitor</span></span>
* <span data-ttu-id="d1720-276">Ki lett javítva a Get-AzLog parancsmag leírása.</span><span class="sxs-lookup"><span data-stu-id="d1720-276">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="d1720-277">Egy új, ActionGroupId nevű paraméter lett hozzáadva a „New-AzMetricAlertRuleV2” parancshoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-277">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="d1720-278">A felhasználó a következőket adhatja meg: ActionGroupId(string) vagy ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="d1720-278">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-279">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-279">Az.Network</span></span>
* <span data-ttu-id="d1720-280">Hozzá lett adva egy extra paramétermegjegyzés a „New-AzPrivateLinkService” parancsmag „-EnableProxyProtocol” paraméteréhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-280">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="d1720-281">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-281">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="d1720-282">Hozzá lett adva egy csomagrögzítési példa a Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és Start-AzVirtualnetworkGatewayPacketCapture.md minden belső és külső csomagjának rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-282">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="d1720-283">Az Azure Firewall-szabályzat mostantól támogatott a Vnet-tűzfalakon</span><span class="sxs-lookup"><span data-stu-id="d1720-283">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="d1720-284">Nem lettek hozzáadva új parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="d1720-284">No new cmdlets are added.</span></span> <span data-ttu-id="d1720-285">Enyhítve lettek a tűzfalszabályzat korlátozásai a Vnet-tűzfalak esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-285">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-287">A fájlokként történő visszaállítás mostantól támogatott az SQL-adatbázisok esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-287">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-288">Az.Resources</span></span>
* <span data-ttu-id="d1720-289">Újra lettek tervezve a sablonalapú üzembehelyezési parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d1720-289">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="d1720-290">Új parancsmagok lettek hozzáadva a felügyeleti csoportban való üzembe helyezés kezeléséhez: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d1720-290">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="d1720-291">Új parancsmagok lettek hozzáadva a bérlői hatókörben való üzembe helyezés kezeléséhez: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d1720-291">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="d1720-292">Az \*-AzDeployment parancsmagok kifejezetten az előfizetési hatókörben való működéshez lettek újratervezve</span><span class="sxs-lookup"><span data-stu-id="d1720-292">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="d1720-293">Az \*-AzSubscriptionDeployment aliasok lettek létrehozva az \*-AzDeployment parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-293">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="d1720-294">Ki lett javítva az „Update-AzADApplication” nem beállított „AvailableToOtherTenants” paraméter esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-294">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="d1720-295">Az ApplicationObjectWithoutCredentialParameterSet el lett távolítva az AmbiguousParameterSetException elkerülése érdekében.</span><span class="sxs-lookup"><span data-stu-id="d1720-295">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="d1720-296">A súgófájlok újra létre lettek hozva</span><span class="sxs-lookup"><span data-stu-id="d1720-296">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-297">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-297">Az.Sql</span></span>
* <span data-ttu-id="d1720-298">Az előfizetések közötti időponthoz kötött visszaállítás mostantól támogatott a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="d1720-298">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="d1720-299">A már meglévő felügyelt SQL-példány hardvergenerációjának módosítása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="d1720-299">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="d1720-300">Ki lettek javítva az „Update-AzSqlServerVulnerabilityAssessmentSetting” súgópéldái: paraméter/tulajdonságkimenet – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="d1720-300">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="d1720-301">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d1720-301">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="d1720-302">Parancsmagokat hozzáadva a rendelkezésreállási csoport figyelőjéhez</span><span class="sxs-lookup"><span data-stu-id="d1720-302">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d1720-303">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d1720-303">Az.StorageSync</span></span>
* <span data-ttu-id="d1720-304">Frissültek az „Invoke-AzStorageSyncCompatibilityCheck” támogatott karakterkészletei.</span><span class="sxs-lookup"><span data-stu-id="d1720-304">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="d1720-305">3.4.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="d1720-305">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d1720-306">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="d1720-306">Highlights since the last major release</span></span>
* <span data-ttu-id="d1720-307">Megjelent az Az.CosmosDB 0.1.0-s kezdeti verziója</span><span class="sxs-lookup"><span data-stu-id="d1720-307">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="d1720-308">Az.Network ConnectionMonitor V2 támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d1720-308">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d1720-309">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-309">Az.Accounts</span></span>
* <span data-ttu-id="d1720-310">A környezet automatikus mentésének letiltása, ha az AzureRmContext.json nem érhető el</span><span class="sxs-lookup"><span data-stu-id="d1720-310">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="d1720-311">Az Azure Powershell Common referenciájának frissítése 1.3.5-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="d1720-311">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d1720-312">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d1720-312">Az.ApiManagement</span></span>
* <span data-ttu-id="d1720-313">**Get-AzApiManagementApiSchema** Az API-val társított Open-API séma kijavítása   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="d1720-313">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="d1720-314">**New-AzApiManagementProduct**\* és **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="d1720-314">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="d1720-315">https://github.com/Azure/azure-powershell/issues/10472 dokumentációja kijavítva</span><span class="sxs-lookup"><span data-stu-id="d1720-315">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="d1720-316">**Set-AzApiManagementApi** A ServiceUrl parancsmaggal való frissítését bemutató példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-316">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-317">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-317">Az.Compute</span></span>
* <span data-ttu-id="d1720-318">A virtuális gép állapotának korlátozása 100 értékre, hogy ne legyen szabályozás, ha a Get-AzVM -Status a virtuális gép neve nélkül lett végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="d1720-318">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="d1720-319">Update-AzDiskEncryptionSet parancsmagok hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d1720-319">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="d1720-320">Az EncryptionType és a DiskEncryptionSetId paraméterek hozzáadása a következő parancsmagokhoz:</span><span class="sxs-lookup"><span data-stu-id="d1720-320">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="d1720-321">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-321">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="d1720-322">A ColocationStatus paraméter hozzáadva a Get-AzProximityPlacementGroup parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-322">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d1720-323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1720-323">Az.DataFactory</span></span>
* <span data-ttu-id="d1720-324">Az ADF .Net SDK frissítve lett a 4.7.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="d1720-324">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d1720-325">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d1720-325">Az.DeploymentManager</span></span>
* <span data-ttu-id="d1720-326">LIST műveletek hozzáadása az erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-326">Adds LIST operations for resources</span></span>
* <span data-ttu-id="d1720-327">Műveletek végrehajtásának lehetősége az állapotellenőrzés lépésein</span><span class="sxs-lookup"><span data-stu-id="d1720-327">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d1720-328">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d1720-328">Az.HDInsight</span></span>
* <span data-ttu-id="d1720-329">A New-AzHDInsightCluster dokumentációs hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="d1720-329">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d1720-330">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d1720-330">Az.KeyVault</span></span>
* <span data-ttu-id="d1720-331">Name alias hozzáadása a VaultName attribútumhoz, hogy a Remove-AzureKeyVault konzisztens legyen a New-AzureKeyVault paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="d1720-331">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-332">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-332">Az.Network</span></span>
* <span data-ttu-id="d1720-333">Új példa hozzáadva a Set-AzNetworkWatcherConfigFlowLog.md fájlhoz a Traffic Analytics-letiltási forgatókönyv szemléltetésére.</span><span class="sxs-lookup"><span data-stu-id="d1720-333">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="d1720-334">Felügyeleti IP-konfiguráció támogatás hozzáadva az Azure Firewallhoz – egy dedikált alhálózat és nyilvános IP-cím, amelyet a tűzfal a forgalom felügyeléséhez használni fog</span><span class="sxs-lookup"><span data-stu-id="d1720-334">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="d1720-335">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="d1720-335">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="d1720-336">Hozzá lett adva a (nem kötelező) -PublicIpAddress-ManagementPublicIpAddress paraméter, amely egy nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="d1720-336">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="d1720-337">Hozzá lett adva a SetManagementIpConfiguration metódus a tűzfalobjektumok esetében – nyilvános IP-cím-objektumokat fogad el bemeneti adatként – az alhálózat nevének AzureFirewallManagementSubnet értéknek kell lennie</span><span class="sxs-lookup"><span data-stu-id="d1720-337">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="d1720-338">A Get-AzNetworkSecurityGroup példái javítva, hogy hálózati biztonsági csoportok példáit tartalmazzák hálózati adapterek helyett.</span><span class="sxs-lookup"><span data-stu-id="d1720-338">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="d1720-339">Javítottunk egy elírást a New-AzVpnSite parancsban, amely megakadályozta, hogy az erőforrásazonosító-kiegészítő kiegészítsen egy paramétert.</span><span class="sxs-lookup"><span data-stu-id="d1720-339">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="d1720-340">Az Application Gateway szabály-újraírási műveletkészletének URL-konfigurálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="d1720-340">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="d1720-341">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d1720-341">New cmdlets added:</span></span>
        - <span data-ttu-id="d1720-342">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1720-342">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="d1720-343">A parancsmagok frissültek a nem kötelező UrlConfiguration paraméterrel</span><span class="sxs-lookup"><span data-stu-id="d1720-343">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="d1720-344">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d1720-344">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="d1720-345">A Network Watcher Connection Monitor 2-es verziójú erőforrások támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-345">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d1720-346">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d1720-346">Az.PolicyInsights</span></span>
* <span data-ttu-id="d1720-347">A javítandó erőforrások azonosítása előtti megfelelőségértékelés támogatása</span><span class="sxs-lookup"><span data-stu-id="d1720-347">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="d1720-348">-ResourceDiscoverMode paraméter hozzáadása a Start-AzPolicyRemediation parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-348">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="d1720-349">A szabályzatok metaadat-erőforrásainak elérésére szolgáló Get-AzPolicyMetadata parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d1720-349">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="d1720-350">A Get-AzPolicyState és a Get-AzPolicyStateSummary frissült a 2019-10-01 API-verzióhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-350">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-351">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-352">Azure Site Recovery-támogatás a replikált lemezek eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="d1720-352">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="d1720-353">Hozzáadott Azure Backup-támogatás a helyreállítási tárak létrehozása közbeni címkehozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-353">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-354">Az.Resources</span></span>
* <span data-ttu-id="d1720-355">A -Scope választható a \*-AzPolicyAssignment parancsmagokban; az alapértelmezett érték a környezeti előfizetés</span><span class="sxs-lookup"><span data-stu-id="d1720-355">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="d1720-356">Az ADServicePrincipal jelszó és kulcs típusú hitelesítő adatokkal való létrehozását szemléltető példák hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-356">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-357">Az.Sql</span></span>
<span data-ttu-id="d1720-358">A New-AzSqlDatabaseSecondary parancsmag javítva, hogy a PartnerDatabaseName létezését ellenőrizze a DatabaseName létezése helyett.</span><span class="sxs-lookup"><span data-stu-id="d1720-358">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-359">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-359">Az.Storage</span></span>
* <span data-ttu-id="d1720-360">A Table/Queue Encryption Keytype készlet beállításának támogatása Storage-fiók létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="d1720-360">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="d1720-361">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d1720-361">New-AzStorageAccount</span></span>
* <span data-ttu-id="d1720-362">RequestId megjelenítése, ha a StorageException nem rendelkezik ExtendedErrorInformation paraméterrel</span><span class="sxs-lookup"><span data-stu-id="d1720-362">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="d1720-363">A Start-AzStorageBlobCopy parancsmag 6. példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="d1720-363">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-364">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-364">Az.Websites</span></span>
* <span data-ttu-id="d1720-365">A Set-AzWebapp és a Set-AzWebappSlot támogatja az AlwaysOn, a MinTls és a FtpsState tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="d1720-365">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="d1720-366">Javítva a hiba, amely miatt a HttpsOnly és az AppservicePlan Set-AzWebApp paranccsal történő egyidejű módosításakor a HttpsOnly paraméter alaphelyzetbe állt.</span><span class="sxs-lookup"><span data-stu-id="d1720-366">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="d1720-367">3.3.0 – 2020. január</span><span class="sxs-lookup"><span data-stu-id="d1720-367">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d1720-368">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-368">Az.Accounts</span></span>
* <span data-ttu-id="d1720-369">Frissítve lettek az Add-AzEnvironment és Set-AzEnvironment parancsmagok, amelyek mostantól elfogadják az AzureAttestationServiceEndpointResourceId és AzureAttestationServiceEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="d1720-369">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d1720-370">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d1720-370">Az.Cdn</span></span>
* <span data-ttu-id="d1720-371">A hibaválasz részleteinek láthatóvá tétele a New-AzCdnEndpoint parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d1720-371">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-372">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-372">Az.Compute</span></span>
* <span data-ttu-id="d1720-373">Javítva lett a Set-AzVMCustomScriptExtension parancsmag az olyan virtuális gépek esetében, amelyek felügyelt operációsrendszer-lemeze nem rendelkezik operációsrendszer-profillal.</span><span class="sxs-lookup"><span data-stu-id="d1720-373">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="d1720-374">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d1720-374">Az.ContainerInstance</span></span>
* <span data-ttu-id="d1720-375">Javítva lettek a New-AzContainerGroup parancsmagpélda által használt paraméternevek</span><span class="sxs-lookup"><span data-stu-id="d1720-375">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="d1720-376">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d1720-376">Az.DataBoxEdge</span></span>
* <span data-ttu-id="d1720-377">Hozzá lett adva a Get-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="d1720-377">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d1720-378">Az Edge Storage-tároló lekérése</span><span class="sxs-lookup"><span data-stu-id="d1720-378">Get the Edge Storage Container</span></span>
* <span data-ttu-id="d1720-379">Hozzá lett adva a New-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="d1720-379">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d1720-380">Új Edge Storage-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="d1720-380">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="d1720-381">Hozzá lett adva a Remove-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="d1720-381">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d1720-382">Az Edge Storage-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d1720-382">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="d1720-383">Hozzá lett adva az Invoke-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="d1720-383">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d1720-384">Meghívási művelet az Edge Storage-tárolóban lévő adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-384">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="d1720-385">Hozzá lett adva a Get-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="d1720-385">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d1720-386">Az Edge Storage-fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="d1720-386">Get the Edge Storage Account</span></span>
* <span data-ttu-id="d1720-387">Hozzá lett adva a New-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="d1720-387">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d1720-388">Új Edge Storage-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="d1720-388">Create new Edge Storage Account</span></span>
* <span data-ttu-id="d1720-389">Hozzá lett adva a Remove-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="d1720-389">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d1720-390">Az Edge Storage-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d1720-390">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="d1720-391">Hozzá lett adva az Invoke-AzDataBoxEdgeShare parancsmag</span><span class="sxs-lookup"><span data-stu-id="d1720-391">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="d1720-392">Meghívási művelet a megosztott adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-392">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="d1720-393">Hozzá lett adva a Set-AzDataBoxEdgeStorageAccountCredential parancsmag</span><span class="sxs-lookup"><span data-stu-id="d1720-393">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="d1720-394">Az Az.DataBoxEdge tárfiók hitelesítő adatainak beállítása</span><span class="sxs-lookup"><span data-stu-id="d1720-394">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d1720-395">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1720-395">Az.DataFactory</span></span>
* <span data-ttu-id="d1720-396">Hozzá lettek adva az AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId és VersionStatus tulajdonságok a Get-AzDataFactoryV2IntegrationRuntime parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-396">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="d1720-397">Az ADF .Net SDK frissítve lett a 4.6.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="d1720-397">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="d1720-398">A PublicIPs paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz statikus nyilvános IP-címekkel rendelkező Azure-SSIS IR létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="d1720-398">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="d1720-399">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="d1720-399">Az.DevTestLabs</span></span>
* <span data-ttu-id="d1720-400">A hibás hivatkozás el lett távolítva a Get-AzDtlAllowedVMSizesPolicy.md parancsmagból</span><span class="sxs-lookup"><span data-stu-id="d1720-400">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d1720-401">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d1720-401">Az.EventHub</span></span>
* <span data-ttu-id="d1720-402">A 10634-es hiba javítása: Ki lett javítva a nullértékű objektumhivatkozás a remove eventhubnamespace esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-402">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d1720-403">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d1720-403">Az.HDInsight</span></span>
* <span data-ttu-id="d1720-404">Ki lett javítva az Invoke-AzHDInsightHiveJob.md hibája.</span><span class="sxs-lookup"><span data-stu-id="d1720-404">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d1720-405">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d1720-405">Az.MachineLearning</span></span>
* <span data-ttu-id="d1720-406">El lettek távolítva az alábbi parancsmagok, mivel a MachineLearningCompute már nem érhető el</span><span class="sxs-lookup"><span data-stu-id="d1720-406">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="d1720-407">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d1720-407">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="d1720-408">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="d1720-408">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="d1720-409">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d1720-409">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="d1720-410">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d1720-410">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="d1720-411">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d1720-411">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="d1720-412">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="d1720-412">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="d1720-413">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="d1720-413">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-414">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-414">Az.Network</span></span>
* <span data-ttu-id="d1720-415">Frissítve lett a Microsoft.Azure.Management.Sql függősége: 1.36-preview helyett 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="d1720-415">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-416">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-416">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-417">Módosított Azure Site Recovery-támogatás azon felügyelt lemezeken található, inaktív állapotban titkosított virtuális gépeknél, amelyekhez felhasználó által kezelt kulcsok tartoznak a következő esetében: Azure – Azure-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="d1720-417">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="d1720-418">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a védelem engedélyezése során a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="d1720-418">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="d1720-419">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a lemez szintjén a védelem engedélyezéséhez a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="d1720-419">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="d1720-420">Azure Site Recovery-támogatás a Replikációval védett, lemeztitkosítási csoportleképezéssel ellátott elemek frissítéséhez a következő esetében: HyperV – Azure.</span><span class="sxs-lookup"><span data-stu-id="d1720-420">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-421">Az.Resources</span></span>
* <span data-ttu-id="d1720-422">Javítva lett egy hiba a Remove-AzTag súgódokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="d1720-422">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-423">Az.Sql</span></span>
* <span data-ttu-id="d1720-424">Javítva lett a sebezhetőségi felmérés csoportszintű alapkonfigurációs parancsmagjainak működése: az Azure-adatbázis főadatbázisában használható, a felügyelt példányok rendszeradatbázisaiban korlátozott.</span><span class="sxs-lookup"><span data-stu-id="d1720-424">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="d1720-425">Ki lett javítva egy hiba az SQL-példányok feladatátvételi csoportjainak létrehozása esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-425">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="d1720-426">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d1720-426">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="d1720-427">Hozzá lett adva a DR, mint új érvényes licenctípus</span><span class="sxs-lookup"><span data-stu-id="d1720-427">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-428">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-428">Az.Storage</span></span>
* <span data-ttu-id="d1720-429">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet a DefaultAction értékének módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="d1720-429">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="d1720-430">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d1720-430">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="d1720-431">Támogatott a tárfiók legutóbbi szinkronizálási időpontjának lekérése a get-AzureRMStorageAccount parancsmag -IncludeGeoReplicationStats paraméterrel való futtatásával</span><span class="sxs-lookup"><span data-stu-id="d1720-431">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="d1720-432">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d1720-432">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="d1720-433">3.2.0 – 2019. december</span><span class="sxs-lookup"><span data-stu-id="d1720-433">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="d1720-434">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d1720-434">General</span></span>
* <span data-ttu-id="d1720-435">A .psd1 hivatkozásai frissítve, hogy minden modulhoz a relatív elérési utat használják</span><span class="sxs-lookup"><span data-stu-id="d1720-435">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d1720-436">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-436">Az.Accounts</span></span>
* <span data-ttu-id="d1720-437">A megfelelő felhasználói ügynök beállítva az ügyféloldali telemetriához az Az 4.0 előzetes verziójában</span><span class="sxs-lookup"><span data-stu-id="d1720-437">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="d1720-438">Felhasználóbarát hibaüzenet megjelenítése, ha az Az 4.0 előzetes verziójában a környezet null értékű</span><span class="sxs-lookup"><span data-stu-id="d1720-438">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d1720-439">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d1720-439">Az.Batch</span></span>
* <span data-ttu-id="d1720-440">Ki lett javítva a [10602-es](https://github.com/Azure/azure-powershell/issues/10602) számú hiba, amely miatt a **New-AzBatchPool** nem megfelelően küldte el a „VirtualMachineConfiguration.ContainerConfiguration” és a „VirtualMachineConfiguration.DataDisks” paramétereket a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="d1720-440">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d1720-441">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1720-441">Az.DataFactory</span></span>
* <span data-ttu-id="d1720-442">Az ADF .Net SDK a 4.5.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d1720-442">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d1720-443">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d1720-443">Az.FrontDoor</span></span>
* <span data-ttu-id="d1720-444">A WAF felügyeleti szabályok kizárása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="d1720-444">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="d1720-445">Hozzá lett adva a SocketAddr automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="d1720-445">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d1720-446">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d1720-446">Az.HealthcareApis</span></span>
* <span data-ttu-id="d1720-447">Kivételkezelés</span><span class="sxs-lookup"><span data-stu-id="d1720-447">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d1720-448">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d1720-448">Az.KeyVault</span></span>
* <span data-ttu-id="d1720-449">Ki lett javítva az esetleg nem beállított értékek hozzáférésével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="d1720-449">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="d1720-450">Az elliptikus görbéjű titkosítási tanúsítványok kezelése</span><span class="sxs-lookup"><span data-stu-id="d1720-450">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="d1720-451">A görbe tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="d1720-451">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d1720-452">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d1720-452">Az.Monitor</span></span>
* <span data-ttu-id="d1720-453">Opcionális argumentum hozzáadva a Diagnosztikai beállítások hozzáadása parancshoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-453">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="d1720-454">Ez egy kapcsoló argumentum, amely megléte esetén azt jelzi, hogy a Log Analyticsbe történő exportálást egy rögzített séma (más néven</span><span class="sxs-lookup"><span data-stu-id="d1720-454">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="d1720-455">dedikált adattípus) szerint kell végrehajtani</span><span class="sxs-lookup"><span data-stu-id="d1720-455">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-456">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-456">Az.Network</span></span>
* <span data-ttu-id="d1720-457">Támogatás az Ip-csoportok számára az AzureFirewall alkalmazás, valamint a Nat- és a hálózati szabályok esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-457">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-458">Az.Resources</span></span>
* <span data-ttu-id="d1720-459">Ki lett javítva az a hiba, amely miatt a sablonalapú üzembe helyezés során a sablonparamétert nem lehet olvasni, ha a sablonparaméter és egy beépített paraméter neve között névütközés áll fenn.</span><span class="sxs-lookup"><span data-stu-id="d1720-459">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="d1720-460">Frissültek a szabályzat parancsmagjai a 2019. 09. 01. dátumú új API-verzió használatára, amely bevezeti a szabályzatkészlet-definíciókon belüli csoportos támogatást.</span><span class="sxs-lookup"><span data-stu-id="d1720-460">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-461">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-461">Az.Sql</span></span>
* <span data-ttu-id="d1720-462">Frissítve lett a sebezhetőségi felmérés automatikus engedélyezéséhez szükséges tárterület létrehozása a Storagev2-ben</span><span class="sxs-lookup"><span data-stu-id="d1720-462">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-463">Az.Storage</span></span>
* <span data-ttu-id="d1720-464">A blob-/tárolóidentitás-alapú SAS-token Oauth-hitelesítésen alapuló Storage-környezettel való létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="d1720-464">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="d1720-465">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d1720-465">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="d1720-466">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d1720-466">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="d1720-467">Támogatott lett a tárfiókhoz tartozó felhasználódelegálási kulcsok visszavonása, így minden identitásalapú SAS-token visszavonható</span><span class="sxs-lookup"><span data-stu-id="d1720-467">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="d1720-468">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="d1720-468">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="d1720-469">Frissítés a Microsoft.Azure.Management.Storage 14.2.0-s verziójára az új API-verzió (2019. 06. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="d1720-469">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="d1720-470">A QuotaGiB (gigabájtban megadott megosztási kvóta) esetében támogatottak az 5120-nál nagyobb értékek a fájlmegosztási parancsmagok felügyeleti síkján, és hozzá lett adva a Quota paraméteralias a QuotaGiB paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-470">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="d1720-471">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d1720-471">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="d1720-472">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d1720-472">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="d1720-473">A „QuotaGiB” paraméteralias hozzáadva a „kvóta” paraméterhez</span><span class="sxs-lookup"><span data-stu-id="d1720-473">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="d1720-474">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="d1720-474">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="d1720-475">Ki lett javítva az a hiba, amely miatt a Set-AzStorageContainerAcl parancsmag el tudta távolítani a tárolt hozzáférési szabályzatot</span><span class="sxs-lookup"><span data-stu-id="d1720-475">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="d1720-476">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="d1720-476">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="d1720-477">3.1.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="d1720-477">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d1720-478">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="d1720-478">Highlights since the last major release</span></span>
* <span data-ttu-id="d1720-479">Az.DataBoxEdge 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="d1720-479">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="d1720-480">Az.SqlVirtualMachine 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="d1720-480">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-481">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-481">Az.Compute</span></span>
* <span data-ttu-id="d1720-482">A virtuális gépek Reapply funkciója</span><span class="sxs-lookup"><span data-stu-id="d1720-482">VM Reapply feature</span></span>
    - <span data-ttu-id="d1720-483">A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-483">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="d1720-484">A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:</span><span class="sxs-lookup"><span data-stu-id="d1720-484">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="d1720-485">Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d1720-485">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="d1720-486">Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-486">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="d1720-487">A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez</span><span class="sxs-lookup"><span data-stu-id="d1720-487">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="d1720-488">A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-488">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="d1720-489">A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező</span><span class="sxs-lookup"><span data-stu-id="d1720-489">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="d1720-490">A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="d1720-490">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="d1720-491">A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d1720-491">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="d1720-492">A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-492">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="d1720-493">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d1720-493">Az.DataBoxEdge</span></span>
* <span data-ttu-id="d1720-494">A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d1720-494">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d1720-495">Megrendelés lekérése</span><span class="sxs-lookup"><span data-stu-id="d1720-495">Get the Order</span></span>
* <span data-ttu-id="d1720-496">A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d1720-496">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d1720-497">Új megrendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="d1720-497">Create new Order</span></span>
* <span data-ttu-id="d1720-498">A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d1720-498">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d1720-499">Megrendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d1720-499">Remove the Order</span></span>
* <span data-ttu-id="d1720-500">`New-AzDataBoxEdgeShare` parancsmag módosítása</span><span class="sxs-lookup"><span data-stu-id="d1720-500">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="d1720-501">Mostantól helyi megosztást hoz létre</span><span class="sxs-lookup"><span data-stu-id="d1720-501">Now creates Local Share</span></span>
* <span data-ttu-id="d1720-502">A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d1720-502">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="d1720-503">Mostantól az IotRole leképezhető a Share-re</span><span class="sxs-lookup"><span data-stu-id="d1720-503">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="d1720-504">A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d1720-504">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="d1720-505">Frissítések keresésének, letöltésének, telepítésének indítása az eszközön</span><span class="sxs-lookup"><span data-stu-id="d1720-505">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="d1720-506">A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d1720-506">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d1720-507">Triggerek információinak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="d1720-507">Gets the information about Triggers</span></span>
* <span data-ttu-id="d1720-508">A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d1720-508">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d1720-509">Új triggerek létrehozása</span><span class="sxs-lookup"><span data-stu-id="d1720-509">Create new Triggers</span></span>
* <span data-ttu-id="d1720-510">A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d1720-510">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d1720-511">Triggerek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d1720-511">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d1720-512">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1720-512">Az.DataFactory</span></span>
* <span data-ttu-id="d1720-513">Az ADF .Net SDK a 4.4.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d1720-513">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="d1720-514">Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-514">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d1720-515">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1720-515">Az.DataLakeStore</span></span>
* <span data-ttu-id="d1720-516">Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d1720-516">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d1720-517">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d1720-517">Az.EventHub</span></span>
* <span data-ttu-id="d1720-518">A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása</span><span class="sxs-lookup"><span data-stu-id="d1720-518">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d1720-519">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d1720-519">Az.FrontDoor</span></span>
* <span data-ttu-id="d1720-520">Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="d1720-520">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="d1720-521">A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="d1720-521">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="d1720-522">Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához</span><span class="sxs-lookup"><span data-stu-id="d1720-522">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="d1720-523">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="d1720-523">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-524">Az.Network</span></span>
* <span data-ttu-id="d1720-525">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.</span><span class="sxs-lookup"><span data-stu-id="d1720-525">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="d1720-526">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="d1720-526">Az.PrivateDns</span></span>
* <span data-ttu-id="d1720-527">A PrivateDns .net sdk frissült az 1.0.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="d1720-527">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-528">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-528">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-529">Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="d1720-529">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="d1720-530">Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-530">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="d1720-531">SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="d1720-531">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d1720-532">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d1720-532">Az.RedisCache</span></span>
* <span data-ttu-id="d1720-533">A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="d1720-533">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="d1720-534">Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-534">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="d1720-535">Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-535">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-536">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-536">Az.Resources</span></span>
- <span data-ttu-id="d1720-537">Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.</span><span class="sxs-lookup"><span data-stu-id="d1720-537">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="d1720-538">Frissült a létrehozási szabályzat definíciójának súgóbeli példája</span><span class="sxs-lookup"><span data-stu-id="d1720-538">Updated create policy definition help example</span></span>
- <span data-ttu-id="d1720-539">Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.</span><span class="sxs-lookup"><span data-stu-id="d1720-539">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="d1720-540">Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.</span><span class="sxs-lookup"><span data-stu-id="d1720-540">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="d1720-541">A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="d1720-541">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-542">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-542">Az.Sql</span></span>
* <span data-ttu-id="d1720-543">Az adatbázisbeli ReadReplicaCount mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="d1720-543">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="d1720-544">A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén</span><span class="sxs-lookup"><span data-stu-id="d1720-544">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="d1720-545">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="d1720-545">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="d1720-546">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d1720-546">General</span></span>
* <span data-ttu-id="d1720-547">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d1720-547">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d1720-548">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-548">Az.Accounts</span></span>
* <span data-ttu-id="d1720-549">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="d1720-549">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d1720-550">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d1720-550">Az.Advisor</span></span>
* <span data-ttu-id="d1720-551">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-551">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d1720-552">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d1720-552">Az.Batch</span></span>
* <span data-ttu-id="d1720-553">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="d1720-553">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="d1720-554">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="d1720-554">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="d1720-555">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="d1720-555">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="d1720-556">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="d1720-556">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="d1720-557">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-557">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="d1720-558">Ezek az **New-AzBatchTask**`-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="d1720-558">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="d1720-559">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="d1720-559">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="d1720-560">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="d1720-560">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="d1720-561">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="d1720-561">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="d1720-562">A `PSApplication`**Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-562">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="d1720-563">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="d1720-563">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="d1720-564">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="d1720-564">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="d1720-565">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-565">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="d1720-566">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="d1720-566">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="d1720-567">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="d1720-567">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="d1720-568">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-568">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="d1720-569">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-569">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="d1720-570">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="d1720-570">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="d1720-571">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-571">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="d1720-572">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="d1720-572">This operation is no longer supported.</span></span>
* <span data-ttu-id="d1720-573">`PSCloudServiceConfiguration``TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-573">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="d1720-574">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-574">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="d1720-575">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="d1720-575">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="d1720-576">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="d1720-576">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="d1720-577">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="d1720-577">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="d1720-578">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="d1720-578">New non-verified images are also now returned.</span></span> <span data-ttu-id="d1720-579">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="d1720-579">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="d1720-580">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="d1720-580">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="d1720-581">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="d1720-581">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="d1720-582">Ez a `PSNetworkSecurityGroupRule``SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="d1720-582">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="d1720-583">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="d1720-583">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="d1720-584">Ezt a `PSTaskContainerSettings``WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="d1720-584">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="d1720-585">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="d1720-585">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="d1720-586">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="d1720-586">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="d1720-587">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="d1720-587">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="d1720-588">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="d1720-588">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d1720-589">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d1720-589">Az.Cdn</span></span>
* <span data-ttu-id="d1720-590">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="d1720-590">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="d1720-591">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="d1720-591">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-592">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-592">Az.Compute</span></span>
* <span data-ttu-id="d1720-593">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="d1720-593">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="d1720-594">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d1720-594">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="d1720-595">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d1720-595">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="d1720-596">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-596">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d1720-597">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-597">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="d1720-598">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="d1720-598">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="d1720-599">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-599">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="d1720-600">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="d1720-600">Breaking changes</span></span>
    - <span data-ttu-id="d1720-601">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="d1720-601">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="d1720-602">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="d1720-602">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d1720-603">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1720-603">Az.DataFactory</span></span>
* <span data-ttu-id="d1720-604">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d1720-604">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d1720-605">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1720-605">Az.DataLakeStore</span></span>
* <span data-ttu-id="d1720-606">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="d1720-606">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="d1720-607">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="d1720-607">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="d1720-608">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="d1720-608">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="d1720-609">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="d1720-609">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="d1720-610">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-610">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="d1720-611">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="d1720-611">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d1720-612">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d1720-612">Az.FrontDoor</span></span>
* <span data-ttu-id="d1720-613">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="d1720-613">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d1720-614">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d1720-614">Az.HDInsight</span></span>
* <span data-ttu-id="d1720-615">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-615">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="d1720-616">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-616">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="d1720-617">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="d1720-617">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="d1720-618">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="d1720-618">Removed five cmdlets:</span></span>
    - <span data-ttu-id="d1720-619">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d1720-619">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d1720-620">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d1720-620">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d1720-621">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d1720-621">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d1720-622">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d1720-622">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="d1720-623">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d1720-623">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="d1720-624">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="d1720-624">Added three cmdlets:</span></span>
    - <span data-ttu-id="d1720-625">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="d1720-625">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="d1720-626">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="d1720-626">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="d1720-627">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="d1720-627">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="d1720-628">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="d1720-628">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="d1720-629">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="d1720-629">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="d1720-630">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="d1720-630">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="d1720-631">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="d1720-631">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="d1720-632">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="d1720-632">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="d1720-633">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="d1720-633">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="d1720-634">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="d1720-634">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="d1720-635">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="d1720-635">Added some scenario test cases.</span></span>
* <span data-ttu-id="d1720-636">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="d1720-636">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d1720-637">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d1720-637">Az.IotHub</span></span>
* <span data-ttu-id="d1720-638">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="d1720-638">Breaking changes:</span></span>
    - <span data-ttu-id="d1720-639">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-639">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d1720-640">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-640">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d1720-641">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-641">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d1720-642">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-642">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d1720-643">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-643">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="d1720-644">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-644">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="d1720-645">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="d1720-645">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="d1720-646">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="d1720-646">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="d1720-647">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-647">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d1720-648">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-648">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d1720-649">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-649">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d1720-650">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-650">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-651">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-651">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-652">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="d1720-652">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="d1720-653">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="d1720-653">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="d1720-654">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="d1720-654">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="d1720-655">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="d1720-655">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="d1720-656">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="d1720-656">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="d1720-657">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="d1720-657">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="d1720-658">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="d1720-658">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="d1720-659">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="d1720-659">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="d1720-660">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="d1720-660">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-661">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-661">Az.Resources</span></span>
* <span data-ttu-id="d1720-662">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="d1720-662">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-663">Az.Network</span></span>
* <span data-ttu-id="d1720-664">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="d1720-664">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="d1720-665">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="d1720-665">Updated cmdlet:</span></span>
        - <span data-ttu-id="d1720-666">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-666">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d1720-667">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-667">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d1720-668">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-668">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d1720-669">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-669">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d1720-670">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-670">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d1720-671">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="d1720-671">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="d1720-672">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="d1720-672">New cmdlet:</span></span>
        - <span data-ttu-id="d1720-673">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d1720-673">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="d1720-674">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-674">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="d1720-675">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="d1720-675">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="d1720-676">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="d1720-676">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="d1720-677">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="d1720-677">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="d1720-678">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="d1720-678">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="d1720-679">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="d1720-679">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="d1720-680">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-680">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="d1720-681">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d1720-681">New cmdlets added:</span></span>
        - <span data-ttu-id="d1720-682">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="d1720-682">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="d1720-683">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1720-683">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d1720-684">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1720-684">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d1720-685">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1720-685">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d1720-686">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d1720-686">Set-AzVirtualHub</span></span>
* <span data-ttu-id="d1720-687">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-687">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="d1720-688">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d1720-688">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d1720-689">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-689">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="d1720-690">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-690">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="d1720-691">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-691">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="d1720-692">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-692">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="d1720-693">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-693">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="d1720-694">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d1720-694">New cmdlets added:</span></span>
        - <span data-ttu-id="d1720-695">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-695">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="d1720-696">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d1720-696">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d1720-697">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-697">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d1720-698">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-698">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d1720-699">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-699">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d1720-700">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-700">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d1720-701">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-701">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="d1720-702">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-702">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="d1720-703">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d1720-703">New cmdlets added:</span></span>
        - <span data-ttu-id="d1720-704">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="d1720-704">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="d1720-705">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="d1720-705">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="d1720-706">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="d1720-706">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="d1720-707">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="d1720-707">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="d1720-708">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="d1720-708">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="d1720-709">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="d1720-709">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="d1720-710">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d1720-710">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d1720-711">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-711">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="d1720-712">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-712">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="d1720-713">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="d1720-713">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="d1720-714">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-714">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="d1720-715">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d1720-715">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d1720-716">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-716">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="d1720-717">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-717">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="d1720-718">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="d1720-718">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="d1720-719">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="d1720-719">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="d1720-720">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-720">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="d1720-721">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d1720-721">New cmdlets added:</span></span>
        - <span data-ttu-id="d1720-722">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d1720-722">New-AzIpGroup</span></span>
        - <span data-ttu-id="d1720-723">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d1720-723">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="d1720-724">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d1720-724">Get-AzIpGroup</span></span>
        - <span data-ttu-id="d1720-725">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d1720-725">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d1720-726">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d1720-726">Az.ServiceFabric</span></span>
* <span data-ttu-id="d1720-727">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="d1720-727">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-728">Az.Sql</span></span>
* <span data-ttu-id="d1720-729">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="d1720-729">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="d1720-730">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="d1720-730">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="d1720-731">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="d1720-731">Removed deprecated aliases:</span></span>
* <span data-ttu-id="d1720-732">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="d1720-732">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="d1720-733">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="d1720-733">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="d1720-734">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="d1720-734">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d1720-735">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="d1720-735">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="d1720-736">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="d1720-736">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="d1720-737">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="d1720-737">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-738">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-738">Az.Storage</span></span>
* <span data-ttu-id="d1720-739">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="d1720-739">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="d1720-740">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d1720-740">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d1720-741">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d1720-741">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d1720-742">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="d1720-742">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="d1720-743">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d1720-743">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="d1720-744">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d1720-744">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="d1720-745">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="d1720-745">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="d1720-746">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d1720-746">General</span></span>
* <span data-ttu-id="d1720-747">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="d1720-747">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d1720-748">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-748">Az.Accounts</span></span>
* <span data-ttu-id="d1720-749">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="d1720-749">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d1720-750">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d1720-750">Az.ApiManagement</span></span>
* <span data-ttu-id="d1720-751">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d1720-751">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="d1720-752">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="d1720-752">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d1720-753">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d1720-753">Az.Automation</span></span>
* <span data-ttu-id="d1720-754">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="d1720-754">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d1720-755">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d1720-755">Az.Batch</span></span>
* <span data-ttu-id="d1720-756">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="d1720-756">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-757">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-757">Az.Compute</span></span>
* <span data-ttu-id="d1720-758">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-758">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="d1720-759">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="d1720-759">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="d1720-760">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="d1720-760">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="d1720-761">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="d1720-761">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d1720-762">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1720-762">Az.DataFactory</span></span>
* <span data-ttu-id="d1720-763">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="d1720-763">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="d1720-764">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="d1720-764">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="d1720-765">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d1720-765">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d1720-766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1720-766">Az.DataLakeStore</span></span>
* <span data-ttu-id="d1720-767">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="d1720-767">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d1720-768">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d1720-768">Az.HealthcareApis</span></span>
* <span data-ttu-id="d1720-769">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d1720-769">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="d1720-770">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d1720-770">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="d1720-771">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="d1720-771">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="d1720-772">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="d1720-772">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d1720-773">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d1720-773">Az.IotHub</span></span>
* <span data-ttu-id="d1720-774">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="d1720-774">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="d1720-775">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1720-775">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d1720-776">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d1720-776">Az.Monitor</span></span>
* <span data-ttu-id="d1720-777">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="d1720-777">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="d1720-778">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="d1720-778">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="d1720-779">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="d1720-779">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="d1720-780">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="d1720-780">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-781">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-781">Az.Network</span></span>
* <span data-ttu-id="d1720-782">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="d1720-782">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="d1720-783">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="d1720-783">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="d1720-784">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d1720-784">New cmdlets added:</span></span>
        - <span data-ttu-id="d1720-785">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="d1720-785">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="d1720-786">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-786">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d1720-787">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="d1720-787">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="d1720-788">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d1720-788">Updated cmdlets:</span></span>
        - <span data-ttu-id="d1720-789">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-789">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d1720-790">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-790">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d1720-791">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-791">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d1720-792">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="d1720-792">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="d1720-793">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="d1720-793">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="d1720-794">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="d1720-794">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="d1720-795">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="d1720-795">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d1720-796">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d1720-796">Az.RedisCache</span></span>
* <span data-ttu-id="d1720-797">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="d1720-797">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-798">Az.Sql</span></span>
* <span data-ttu-id="d1720-799">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="d1720-799">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-800">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-800">Az.Storage</span></span>
* <span data-ttu-id="d1720-801">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="d1720-801">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="d1720-802">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="d1720-802">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d1720-803">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d1720-803">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="d1720-804">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="d1720-804">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d1720-805">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d1720-805">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d1720-806">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d1720-806">Az.StorageSync</span></span>
* <span data-ttu-id="d1720-807">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="d1720-807">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-808">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-808">Az.Websites</span></span>
* <span data-ttu-id="d1720-809">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="d1720-809">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="d1720-810">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="d1720-810">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d1720-811">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d1720-811">Az.ApiManagement</span></span>
* <span data-ttu-id="d1720-812">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="d1720-812">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="d1720-813">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="d1720-813">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="d1720-814">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="d1720-814">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d1720-815">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d1720-815">Az.Automation</span></span>
* <span data-ttu-id="d1720-816">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="d1720-816">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="d1720-817">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-817">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="d1720-818">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="d1720-818">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-819">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-819">Az.Compute</span></span>
* <span data-ttu-id="d1720-820">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-820">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="d1720-821">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-821">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d1720-822">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="d1720-822">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="d1720-823">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-823">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="d1720-824">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-824">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="d1720-825">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="d1720-825">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="d1720-826">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="d1720-826">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="d1720-827">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-827">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="d1720-828">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-828">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d1720-829">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1720-829">Az.DataFactory</span></span>
* <span data-ttu-id="d1720-830">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="d1720-830">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="d1720-831">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d1720-831">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d1720-832">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d1720-832">Az.HDInsight</span></span>
* <span data-ttu-id="d1720-833">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="d1720-833">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d1720-834">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d1720-834">Az.IotHub</span></span>
* <span data-ttu-id="d1720-835">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="d1720-835">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="d1720-836">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="d1720-836">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="d1720-837">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="d1720-837">New cmdlets are:</span></span>
    - <span data-ttu-id="d1720-838">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d1720-838">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d1720-839">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d1720-839">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d1720-840">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d1720-840">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d1720-841">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d1720-841">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d1720-842">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d1720-842">Az.Monitor</span></span>
* <span data-ttu-id="d1720-843">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="d1720-843">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="d1720-844">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="d1720-844">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="d1720-845">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="d1720-845">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="d1720-846">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="d1720-846">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="d1720-847">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-847">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="d1720-848">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="d1720-848">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="d1720-849">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="d1720-849">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="d1720-850">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="d1720-850">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="d1720-851">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="d1720-851">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d1720-852">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="d1720-852">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="d1720-853">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="d1720-853">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d1720-854">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="d1720-854">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="d1720-855">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-855">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="d1720-856">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="d1720-856">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="d1720-857">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="d1720-857">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="d1720-858">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="d1720-858">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="d1720-859">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="d1720-859">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="d1720-860">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="d1720-860">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="d1720-861">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="d1720-861">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="d1720-862">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="d1720-862">Overall improved help files</span></span>
* <span data-ttu-id="d1720-863">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="d1720-863">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-864">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-864">Az.Network</span></span>
* <span data-ttu-id="d1720-865">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="d1720-865">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="d1720-866">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="d1720-866">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="d1720-867">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="d1720-867">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="d1720-868">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="d1720-868">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="d1720-869">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="d1720-869">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="d1720-870">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="d1720-870">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="d1720-871">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="d1720-871">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="d1720-872">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-872">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="d1720-873">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-873">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="d1720-874">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="d1720-874">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="d1720-875">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="d1720-875">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="d1720-876">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="d1720-876">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="d1720-877">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d1720-877">New cmdlets</span></span>
        - <span data-ttu-id="d1720-878">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="d1720-878">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="d1720-879">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-879">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="d1720-880">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="d1720-880">Updated cmdlet:</span></span>
        - <span data-ttu-id="d1720-881">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="d1720-881">New-VpnSite</span></span>
        - <span data-ttu-id="d1720-882">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="d1720-882">Update-VpnSite</span></span>
        - <span data-ttu-id="d1720-883">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-883">New-VpnConnection</span></span>
        - <span data-ttu-id="d1720-884">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-884">Update-VpnConnection</span></span>
* <span data-ttu-id="d1720-885">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="d1720-885">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-886">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-886">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-887">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="d1720-887">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="d1720-888">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="d1720-888">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-889">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-889">Az.Resources</span></span>
* <span data-ttu-id="d1720-890">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="d1720-890">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d1720-891">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d1720-891">Az.ServiceFabric</span></span>
* <span data-ttu-id="d1720-892">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="d1720-892">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="d1720-893">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="d1720-893">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="d1720-894">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d1720-894">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d1720-895">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d1720-895">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d1720-896">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d1720-896">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d1720-897">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d1720-897">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="d1720-898">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d1720-898">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d1720-899">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d1720-899">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d1720-900">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d1720-900">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d1720-901">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d1720-901">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d1720-902">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d1720-902">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="d1720-903">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d1720-903">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d1720-904">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d1720-904">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d1720-905">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d1720-905">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d1720-906">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="d1720-906">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="d1720-907">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="d1720-907">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d1720-908">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d1720-908">Az.SignalR</span></span>
* <span data-ttu-id="d1720-909">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d1720-909">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-910">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-910">Az.Sql</span></span>
* <span data-ttu-id="d1720-911">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="d1720-911">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="d1720-912">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="d1720-912">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="d1720-913">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d1720-913">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="d1720-914">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="d1720-914">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="d1720-915">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="d1720-915">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-916">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-916">Az.Storage</span></span>
* <span data-ttu-id="d1720-917">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="d1720-917">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="d1720-918">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-918">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="d1720-919">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d1720-919">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="d1720-920">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d1720-920">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="d1720-921">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-921">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="d1720-922">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d1720-922">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="d1720-923">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="d1720-923">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="d1720-924">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d1720-924">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d1720-925">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d1720-925">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d1720-926">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d1720-926">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d1720-927">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d1720-927">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-928">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-928">Az.Websites</span></span>
* <span data-ttu-id="d1720-929">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="d1720-929">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="d1720-930">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="d1720-930">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="d1720-931">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="d1720-931">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="d1720-932">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="d1720-932">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="d1720-933">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d1720-933">General</span></span>
* <span data-ttu-id="d1720-934">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="d1720-934">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d1720-935">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-935">Az.Accounts</span></span>
* <span data-ttu-id="d1720-936">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="d1720-936">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="d1720-937">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d1720-937">Az.Aks</span></span>
* <span data-ttu-id="d1720-938">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="d1720-938">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="d1720-939">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="d1720-939">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d1720-940">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d1720-940">Az.ApiManagement</span></span>
* <span data-ttu-id="d1720-941">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="d1720-941">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="d1720-942">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="d1720-942">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="d1720-943">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="d1720-943">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="d1720-944">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="d1720-944">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="d1720-945">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="d1720-945">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d1720-946">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d1720-946">Az.Batch</span></span>
* <span data-ttu-id="d1720-947">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="d1720-947">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d1720-948">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d1720-948">Az.Cdn</span></span>
* <span data-ttu-id="d1720-949">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="d1720-949">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-950">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-950">Az.Compute</span></span>
* <span data-ttu-id="d1720-951">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-951">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="d1720-952">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-952">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="d1720-953">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-953">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="d1720-954">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="d1720-954">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="d1720-955">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="d1720-955">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="d1720-956">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-956">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="d1720-957">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="d1720-957">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="d1720-958">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="d1720-958">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d1720-959">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1720-959">Az.DataFactory</span></span>
* <span data-ttu-id="d1720-960">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="d1720-960">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="d1720-961">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d1720-961">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="d1720-962">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="d1720-962">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="d1720-963">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="d1720-963">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d1720-964">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1720-964">Az.DataLakeStore</span></span>
* <span data-ttu-id="d1720-965">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="d1720-965">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d1720-966">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d1720-966">Az.EventHub</span></span>
* <span data-ttu-id="d1720-967">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d1720-967">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="d1720-968">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="d1720-968">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="d1720-969">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-969">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="d1720-970">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="d1720-970">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="d1720-971">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d1720-971">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d1720-972">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="d1720-972">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d1720-973">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d1720-973">Az.Monitor</span></span>
* <span data-ttu-id="d1720-974">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="d1720-974">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-975">Az.Network</span></span>
* <span data-ttu-id="d1720-976">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-976">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="d1720-977">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="d1720-977">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="d1720-978">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="d1720-978">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="d1720-979">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="d1720-979">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="d1720-980">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="d1720-980">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="d1720-981">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="d1720-981">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="d1720-982">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="d1720-982">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d1720-983">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d1720-983">Az.OperationalInsights</span></span>
* <span data-ttu-id="d1720-984">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d1720-984">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="d1720-985">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-985">Added example</span></span>
    - <span data-ttu-id="d1720-986">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="d1720-986">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="d1720-987">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-987">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="d1720-988">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="d1720-988">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-989">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-990">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="d1720-990">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-991">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-991">Az.Resources</span></span>
* <span data-ttu-id="d1720-992">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="d1720-992">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="d1720-993">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-993">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="d1720-994">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="d1720-994">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="d1720-995">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-995">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d1720-996">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d1720-996">Az.ServiceBus</span></span>
* <span data-ttu-id="d1720-997">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d1720-997">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="d1720-998">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="d1720-998">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="d1720-999">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="d1720-999">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d1720-1000">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d1720-1000">Az.ServiceFabric</span></span>
* <span data-ttu-id="d1720-1001">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="d1720-1001">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="d1720-1002">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="d1720-1002">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="d1720-1003">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="d1720-1003">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="d1720-1004">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="d1720-1004">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="d1720-1005">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="d1720-1005">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="d1720-1006">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="d1720-1006">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-1007">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1007">Az.Sql</span></span>
* <span data-ttu-id="d1720-1008">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="d1720-1008">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-1009">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-1009">Az.Storage</span></span>
* <span data-ttu-id="d1720-1010">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="d1720-1010">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="d1720-1011">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1011">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="d1720-1012">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d1720-1012">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="d1720-1013">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d1720-1013">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="d1720-1014">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="d1720-1014">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="d1720-1015">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d1720-1015">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-1016">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-1016">Az.Websites</span></span>
* <span data-ttu-id="d1720-1017">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1017">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="d1720-1018">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="d1720-1018">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d1720-1019">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-1019">Az.Accounts</span></span>
* <span data-ttu-id="d1720-1020">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="d1720-1020">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="d1720-1021">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d1720-1021">Az.ApplicationInsights</span></span>
* <span data-ttu-id="d1720-1022">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1022">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d1720-1023">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d1720-1023">Az.Automation</span></span>
* <span data-ttu-id="d1720-1024">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1024">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d1720-1025">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1025">Az.CognitiveServices</span></span>
* <span data-ttu-id="d1720-1026">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="d1720-1026">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-1027">Az.Compute</span></span>
* <span data-ttu-id="d1720-1028">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="d1720-1028">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d1720-1029">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d1720-1029">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d1720-1030">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1030">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="d1720-1031">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="d1720-1031">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d1720-1032">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1720-1032">Az.DataFactory</span></span>
* <span data-ttu-id="d1720-1033">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d1720-1033">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="d1720-1034">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1034">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d1720-1035">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d1720-1035">Az.EventHub</span></span>
* <span data-ttu-id="d1720-1036">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="d1720-1036">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d1720-1037">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="d1720-1037">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d1720-1038">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d1720-1038">Az.KeyVault</span></span>
* <span data-ttu-id="d1720-1039">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="d1720-1039">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d1720-1040">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d1720-1040">Az.LogicApp</span></span>
* <span data-ttu-id="d1720-1041">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="d1720-1041">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="d1720-1042">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="d1720-1042">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="d1720-1043">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1043">Az.ManagedServices</span></span>
* <span data-ttu-id="d1720-1044">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-1044">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-1045">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-1045">Az.Network</span></span>
* <span data-ttu-id="d1720-1046">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-1046">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="d1720-1047">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d1720-1047">New cmdlets</span></span>
        - <span data-ttu-id="d1720-1048">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1720-1048">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d1720-1049">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d1720-1049">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d1720-1050">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-1050">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d1720-1051">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-1051">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d1720-1052">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-1052">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d1720-1053">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-1053">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d1720-1054">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="d1720-1054">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="d1720-1055">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d1720-1055">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="d1720-1056">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="d1720-1056">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="d1720-1057">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="d1720-1057">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="d1720-1058">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-1058">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="d1720-1059">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-1059">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="d1720-1060">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="d1720-1060">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="d1720-1061">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1061">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="d1720-1062">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d1720-1062">Updated cmdlets</span></span>
        - <span data-ttu-id="d1720-1063">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-1063">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d1720-1064">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-1064">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d1720-1065">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-1065">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d1720-1066">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="d1720-1066">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d1720-1067">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="d1720-1067">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="d1720-1068">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="d1720-1068">Updated cmdlet:</span></span>
        - <span data-ttu-id="d1720-1069">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-1069">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d1720-1070">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-1070">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d1720-1071">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-1071">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="d1720-1072">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="d1720-1072">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="d1720-1073">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="d1720-1073">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="d1720-1074">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="d1720-1074">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d1720-1075">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d1720-1075">Az.OperationalInsights</span></span>
* <span data-ttu-id="d1720-1076">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="d1720-1076">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="d1720-1077">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="d1720-1077">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-1078">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1078">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-1079">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1079">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d1720-1080">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1080">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="d1720-1081">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1081">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="d1720-1082">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1082">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d1720-1083">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1083">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="d1720-1084">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1084">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d1720-1085">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1085">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="d1720-1086">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1086">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d1720-1087">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1087">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="d1720-1088">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1088">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-1089">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-1089">Az.Resources</span></span>
- <span data-ttu-id="d1720-1090">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1090">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="d1720-1091">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="d1720-1091">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d1720-1092">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d1720-1092">Az.ServiceBus</span></span>
* <span data-ttu-id="d1720-1093">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="d1720-1093">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d1720-1094">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="d1720-1094">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-1095">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1095">Az.Sql</span></span>
* <span data-ttu-id="d1720-1096">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1096">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="d1720-1097">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1097">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="d1720-1098">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="d1720-1098">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-1099">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-1099">Az.Storage</span></span>
* <span data-ttu-id="d1720-1100">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="d1720-1100">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d1720-1101">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d1720-1101">Az.StorageSync</span></span>
* <span data-ttu-id="d1720-1102">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="d1720-1102">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="d1720-1103">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="d1720-1103">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-1104">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-1104">Az.Websites</span></span>
* <span data-ttu-id="d1720-1105">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="d1720-1105">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="d1720-1106">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1106">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="d1720-1107">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1107">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="d1720-1108">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="d1720-1108">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d1720-1109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-1109">Az.Accounts</span></span>
* <span data-ttu-id="d1720-1110">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d1720-1110">Add support for profile cmdlets</span></span>
* <span data-ttu-id="d1720-1111">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d1720-1111">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="d1720-1112">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="d1720-1112">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d1720-1113">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d1720-1113">Az.Advisor</span></span>
* <span data-ttu-id="d1720-1114">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="d1720-1114">GA release of Az.Advisor</span></span>
* <span data-ttu-id="d1720-1115">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="d1720-1115">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d1720-1116">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d1720-1116">Az.ApiManagement</span></span>
* <span data-ttu-id="d1720-1117">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="d1720-1117">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="d1720-1118">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d1720-1118">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="d1720-1119">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-1119">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="d1720-1120">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-1120">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="d1720-1121">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="d1720-1121">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="d1720-1122">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d1720-1122">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="d1720-1123">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="d1720-1123">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d1720-1124">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d1720-1124">Az.Automation</span></span>
* <span data-ttu-id="d1720-1125">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="d1720-1125">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-1126">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-1126">Az.Compute</span></span>
* <span data-ttu-id="d1720-1127">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1127">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d1720-1128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1720-1128">Az.DataFactory</span></span>
* <span data-ttu-id="d1720-1129">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="d1720-1129">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d1720-1130">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d1720-1130">Az.EventGrid</span></span>
* <span data-ttu-id="d1720-1131">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="d1720-1131">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d1720-1132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d1720-1132">Az.IotHub</span></span>
* <span data-ttu-id="d1720-1133">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="d1720-1133">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-1134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-1134">Az.Network</span></span>
* <span data-ttu-id="d1720-1135">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1135">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="d1720-1136">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="d1720-1136">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d1720-1137">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d1720-1137">Az.PolicyInsights</span></span>
* <span data-ttu-id="d1720-1138">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d1720-1138">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="d1720-1139">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="d1720-1139">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d1720-1140">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d1720-1140">Az.OperationalInsights</span></span>
* <span data-ttu-id="d1720-1141">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="d1720-1141">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-1142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1142">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-1143">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1143">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-1144">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-1144">Az.Resources</span></span>
    - <span data-ttu-id="d1720-1145">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1145">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="d1720-1146">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1146">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="d1720-1147">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1147">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="d1720-1148">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1148">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d1720-1149">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d1720-1149">Az.ServiceBus</span></span>
* <span data-ttu-id="d1720-1150">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="d1720-1150">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1151">Az.Sql</span></span>
* <span data-ttu-id="d1720-1152">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1152">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="d1720-1153">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="d1720-1153">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="d1720-1154">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d1720-1154">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d1720-1155">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d1720-1155">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d1720-1156">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d1720-1156">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d1720-1157">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d1720-1157">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d1720-1158">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d1720-1158">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d1720-1159">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d1720-1159">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="d1720-1160">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="d1720-1160">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-1161">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-1161">Az.Storage</span></span>
* <span data-ttu-id="d1720-1162">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="d1720-1162">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="d1720-1163">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d1720-1163">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="d1720-1164">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="d1720-1164">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="d1720-1165">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="d1720-1165">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="d1720-1166">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="d1720-1166">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="d1720-1167">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d1720-1167">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d1720-1168">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d1720-1168">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d1720-1169">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="d1720-1169">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="d1720-1170">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d1720-1170">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="d1720-1171">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d1720-1171">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d1720-1172">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d1720-1172">Az.StorageSync</span></span>
* <span data-ttu-id="d1720-1173">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="d1720-1173">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="d1720-1174">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="d1720-1174">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d1720-1175">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-1175">Az.Accounts</span></span>
* <span data-ttu-id="d1720-1176">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1176">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="d1720-1177">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="d1720-1177">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="d1720-1178">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1178">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="d1720-1179">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d1720-1179">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="d1720-1180">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="d1720-1180">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-1181">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-1181">Az.Compute</span></span>
* <span data-ttu-id="d1720-1182">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="d1720-1182">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="d1720-1183">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="d1720-1183">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="d1720-1184">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d1720-1184">Az.Dns</span></span>
* <span data-ttu-id="d1720-1185">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="d1720-1185">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d1720-1186">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d1720-1186">Az.EventGrid</span></span>
* <span data-ttu-id="d1720-1187">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="d1720-1187">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="d1720-1188">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d1720-1188">New cmdlets:</span></span>
    - <span data-ttu-id="d1720-1189">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d1720-1189">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d1720-1190">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="d1720-1190">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d1720-1191">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d1720-1191">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d1720-1192">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="d1720-1192">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="d1720-1193">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d1720-1193">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d1720-1194">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="d1720-1194">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d1720-1195">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d1720-1195">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d1720-1196">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-1196">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d1720-1197">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d1720-1197">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d1720-1198">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="d1720-1198">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="d1720-1199">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="d1720-1199">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d1720-1200">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d1720-1200">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="d1720-1201">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d1720-1201">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="d1720-1202">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="d1720-1202">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="d1720-1203">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="d1720-1203">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d1720-1204">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="d1720-1204">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="d1720-1205">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d1720-1205">Updated cmdlets:</span></span>
    - <span data-ttu-id="d1720-1206">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="d1720-1206">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="d1720-1207">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="d1720-1207">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d1720-1208">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="d1720-1208">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d1720-1209">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="d1720-1209">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="d1720-1210">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="d1720-1210">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="d1720-1211">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="d1720-1211">Event subscription expiration date,</span></span>
            - <span data-ttu-id="d1720-1212">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="d1720-1212">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="d1720-1213">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="d1720-1213">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="d1720-1214">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="d1720-1214">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="d1720-1215">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="d1720-1215">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="d1720-1216">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="d1720-1216">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="d1720-1217">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d1720-1217">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="d1720-1218">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="d1720-1218">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="d1720-1219">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="d1720-1219">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d1720-1220">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d1720-1220">Az.FrontDoor</span></span>
* <span data-ttu-id="d1720-1221">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="d1720-1221">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="d1720-1222">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="d1720-1222">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="d1720-1223">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="d1720-1223">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="d1720-1224">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="d1720-1224">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-1225">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-1225">Az.Network</span></span>
* <span data-ttu-id="d1720-1226">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-1226">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="d1720-1227">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d1720-1227">New cmdlets</span></span>
        - <span data-ttu-id="d1720-1228">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="d1720-1228">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="d1720-1229">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-1229">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="d1720-1230">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d1720-1230">New cmdlets</span></span>
        - <span data-ttu-id="d1720-1231">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d1720-1231">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="d1720-1232">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-1232">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="d1720-1233">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d1720-1233">New cmdlets</span></span>
        - <span data-ttu-id="d1720-1234">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d1720-1234">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d1720-1235">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d1720-1235">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d1720-1236">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d1720-1236">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d1720-1237">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-1237">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="d1720-1238">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-1238">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d1720-1239">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-1239">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="d1720-1240">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d1720-1240">New cmdlets</span></span>
        - <span data-ttu-id="d1720-1241">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1720-1241">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d1720-1242">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1720-1242">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d1720-1243">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1720-1243">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d1720-1244">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="d1720-1244">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="d1720-1245">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="d1720-1245">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="d1720-1246">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="d1720-1246">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="d1720-1247">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="d1720-1247">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="d1720-1248">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-1248">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="d1720-1249">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-1249">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="d1720-1250">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="d1720-1250">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="d1720-1251">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="d1720-1251">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="d1720-1252">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="d1720-1252">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="d1720-1253">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1253">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="d1720-1254">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="d1720-1254">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="d1720-1255">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1255">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="d1720-1256">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1256">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="d1720-1257">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="d1720-1257">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="d1720-1258">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1258">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="d1720-1259">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="d1720-1259">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="d1720-1260">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="d1720-1260">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="d1720-1261">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="d1720-1261">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="d1720-1262">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="d1720-1262">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="d1720-1263">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="d1720-1263">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="d1720-1264">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-1264">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="d1720-1265">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-1265">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d1720-1266">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-1266">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d1720-1267">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-1267">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d1720-1268">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d1720-1268">Az.OperationalInsights</span></span>
* <span data-ttu-id="d1720-1269">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1269">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-1270">Az.Resources</span></span>
* <span data-ttu-id="d1720-1271">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="d1720-1271">Support for additional Template Export options</span></span>
    - <span data-ttu-id="d1720-1272">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1272">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d1720-1273">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1273">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d1720-1274">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1274">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d1720-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d1720-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="d1720-1276">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="d1720-1276">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-1277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1277">Az.Sql</span></span>
* <span data-ttu-id="d1720-1278">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="d1720-1278">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="d1720-1279">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="d1720-1279">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="d1720-1280">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1280">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="d1720-1281">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d1720-1281">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d1720-1282">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d1720-1282">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d1720-1283">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d1720-1283">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d1720-1284">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d1720-1284">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="d1720-1285">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d1720-1285">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-1286">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-1286">Az.Storage</span></span>
* <span data-ttu-id="d1720-1287">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="d1720-1287">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="d1720-1288">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d1720-1288">New-AzStorageAccount</span></span>
* <span data-ttu-id="d1720-1289">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="d1720-1289">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="d1720-1290">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d1720-1290">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-1291">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-1291">Az.Websites</span></span>
* <span data-ttu-id="d1720-1292">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="d1720-1292">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="d1720-1293">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1293">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="d1720-1294">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="d1720-1294">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="d1720-1295">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d1720-1295">Az.Cdn</span></span>
* <span data-ttu-id="d1720-1296">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="d1720-1296">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-1297">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-1297">Az.Compute</span></span>
* <span data-ttu-id="d1720-1298">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="d1720-1298">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="d1720-1299">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d1720-1299">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d1720-1300">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d1720-1300">Az.EventHub</span></span>
* <span data-ttu-id="d1720-1301">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="d1720-1301">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="d1720-1302">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="d1720-1302">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-1303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-1303">Az.Network</span></span>
* <span data-ttu-id="d1720-1304">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="d1720-1304">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="d1720-1305">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d1720-1305">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d1720-1306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d1720-1306">Az.PolicyInsights</span></span>
* <span data-ttu-id="d1720-1307">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d1720-1307">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-1308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1308">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-1309">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="d1720-1309">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d1720-1310">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d1720-1310">Az.ServiceBus</span></span>
* <span data-ttu-id="d1720-1311">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="d1720-1311">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d1720-1312">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d1720-1312">Az.ServiceFabric</span></span>
* <span data-ttu-id="d1720-1313">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1313">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="d1720-1314">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="d1720-1314">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-1315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1315">Az.Sql</span></span>
* <span data-ttu-id="d1720-1316">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="d1720-1316">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="d1720-1317">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="d1720-1317">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d1720-1318">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="d1720-1318">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="d1720-1319">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="d1720-1319">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-1320">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-1320">Az.Websites</span></span>
* <span data-ttu-id="d1720-1321">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="d1720-1321">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="d1720-1322">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="d1720-1322">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d1720-1323">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d1720-1323">Az.ApiManagement</span></span>
* <span data-ttu-id="d1720-1324">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="d1720-1324">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="d1720-1325">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="d1720-1325">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="d1720-1326">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="d1720-1326">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="d1720-1327">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="d1720-1327">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="d1720-1328">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-1328">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="d1720-1329">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1329">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="d1720-1330">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="d1720-1330">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="d1720-1331">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="d1720-1331">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="d1720-1332">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1332">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="d1720-1333">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="d1720-1333">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="d1720-1334">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="d1720-1334">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="d1720-1335">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1335">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="d1720-1336">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1336">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="d1720-1337">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1337">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="d1720-1338">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1338">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="d1720-1339">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="d1720-1339">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="d1720-1340">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1340">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="d1720-1341">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1341">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="d1720-1342">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="d1720-1342">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="d1720-1343">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="d1720-1343">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="d1720-1344">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1344">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="d1720-1345">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="d1720-1345">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="d1720-1346">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="d1720-1346">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="d1720-1347">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1347">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="d1720-1348">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="d1720-1348">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="d1720-1349">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="d1720-1349">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="d1720-1350">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="d1720-1350">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="d1720-1351">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="d1720-1351">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="d1720-1352">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="d1720-1352">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="d1720-1353">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="d1720-1353">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="d1720-1354">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1354">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="d1720-1355">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="d1720-1355">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="d1720-1356">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="d1720-1356">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="d1720-1357">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1357">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d1720-1358">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="d1720-1358">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="d1720-1359">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="d1720-1359">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="d1720-1360">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="d1720-1360">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="d1720-1361">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="d1720-1361">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="d1720-1362">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="d1720-1362">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="d1720-1363">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1363">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d1720-1364">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="d1720-1364">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d1720-1365">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="d1720-1365">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d1720-1366">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="d1720-1366">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="d1720-1367">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="d1720-1367">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="d1720-1368">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1368">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d1720-1369">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="d1720-1369">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d1720-1370">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="d1720-1370">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d1720-1371">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="d1720-1371">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="d1720-1372">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1372">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="d1720-1373">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="d1720-1373">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="d1720-1374">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="d1720-1374">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="d1720-1375">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1375">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="d1720-1376">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="d1720-1376">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="d1720-1377">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1377">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="d1720-1378">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="d1720-1378">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="d1720-1379">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1379">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="d1720-1380">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1380">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d1720-1381">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1381">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d1720-1382">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1382">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d1720-1383">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1383">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d1720-1384">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1384">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d1720-1385">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1385">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d1720-1386">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1386">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d1720-1387">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1387">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d1720-1388">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="d1720-1388">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="d1720-1389">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d1720-1389">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="d1720-1390">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="d1720-1390">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="d1720-1391">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d1720-1391">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="d1720-1392">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="d1720-1392">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="d1720-1393">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d1720-1393">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="d1720-1394">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="d1720-1394">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="d1720-1395">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d1720-1395">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="d1720-1396">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d1720-1396">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="d1720-1397">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="d1720-1397">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="d1720-1398">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d1720-1398">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="d1720-1399">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d1720-1399">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="d1720-1400">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d1720-1400">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d1720-1401">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d1720-1401">Az.Automation</span></span>
* <span data-ttu-id="d1720-1402">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1402">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="d1720-1403">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="d1720-1403">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="d1720-1404">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="d1720-1404">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="d1720-1405">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="d1720-1405">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="d1720-1406">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="d1720-1406">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="d1720-1407">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="d1720-1407">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="d1720-1408">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d1720-1408">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-1409">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-1409">Az.Compute</span></span>
* <span data-ttu-id="d1720-1410">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1410">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="d1720-1411">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="d1720-1411">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d1720-1412">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1720-1412">Az.DataLakeStore</span></span>
* <span data-ttu-id="d1720-1413">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="d1720-1413">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d1720-1414">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d1720-1414">Az.Monitor</span></span>
* <span data-ttu-id="d1720-1415">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="d1720-1415">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-1416">Az.Network</span></span>
* <span data-ttu-id="d1720-1417">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1417">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="d1720-1418">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="d1720-1418">Updated cmdlet:</span></span>
        - <span data-ttu-id="d1720-1419">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1720-1419">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="d1720-1420">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="d1720-1420">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-1421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-1421">Az.Resources</span></span>
* <span data-ttu-id="d1720-1422">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1422">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-1423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1423">Az.Sql</span></span>
* <span data-ttu-id="d1720-1424">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="d1720-1424">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="d1720-1425">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="d1720-1425">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d1720-1426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-1426">Az.Accounts</span></span>
* <span data-ttu-id="d1720-1427">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="d1720-1427">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d1720-1428">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1428">Az.CognitiveServices</span></span>
* <span data-ttu-id="d1720-1429">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="d1720-1429">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="d1720-1430">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="d1720-1430">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-1431">Az.Compute</span></span>
* <span data-ttu-id="d1720-1432">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="d1720-1432">Proximity placement group feature.</span></span>
    - <span data-ttu-id="d1720-1433">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d1720-1433">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="d1720-1434">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-1434">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="d1720-1435">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-1435">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="d1720-1436">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="d1720-1436">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="d1720-1437">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1437">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="d1720-1438">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="d1720-1438">Breaking changes</span></span>
    - <span data-ttu-id="d1720-1439">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="d1720-1439">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="d1720-1440">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="d1720-1440">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d1720-1441">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d1720-1441">Az.DeploymentManager</span></span>
* <span data-ttu-id="d1720-1442">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="d1720-1442">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="d1720-1443">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d1720-1443">Az.Dns</span></span>
* <span data-ttu-id="d1720-1444">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="d1720-1444">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="d1720-1445">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1445">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="d1720-1446">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="d1720-1446">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d1720-1447">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d1720-1447">Az.FrontDoor</span></span>
* <span data-ttu-id="d1720-1448">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="d1720-1448">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="d1720-1449">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="d1720-1449">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="d1720-1450">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d1720-1450">Az.HDInsight</span></span>
* <span data-ttu-id="d1720-1451">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="d1720-1451">Removed two cmdlets:</span></span>
    - <span data-ttu-id="d1720-1452">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d1720-1452">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="d1720-1453">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d1720-1453">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d1720-1454">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="d1720-1454">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d1720-1455">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="d1720-1455">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="d1720-1456">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="d1720-1456">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="d1720-1457">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="d1720-1457">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d1720-1458">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d1720-1458">Az.Monitor</span></span>
* <span data-ttu-id="d1720-1459">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="d1720-1459">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="d1720-1460">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="d1720-1460">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="d1720-1461">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="d1720-1461">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="d1720-1462">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d1720-1462">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="d1720-1463">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d1720-1463">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="d1720-1464">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d1720-1464">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="d1720-1465">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="d1720-1465">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="d1720-1466">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d1720-1466">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d1720-1467">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d1720-1467">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d1720-1468">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d1720-1468">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d1720-1469">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d1720-1469">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d1720-1470">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d1720-1470">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d1720-1471">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="d1720-1471">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="d1720-1472">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="d1720-1472">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-1473">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-1473">Az.Network</span></span>
* <span data-ttu-id="d1720-1474">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-1474">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="d1720-1475">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d1720-1475">New cmdlets</span></span>
        - <span data-ttu-id="d1720-1476">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d1720-1476">New-AzNatGateway</span></span>
        - <span data-ttu-id="d1720-1477">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d1720-1477">Get-AzNatGateway</span></span>
        - <span data-ttu-id="d1720-1478">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d1720-1478">Set-AzNatGateway</span></span>
        - <span data-ttu-id="d1720-1479">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d1720-1479">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="d1720-1480">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d1720-1480">Updated cmdlets</span></span>
        - <span data-ttu-id="d1720-1481">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d1720-1481">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="d1720-1482">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d1720-1482">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="d1720-1483">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d1720-1483">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="d1720-1484">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d1720-1484">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="d1720-1485">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d1720-1485">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d1720-1486">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d1720-1486">Az.PolicyInsights</span></span>
* <span data-ttu-id="d1720-1487">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="d1720-1487">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="d1720-1488">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-1488">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="d1720-1489">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="d1720-1489">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-1490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1490">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-1491">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="d1720-1491">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="d1720-1492">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="d1720-1492">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="d1720-1493">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="d1720-1493">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="d1720-1494">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="d1720-1494">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="d1720-1495">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="d1720-1495">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="d1720-1496">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="d1720-1496">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="d1720-1497">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d1720-1497">Az.Relay</span></span>
* <span data-ttu-id="d1720-1498">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="d1720-1498">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d1720-1499">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d1720-1499">Az.ServiceBus</span></span>
* <span data-ttu-id="d1720-1500">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="d1720-1500">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-1501">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-1501">Az.Storage</span></span>
* <span data-ttu-id="d1720-1502">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="d1720-1502">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="d1720-1503">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="d1720-1503">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="d1720-1504">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="d1720-1504">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="d1720-1505">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d1720-1505">New-AzStorageAccount</span></span>
* <span data-ttu-id="d1720-1506">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="d1720-1506">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="d1720-1507">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d1720-1507">New-AzStorageAccount</span></span>
    - <span data-ttu-id="d1720-1508">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d1720-1508">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="d1720-1509">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d1720-1509">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-1510">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-1510">Az.Websites</span></span>
* <span data-ttu-id="d1720-1511">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1511">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="d1720-1512">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="d1720-1512">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="d1720-1513">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="d1720-1513">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d1720-1514">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="d1720-1514">Highlights since the last major release</span></span>
* <span data-ttu-id="d1720-1515">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="d1720-1515">General availability of `Az` module</span></span>
* <span data-ttu-id="d1720-1516">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d1720-1516">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d1720-1517">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d1720-1517">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d1720-1518">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1518">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d1720-1519">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1519">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d1720-1520">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1520">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d1720-1521">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1521">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d1720-1522">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-1522">Az.Accounts</span></span>
* <span data-ttu-id="d1720-1523">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1523">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d1720-1524">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d1720-1524">Az.Batch</span></span>
* <span data-ttu-id="d1720-1525">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1525">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d1720-1526">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d1720-1526">Az.Cdn</span></span>
* <span data-ttu-id="d1720-1527">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1527">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d1720-1528">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1528">Az.CognitiveServices</span></span>
* <span data-ttu-id="d1720-1529">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1529">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-1530">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-1530">Az.Compute</span></span>
* <span data-ttu-id="d1720-1531">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="d1720-1531">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="d1720-1532">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1532">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d1720-1533">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d1720-1533">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d1720-1534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1720-1534">Az.DataFactory</span></span>
* <span data-ttu-id="d1720-1535">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="d1720-1535">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d1720-1536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1720-1536">Az.DataLakeStore</span></span>
* <span data-ttu-id="d1720-1537">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1537">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d1720-1538">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d1720-1538">Az.EventGrid</span></span>
* <span data-ttu-id="d1720-1539">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="d1720-1539">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d1720-1540">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d1720-1540">Az.EventHub</span></span>
* <span data-ttu-id="d1720-1541">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="d1720-1541">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d1720-1542">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d1720-1542">Az.HDInsight</span></span>
* <span data-ttu-id="d1720-1543">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1543">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d1720-1544">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d1720-1544">Az.IotHub</span></span>
* <span data-ttu-id="d1720-1545">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1545">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d1720-1546">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d1720-1546">Az.KeyVault</span></span>
* <span data-ttu-id="d1720-1547">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1547">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d1720-1548">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d1720-1548">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d1720-1549">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d1720-1549">Az.MachineLearning</span></span>
* <span data-ttu-id="d1720-1550">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1550">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="d1720-1551">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d1720-1551">Az.Media</span></span>
* <span data-ttu-id="d1720-1552">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1552">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d1720-1553">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d1720-1553">Az.Monitor</span></span>
  * <span data-ttu-id="d1720-1554">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d1720-1554">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="d1720-1555">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d1720-1555">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="d1720-1556">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d1720-1556">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="d1720-1557">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d1720-1557">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d1720-1558">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d1720-1558">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d1720-1559">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d1720-1559">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="d1720-1560">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="d1720-1560">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-1561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-1561">Az.Network</span></span>
* <span data-ttu-id="d1720-1562">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1562">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d1720-1563">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d1720-1563">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="d1720-1564">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="d1720-1564">Az.NotificationHubs</span></span>
* <span data-ttu-id="d1720-1565">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1565">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d1720-1566">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d1720-1566">Az.OperationalInsights</span></span>
* <span data-ttu-id="d1720-1567">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1567">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="d1720-1568">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d1720-1568">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="d1720-1569">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-1570">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1570">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-1571">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1571">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d1720-1572">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="d1720-1572">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="d1720-1573">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="d1720-1573">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="d1720-1574">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="d1720-1574">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d1720-1575">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d1720-1575">Az.RedisCache</span></span>
* <span data-ttu-id="d1720-1576">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1576">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-1577">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-1577">Az.Resources</span></span>
* <span data-ttu-id="d1720-1578">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d1720-1578">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-1579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1579">Az.Sql</span></span>
* <span data-ttu-id="d1720-1580">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="d1720-1580">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="d1720-1581">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1581">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d1720-1582">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="d1720-1582">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="d1720-1583">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d1720-1583">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="d1720-1584">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="d1720-1584">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="d1720-1585">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="d1720-1585">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="d1720-1586">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d1720-1586">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-1587">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-1587">Az.Websites</span></span>
* <span data-ttu-id="d1720-1588">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="d1720-1588">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="d1720-1589">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d1720-1589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d1720-1590">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="d1720-1590">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="d1720-1591">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="d1720-1591">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="d1720-1592">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="d1720-1592">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d1720-1593">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="d1720-1593">Highlights since the last major release</span></span>
* <span data-ttu-id="d1720-1594">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="d1720-1594">General availability of `Az` module</span></span>
* <span data-ttu-id="d1720-1595">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d1720-1595">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d1720-1596">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d1720-1596">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d1720-1597">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1597">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d1720-1598">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1598">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d1720-1599">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1599">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d1720-1600">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1600">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d1720-1601">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-1601">Az.Accounts</span></span>
* <span data-ttu-id="d1720-1602">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="d1720-1602">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d1720-1603">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1603">Az.AnalysisServices</span></span>
* <span data-ttu-id="d1720-1604">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1604">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="d1720-1605">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1605">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d1720-1606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d1720-1606">Az.Automation</span></span>
* <span data-ttu-id="d1720-1607">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="d1720-1607">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="d1720-1608">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="d1720-1608">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="d1720-1609">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1609">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-1610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-1610">Az.Compute</span></span>
* <span data-ttu-id="d1720-1611">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1611">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d1720-1612">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="d1720-1612">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="d1720-1613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d1720-1613">Az.ContainerInstance</span></span>
* <span data-ttu-id="d1720-1614">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="d1720-1614">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d1720-1615">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1720-1615">Az.DataFactory</span></span>
* <span data-ttu-id="d1720-1616">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="d1720-1616">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="d1720-1617">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="d1720-1617">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-1618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-1618">Az.Resources</span></span>
* <span data-ttu-id="d1720-1619">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="d1720-1619">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="d1720-1620">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1620">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="d1720-1621">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="d1720-1621">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="d1720-1622">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d1720-1622">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="d1720-1623">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1623">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="d1720-1624">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d1720-1624">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-1625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1625">Az.Sql</span></span>
* <span data-ttu-id="d1720-1626">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="d1720-1626">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-1627">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-1627">Az.Storage</span></span>
* <span data-ttu-id="d1720-1628">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="d1720-1628">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="d1720-1629">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d1720-1629">New-AzStorageContext</span></span>
* <span data-ttu-id="d1720-1630">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="d1720-1630">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="d1720-1631">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d1720-1631">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d1720-1632">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d1720-1632">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d1720-1633">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d1720-1633">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="d1720-1634">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d1720-1634">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="d1720-1635">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1635">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="d1720-1636">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d1720-1636">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d1720-1637">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d1720-1637">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d1720-1638">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d1720-1638">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="d1720-1639">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d1720-1639">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="d1720-1640">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="d1720-1640">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d1720-1641">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="d1720-1641">Highlights since the last major release</span></span>
* <span data-ttu-id="d1720-1642">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="d1720-1642">General availability of `Az` module</span></span>
* <span data-ttu-id="d1720-1643">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d1720-1643">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d1720-1644">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d1720-1644">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d1720-1645">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1645">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d1720-1646">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1646">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d1720-1647">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1647">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d1720-1648">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1648">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d1720-1649">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d1720-1649">Az.Automation</span></span>
* <span data-ttu-id="d1720-1650">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="d1720-1650">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="d1720-1651">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="d1720-1651">Dynamic grouping</span></span>
    * <span data-ttu-id="d1720-1652">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="d1720-1652">Pre-Post script</span></span>
    * <span data-ttu-id="d1720-1653">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="d1720-1653">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-1654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-1654">Az.Compute</span></span>
* <span data-ttu-id="d1720-1655">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1655">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="d1720-1656">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="d1720-1656">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d1720-1657">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d1720-1657">Az.KeyVault</span></span>
* <span data-ttu-id="d1720-1658">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1658">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-1659">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-1659">Az.Network</span></span>
* <span data-ttu-id="d1720-1660">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1660">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="d1720-1661">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-1661">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-1662">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1662">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-1663">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="d1720-1663">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="d1720-1664">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1664">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-1665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-1665">Az.Resources</span></span>
* <span data-ttu-id="d1720-1666">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1666">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="d1720-1667">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1667">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-1668">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1668">Az.Sql</span></span>
* <span data-ttu-id="d1720-1669">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="d1720-1669">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-1670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-1670">Az.Storage</span></span>
* <span data-ttu-id="d1720-1671">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="d1720-1671">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="d1720-1672">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d1720-1672">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d1720-1673">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d1720-1673">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d1720-1674">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d1720-1674">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d1720-1675">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d1720-1675">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="d1720-1676">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="d1720-1676">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="d1720-1677">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="d1720-1677">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-1678">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-1678">Az.Websites</span></span>
* <span data-ttu-id="d1720-1679">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="d1720-1679">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="d1720-1680">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="d1720-1680">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d1720-1681">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-1681">Az.Accounts</span></span>
* <span data-ttu-id="d1720-1682">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="d1720-1682">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="d1720-1683">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1683">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d1720-1684">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d1720-1684">Az.Automation</span></span>
* <span data-ttu-id="d1720-1685">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1685">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="d1720-1686">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="d1720-1686">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="d1720-1687">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="d1720-1687">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d1720-1688">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d1720-1688">Az.Cdn</span></span>
* <span data-ttu-id="d1720-1689">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="d1720-1689">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-1690">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-1690">Az.Compute</span></span>
* <span data-ttu-id="d1720-1691">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1691">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d1720-1692">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1720-1692">Az.DataFactory</span></span>
* <span data-ttu-id="d1720-1693">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="d1720-1693">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d1720-1694">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d1720-1694">Az.LogicApp</span></span>
* <span data-ttu-id="d1720-1695">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="d1720-1695">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-1696">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-1696">Az.Network</span></span>
* <span data-ttu-id="d1720-1697">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1697">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-1698">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1698">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-1699">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d1720-1699">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="d1720-1700">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="d1720-1700">SDK Update</span></span>
* <span data-ttu-id="d1720-1701">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="d1720-1701">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="d1720-1702">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1702">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-1703">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-1703">Az.Resources</span></span>
* <span data-ttu-id="d1720-1704">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1704">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="d1720-1705">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="d1720-1705">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="d1720-1706">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="d1720-1706">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="d1720-1707">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="d1720-1707">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="d1720-1708">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="d1720-1708">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="d1720-1709">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="d1720-1709">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-1710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1710">Az.Sql</span></span>
* <span data-ttu-id="d1720-1711">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="d1720-1711">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="d1720-1712">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="d1720-1712">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-1713">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-1713">Az.Storage</span></span>
* <span data-ttu-id="d1720-1714">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d1720-1714">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="d1720-1715">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="d1720-1715">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="d1720-1716">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1716">Az.AnalysisServices</span></span>
* <span data-ttu-id="d1720-1717">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="d1720-1717">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d1720-1718">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d1720-1718">Az.Automation</span></span>
* <span data-ttu-id="d1720-1719">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1719">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="d1720-1720">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1720">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="d1720-1721">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1721">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d1720-1722">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1722">Az.CognitiveServices</span></span>
* <span data-ttu-id="d1720-1723">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-1723">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-1724">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-1724">Az.Compute</span></span>
* <span data-ttu-id="d1720-1725">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="d1720-1725">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="d1720-1726">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="d1720-1726">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="d1720-1727">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1727">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="d1720-1728">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="d1720-1728">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d1720-1729">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1720-1729">Az.DataLakeStore</span></span>
* <span data-ttu-id="d1720-1730">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="d1720-1730">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d1720-1731">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d1720-1731">Az.EventHub</span></span>
* <span data-ttu-id="d1720-1732">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="d1720-1732">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d1720-1733">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d1720-1733">Az.KeyVault</span></span>
* <span data-ttu-id="d1720-1734">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1734">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d1720-1735">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d1720-1735">Az.LogicApp</span></span>
* <span data-ttu-id="d1720-1736">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="d1720-1736">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="d1720-1737">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="d1720-1737">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="d1720-1738">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="d1720-1738">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="d1720-1739">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d1720-1739">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d1720-1740">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d1720-1740">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d1720-1741">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d1720-1741">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d1720-1742">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d1720-1742">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="d1720-1743">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="d1720-1743">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="d1720-1744">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1720-1744">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d1720-1745">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1720-1745">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d1720-1746">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1720-1746">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d1720-1747">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1720-1747">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="d1720-1748">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="d1720-1748">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d1720-1749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d1720-1749">Az.Monitor</span></span>
* <span data-ttu-id="d1720-1750">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1750">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-1751">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-1751">Az.Network</span></span>
* <span data-ttu-id="d1720-1752">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="d1720-1752">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d1720-1753">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d1720-1753">Az.OperationalInsights</span></span>
* <span data-ttu-id="d1720-1754">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-1754">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="d1720-1755">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="d1720-1755">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="d1720-1756">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="d1720-1756">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-1757">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-1757">Az.Resources</span></span>
* <span data-ttu-id="d1720-1758">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d1720-1758">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d1720-1759">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d1720-1759">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="d1720-1760">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="d1720-1760">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="d1720-1761">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="d1720-1761">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-1762">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1762">Az.Sql</span></span>
* <span data-ttu-id="d1720-1763">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-1763">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="d1720-1764">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="d1720-1764">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-1765">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-1765">Az.Websites</span></span>
* <span data-ttu-id="d1720-1766">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1766">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="d1720-1767">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="d1720-1767">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d1720-1768">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-1768">Az.Accounts</span></span>
* <span data-ttu-id="d1720-1769">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="d1720-1769">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d1720-1770">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1770">Az.AnalysisServices</span></span>
<span data-ttu-id="d1720-1771">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="d1720-1771">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-1772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-1772">Az.Compute</span></span>
* <span data-ttu-id="d1720-1773">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="d1720-1773">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="d1720-1774">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="d1720-1774">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="d1720-1775">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="d1720-1775">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-1776">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1776">Az.RecoveryServices</span></span>
<span data-ttu-id="d1720-1777">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="d1720-1777">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-1778">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-1778">Az.Resources</span></span>
* <span data-ttu-id="d1720-1779">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-1779">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="d1720-1780">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d1720-1780">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d1720-1781">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="d1720-1781">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="d1720-1782">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d1720-1782">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-1783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1783">Az.Sql</span></span>
* <span data-ttu-id="d1720-1784">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-1784">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="d1720-1785">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="d1720-1785">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="d1720-1786">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="d1720-1786">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="d1720-1787">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="d1720-1787">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d1720-1788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-1788">Az.Accounts</span></span>
* <span data-ttu-id="d1720-1789">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="d1720-1789">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d1720-1790">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1790">Az.AnalysisServices</span></span>
* <span data-ttu-id="d1720-1791">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="d1720-1791">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-1792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1792">Az.RecoveryServices</span></span>
* <span data-ttu-id="d1720-1793">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="d1720-1793">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="d1720-1794">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="d1720-1794">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d1720-1795">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-1795">Az.Accounts</span></span>
* <span data-ttu-id="d1720-1796">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1796">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d1720-1797">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d1720-1797">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d1720-1798">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="d1720-1798">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="d1720-1799">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d1720-1799">Az.Aks</span></span>
* <span data-ttu-id="d1720-1800">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d1720-1800">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d1720-1801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d1720-1801">Az.Automation</span></span>
* <span data-ttu-id="d1720-1802">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="d1720-1802">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="d1720-1803">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d1720-1803">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d1720-1804">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d1720-1804">Az.Cdn</span></span>
* <span data-ttu-id="d1720-1805">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d1720-1805">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-1806">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-1806">Az.Compute</span></span>
* <span data-ttu-id="d1720-1807">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="d1720-1807">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="d1720-1808">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-1808">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="d1720-1809">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-1809">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d1720-1810">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d1720-1810">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d1720-1811">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d1720-1811">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d1720-1812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d1720-1812">Az.DataFactory</span></span>
* <span data-ttu-id="d1720-1813">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="d1720-1813">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d1720-1814">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1720-1814">Az.DataLakeStore</span></span>
* <span data-ttu-id="d1720-1815">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="d1720-1815">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="d1720-1816">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="d1720-1816">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="d1720-1817">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d1720-1817">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d1720-1818">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d1720-1818">Az.IotHub</span></span>
* <span data-ttu-id="d1720-1819">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-1819">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d1720-1820">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d1720-1820">Az.KeyVault</span></span>
* <span data-ttu-id="d1720-1821">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d1720-1821">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-1822">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-1822">Az.Network</span></span>
* <span data-ttu-id="d1720-1823">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d1720-1823">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-1824">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-1824">Az.Resources</span></span>
* <span data-ttu-id="d1720-1825">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="d1720-1825">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="d1720-1826">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="d1720-1826">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="d1720-1827">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-1827">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="d1720-1828">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="d1720-1828">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="d1720-1829">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="d1720-1829">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="d1720-1830">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="d1720-1830">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="d1720-1831">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="d1720-1831">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d1720-1832">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d1720-1832">Az.ServiceFabric</span></span>
* <span data-ttu-id="d1720-1833">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="d1720-1833">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="d1720-1834">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-1834">Fix some error messages.</span></span>
* <span data-ttu-id="d1720-1835">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="d1720-1835">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="d1720-1836">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="d1720-1836">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d1720-1837">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d1720-1837">Az.SignalR</span></span>
* <span data-ttu-id="d1720-1838">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d1720-1838">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-1839">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1839">Az.Sql</span></span>
* <span data-ttu-id="d1720-1840">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d1720-1840">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d1720-1841">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="d1720-1841">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="d1720-1842">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="d1720-1842">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="d1720-1843">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="d1720-1843">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-1844">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-1844">Az.Storage</span></span>
* <span data-ttu-id="d1720-1845">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d1720-1845">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d1720-1846">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="d1720-1846">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="d1720-1847">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d1720-1847">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="d1720-1848">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="d1720-1848">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="d1720-1849">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d1720-1849">Az.TrafficManager</span></span>
* <span data-ttu-id="d1720-1850">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d1720-1850">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-1851">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-1851">Az.Websites</span></span>
* <span data-ttu-id="d1720-1852">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d1720-1852">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d1720-1853">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="d1720-1853">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="d1720-1854">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="d1720-1854">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="d1720-1855">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="d1720-1855">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d1720-1856">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-1856">Az.Accounts</span></span>
* <span data-ttu-id="d1720-1857">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1857">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-1858">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-1858">Az.Compute</span></span>
* <span data-ttu-id="d1720-1859">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="d1720-1859">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="d1720-1860">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="d1720-1860">Updated the description of ID in help files</span></span>
* <span data-ttu-id="d1720-1861">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="d1720-1861">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d1720-1862">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1720-1862">Az.DataLakeStore</span></span>
* <span data-ttu-id="d1720-1863">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="d1720-1863">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="d1720-1864">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="d1720-1864">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d1720-1865">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d1720-1865">Az.EventGrid</span></span>
* <span data-ttu-id="d1720-1866">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="d1720-1866">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="d1720-1867">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="d1720-1867">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="d1720-1868">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="d1720-1868">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d1720-1869">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="d1720-1869">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d1720-1870">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="d1720-1870">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d1720-1871">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="d1720-1871">Dead letter endpoint.</span></span>
    - <span data-ttu-id="d1720-1872">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="d1720-1872">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d1720-1873">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="d1720-1873">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d1720-1874">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="d1720-1874">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d1720-1875">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="d1720-1875">Dead letter endpoint.</span></span>
* <span data-ttu-id="d1720-1876">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="d1720-1876">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="d1720-1877">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="d1720-1877">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d1720-1878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d1720-1878">Az.IotHub</span></span>
* <span data-ttu-id="d1720-1879">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="d1720-1879">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d1720-1880">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d1720-1880">Az.LogicApp</span></span>
* <span data-ttu-id="d1720-1881">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="d1720-1881">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-1882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-1882">Az.Resources</span></span>
* <span data-ttu-id="d1720-1883">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="d1720-1883">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="d1720-1884">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="d1720-1884">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="d1720-1885">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="d1720-1885">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d1720-1886">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="d1720-1886">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="d1720-1887">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="d1720-1887">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="d1720-1888">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="d1720-1888">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d1720-1889">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d1720-1889">Az.SignalR</span></span>
* <span data-ttu-id="d1720-1890">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="d1720-1890">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-1891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1891">Az.Sql</span></span>
* <span data-ttu-id="d1720-1892">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="d1720-1892">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d1720-1893">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-1893">Az.Storage</span></span>
* <span data-ttu-id="d1720-1894">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="d1720-1894">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="d1720-1895">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d1720-1895">New-AzStorageContext</span></span>
* <span data-ttu-id="d1720-1896">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="d1720-1896">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="d1720-1897">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d1720-1897">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-1898">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-1898">Az.Websites</span></span>
* <span data-ttu-id="d1720-1899">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d1720-1899">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="d1720-1900">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="d1720-1900">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="d1720-1901">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="d1720-1901">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="d1720-1902">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d1720-1902">General</span></span>

- <span data-ttu-id="d1720-1903">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="d1720-1903">General Availability of Az Module</span></span>
- <span data-ttu-id="d1720-1904">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1904">Online help for each module</span></span>
- <span data-ttu-id="d1720-1905">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="d1720-1905">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="d1720-1906">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d1720-1906">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="d1720-1907">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-1907">Az.Accounts</span></span>
- <span data-ttu-id="d1720-1908">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="d1720-1908">Changed from Az.Profile</span></span>
- <span data-ttu-id="d1720-1909">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1909">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d1720-1910">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d1720-1910">Az.ApiManagement</span></span>
- <span data-ttu-id="d1720-1911">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="d1720-1911">Fixes for #7002</span></span>
- <span data-ttu-id="d1720-1912">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d1720-1912">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="d1720-1913">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d1720-1913">Az.Batch</span></span>
- <span data-ttu-id="d1720-1914">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="d1720-1914">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="d1720-1915">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="d1720-1915">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="d1720-1916">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d1720-1916">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="d1720-1917">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d1720-1917">Az.Billing</span></span>
- <span data-ttu-id="d1720-1918">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="d1720-1918">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="d1720-1919">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1919">Az.CognitivServices</span></span>
- <span data-ttu-id="d1720-1920">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="d1720-1920">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="d1720-1921">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="d1720-1921">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d1720-1922">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d1720-1922">Az.ContainerInstance</span></span>
- <span data-ttu-id="d1720-1923">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="d1720-1923">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="d1720-1924">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d1720-1924">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="d1720-1925">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d1720-1925">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d1720-1926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1720-1926">Az.DataLakeStore</span></span>
- <span data-ttu-id="d1720-1927">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d1720-1927">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="d1720-1928">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d1720-1928">Az.Monitor</span></span>
- <span data-ttu-id="d1720-1929">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d1720-1929">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="d1720-1930">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d1720-1930">Az.KeyVault</span></span>
- <span data-ttu-id="d1720-1931">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-1931">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="d1720-1932">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d1720-1932">Az.MachineLearning</span></span>
- <span data-ttu-id="d1720-1933">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="d1720-1933">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="d1720-1934">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d1720-1934">Az.Media</span></span>
- <span data-ttu-id="d1720-1935">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="d1720-1935">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d1720-1936">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-1936">Az.Network</span></span>
<span data-ttu-id="d1720-1937">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="d1720-1937">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="d1720-1938">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d1720-1938">New cmdlets added:</span></span>
        - <span data-ttu-id="d1720-1939">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d1720-1939">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d1720-1940">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d1720-1940">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d1720-1941">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d1720-1941">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d1720-1942">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d1720-1942">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d1720-1943">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d1720-1943">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d1720-1944">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d1720-1944">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="d1720-1945">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d1720-1945">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="d1720-1946">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1720-1946">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="d1720-1947">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d1720-1947">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="d1720-1948">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1720-1948">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="d1720-1949">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d1720-1949">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d1720-1950">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d1720-1950">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d1720-1951">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-1951">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="d1720-1952">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-1952">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="d1720-1953">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d1720-1953">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="d1720-1954">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d1720-1954">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="d1720-1955">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d1720-1955">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d1720-1956">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d1720-1956">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d1720-1957">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d1720-1957">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="d1720-1958">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="d1720-1958">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="d1720-1959">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d1720-1959">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="d1720-1960">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d1720-1960">Az.OperationalInsights</span></span>
- <span data-ttu-id="d1720-1961">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d1720-1961">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="d1720-1962">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d1720-1962">Az.Profile</span></span>
- <span data-ttu-id="d1720-1963">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d1720-1963">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-1964">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1964">Az.RecoveryServices</span></span>
- <span data-ttu-id="d1720-1965">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d1720-1965">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="d1720-1966">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-1966">Az.Resources</span></span>
- <span data-ttu-id="d1720-1967">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d1720-1967">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d1720-1968">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d1720-1968">Az.ServiceFabric</span></span>
- <span data-ttu-id="d1720-1969">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="d1720-1969">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="d1720-1970">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d1720-1970">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="d1720-1971">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d1720-1971">Az.SIgnalR</span></span>
- <span data-ttu-id="d1720-1972">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="d1720-1972">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="d1720-1973">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1973">Az.Sql</span></span>
- <span data-ttu-id="d1720-1974">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="d1720-1974">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="d1720-1975">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="d1720-1975">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="d1720-1976">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d1720-1976">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="d1720-1977">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-1977">Az.Storage</span></span>
- <span data-ttu-id="d1720-1978">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d1720-1978">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d1720-1979">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-1979">Az.Websites</span></span>
- <span data-ttu-id="d1720-1980">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d1720-1980">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="d1720-1981">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="d1720-1981">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="d1720-1982">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d1720-1982">General</span></span>

* <span data-ttu-id="d1720-1983">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1983">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="d1720-1984">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-1984">Az.Compute</span></span>

* <span data-ttu-id="d1720-1985">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="d1720-1985">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d1720-1986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1720-1986">Az.DataLakeStore</span></span>

* <span data-ttu-id="d1720-1987">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="d1720-1987">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="d1720-1988">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d1720-1988">Az.FrontDoor</span></span>

* <span data-ttu-id="d1720-1989">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1989">Fixed some broken links</span></span>
    - <span data-ttu-id="d1720-1990">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="d1720-1990">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="d1720-1991">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="d1720-1991">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d1720-1992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d1720-1992">Az.RecoveryServices</span></span>

* <span data-ttu-id="d1720-1993">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="d1720-1993">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="d1720-1994">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="d1720-1994">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="d1720-1995">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-1995">Az.Resources</span></span>

* <span data-ttu-id="d1720-1996">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="d1720-1996">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="d1720-1997">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="d1720-1997">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="d1720-1998">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-1998">Az.Sql</span></span>

* <span data-ttu-id="d1720-1999">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="d1720-1999">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="d1720-2000">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="d1720-2000">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="d1720-2001">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="d1720-2001">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="d1720-2002">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-2002">Az.Storage</span></span>

* <span data-ttu-id="d1720-2003">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-2003">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="d1720-2004">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="d1720-2004">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="d1720-2005">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d1720-2005">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d1720-2006">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="d1720-2006">Support Static Website configuration</span></span>
    - <span data-ttu-id="d1720-2007">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d1720-2007">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="d1720-2008">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d1720-2008">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d1720-2009">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-2009">Az.Websites</span></span>

* <span data-ttu-id="d1720-2010">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d1720-2010">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="d1720-2011">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="d1720-2011">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="d1720-2012">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="d1720-2012">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="d1720-2013">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="d1720-2013">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d1720-2014">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d1720-2014">Az.ApiManagement</span></span>
* <span data-ttu-id="d1720-2015">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="d1720-2015">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="d1720-2016">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d1720-2016">Az.Automation</span></span>
* <span data-ttu-id="d1720-2017">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="d1720-2017">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="d1720-2018">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="d1720-2018">Added Update Management cmdlets</span></span>
* <span data-ttu-id="d1720-2019">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="d1720-2019">Added Source Control cmdlets</span></span>
* <span data-ttu-id="d1720-2020">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="d1720-2020">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="d1720-2021">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="d1720-2021">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="d1720-2022">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-2022">Az.Compute</span></span>
* <span data-ttu-id="d1720-2023">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="d1720-2023">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="d1720-2024">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="d1720-2024">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d1720-2025">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d1720-2025">Az.ContainerInstance</span></span>
* <span data-ttu-id="d1720-2026">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="d1720-2026">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="d1720-2027">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d1720-2027">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d1720-2028">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="d1720-2028">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d1720-2029">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-2029">Az.Network</span></span>
* <span data-ttu-id="d1720-2030">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="d1720-2030">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="d1720-2031">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="d1720-2031">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="d1720-2032">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="d1720-2032">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="d1720-2033">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="d1720-2033">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="d1720-2034">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d1720-2034">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d1720-2035">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="d1720-2035">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="d1720-2036">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="d1720-2036">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="d1720-2037">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d1720-2037">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="d1720-2038">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="d1720-2038">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="d1720-2039">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="d1720-2039">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="d1720-2040">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d1720-2040">Az.Relay</span></span>
* <span data-ttu-id="d1720-2041">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="d1720-2041">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="d1720-2042">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-2042">Az.Resources</span></span>
* <span data-ttu-id="d1720-2043">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="d1720-2043">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="d1720-2044">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="d1720-2044">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="d1720-2045">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="d1720-2045">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d1720-2046">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d1720-2046">Az.ServiceFabric</span></span>
* <span data-ttu-id="d1720-2047">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-2047">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="d1720-2048">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-2048">Az.Sql</span></span>
* <span data-ttu-id="d1720-2049">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="d1720-2049">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="d1720-2050">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d1720-2050">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d1720-2051">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d1720-2051">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d1720-2052">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d1720-2052">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d1720-2053">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d1720-2053">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d1720-2054">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d1720-2054">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d1720-2055">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d1720-2055">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d1720-2056">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d1720-2056">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d1720-2057">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d1720-2057">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="d1720-2058">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="d1720-2058">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="d1720-2059">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="d1720-2059">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="d1720-2060">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="d1720-2060">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="d1720-2061">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d1720-2061">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d1720-2062">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d1720-2062">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d1720-2063">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d1720-2063">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="d1720-2064">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d1720-2064">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="d1720-2065">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="d1720-2065">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="d1720-2066">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="d1720-2066">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d1720-2067">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d1720-2067">General</span></span>
* <span data-ttu-id="d1720-2068">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="d1720-2068">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="d1720-2069">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d1720-2069">Az.Profile</span></span>
* <span data-ttu-id="d1720-2070">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="d1720-2070">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="d1720-2071">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="d1720-2071">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="d1720-2072">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="d1720-2072">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="d1720-2073">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="d1720-2073">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="d1720-2074">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="d1720-2074">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="d1720-2075">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="d1720-2075">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="d1720-2076">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="d1720-2076">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="d1720-2077">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d1720-2077">Az.CognitiveServices</span></span>
* <span data-ttu-id="d1720-2078">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="d1720-2078">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-2079">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-2079">Az.Compute</span></span>
* <span data-ttu-id="d1720-2080">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="d1720-2080">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="d1720-2081">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="d1720-2081">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="d1720-2082">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="d1720-2082">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d1720-2083">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1720-2083">Az.DataLakeStore</span></span>
* <span data-ttu-id="d1720-2084">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="d1720-2084">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="d1720-2085">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="d1720-2085">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="d1720-2086">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="d1720-2086">Az.Insights</span></span>
* <span data-ttu-id="d1720-2087">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="d1720-2087">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="d1720-2088">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="d1720-2088">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="d1720-2089">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="d1720-2089">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="d1720-2090">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="d1720-2090">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-2091">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-2091">Az.Network</span></span>
* <span data-ttu-id="d1720-2092">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="d1720-2092">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="d1720-2093">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1720-2093">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="d1720-2094">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d1720-2094">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="d1720-2095">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d1720-2095">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="d1720-2096">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d1720-2096">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d1720-2097">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1720-2097">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d1720-2098">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d1720-2098">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d1720-2099">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d1720-2099">Az.PolicyInsights</span></span>
* <span data-ttu-id="d1720-2100">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-2100">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-2101">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-2101">Az.Resources</span></span>
* <span data-ttu-id="d1720-2102">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="d1720-2102">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="d1720-2103">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="d1720-2103">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d1720-2104">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d1720-2104">Az.ServiceBus</span></span>
* <span data-ttu-id="d1720-2105">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="d1720-2105">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d1720-2106">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d1720-2106">Az.ServiceFabric</span></span>
* <span data-ttu-id="d1720-2107">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="d1720-2107">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="d1720-2108">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="d1720-2108">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="d1720-2109">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="d1720-2109">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="d1720-2110">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="d1720-2110">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="d1720-2111">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="d1720-2111">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="d1720-2112">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="d1720-2112">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="d1720-2113">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d1720-2113">Az.Profile</span></span>
* <span data-ttu-id="d1720-2114">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="d1720-2114">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="d1720-2115">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="d1720-2115">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-2116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-2116">Az.Compute</span></span>
* <span data-ttu-id="d1720-2117">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="d1720-2117">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="d1720-2118">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="d1720-2118">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d1720-2119">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d1720-2119">Az.DataLakeStore</span></span>
* <span data-ttu-id="d1720-2120">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="d1720-2120">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="d1720-2121">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="d1720-2121">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="d1720-2122">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="d1720-2122">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d1720-2123">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="d1720-2123">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d1720-2124">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="d1720-2124">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-2125">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-2125">Az.Network</span></span>
* <span data-ttu-id="d1720-2126">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="d1720-2126">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="d1720-2127">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="d1720-2127">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-2128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-2128">Az.Resources</span></span>
* <span data-ttu-id="d1720-2129">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="d1720-2129">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="d1720-2130">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="d1720-2130">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="d1720-2131">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="d1720-2131">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="d1720-2132">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="d1720-2132">Azure.Storage</span></span>
* <span data-ttu-id="d1720-2133">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="d1720-2133">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="d1720-2134">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d1720-2134">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="d1720-2135">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d1720-2135">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d1720-2136">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="d1720-2136">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="d1720-2137">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="d1720-2137">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d1720-2138">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d1720-2138">Az.CognitiveServices</span></span>
* <span data-ttu-id="d1720-2139">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="d1720-2139">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d1720-2140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d1720-2140">Az.Compute</span></span>
* <span data-ttu-id="d1720-2141">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="d1720-2141">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="d1720-2142">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="d1720-2142">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="d1720-2143">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="d1720-2143">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="d1720-2144">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d1720-2144">Az.DataFactoryV2</span></span>
* <span data-ttu-id="d1720-2145">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="d1720-2145">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d1720-2146">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d1720-2146">Az.Network</span></span>
* <span data-ttu-id="d1720-2147">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="d1720-2147">Added NetworkProfile functionality.</span></span> <span data-ttu-id="d1720-2148">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d1720-2148">new cmdlets added</span></span>
    - <span data-ttu-id="d1720-2149">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d1720-2149">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="d1720-2150">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d1720-2150">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="d1720-2151">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d1720-2151">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="d1720-2152">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d1720-2152">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="d1720-2153">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-2153">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="d1720-2154">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d1720-2154">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="d1720-2155">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="d1720-2155">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="d1720-2156">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="d1720-2156">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="d1720-2157">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="d1720-2157">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d1720-2158">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d1720-2158">Az.RedisCache</span></span>
* <span data-ttu-id="d1720-2159">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="d1720-2159">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="d1720-2160">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="d1720-2160">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="d1720-2161">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d1720-2161">Az.Resources</span></span>
* <span data-ttu-id="d1720-2162">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d1720-2162">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d1720-2163">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="d1720-2163">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="d1720-2164">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d1720-2164">Az.Sql</span></span>
* <span data-ttu-id="d1720-2165">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="d1720-2165">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d1720-2166">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d1720-2166">Az.Websites</span></span>
* <span data-ttu-id="d1720-2167">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="d1720-2167">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="d1720-2168">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="d1720-2168">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="d1720-2169">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="d1720-2169">0.2.0 - September 2018</span></span>
 <span data-ttu-id="d1720-2170">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="d1720-2170">Initial Release</span></span>
