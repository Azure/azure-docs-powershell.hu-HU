---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ab367ed41c77629122d6a4a9a79b96c7c66d09cb
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427581"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="8fe76-103">Az Azure PowerShell kibocsátási megjegyzései</span><span class="sxs-lookup"><span data-stu-id="8fe76-103">Azure PowerShell release notes</span></span>
## <a name="0100-preview---april-2020"></a><span data-ttu-id="8fe76-104">0.10.0-s előzetes verzió – 2020. április</span><span class="sxs-lookup"><span data-stu-id="8fe76-104">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="8fe76-105">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="8fe76-105">General</span></span>
* <span data-ttu-id="8fe76-106">Az Az modulok előzetes verziója mostantól elérhető az Azure Stack Hubon.</span><span class="sxs-lookup"><span data-stu-id="8fe76-106">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="8fe76-107">Ez lehetővé teszi a platformok közötti kompatibilitást a Linux és a macOs rendszerekkel.</span><span class="sxs-lookup"><span data-stu-id="8fe76-107">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="8fe76-108">A Azure Stack Hub mostantól támogatja a PowerShell Core-t az Az modulokkal, további információt [itt](/azure-stack/operator/powershell-install-az-module) talál</span><span class="sxs-lookup"><span data-stu-id="8fe76-108">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="8fe76-109">Az Az modulok támogatják a 2019-03-01-hybrid profilt:</span><span class="sxs-lookup"><span data-stu-id="8fe76-109">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="8fe76-110">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8fe76-110">Az.Billing</span></span>
  - <span data-ttu-id="8fe76-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-111">Az.Compute</span></span>
  - <span data-ttu-id="8fe76-112">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="8fe76-112">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="8fe76-113">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-113">Az.EventHub</span></span>
  - <span data-ttu-id="8fe76-114">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-114">Az.IotHub</span></span>
  - <span data-ttu-id="8fe76-115">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8fe76-115">Az.KeyVault</span></span>
  - <span data-ttu-id="8fe76-116">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8fe76-116">Az.Monitor</span></span>
  - <span data-ttu-id="8fe76-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-117">Az.Network</span></span>
  - <span data-ttu-id="8fe76-118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-118">Az.Resources</span></span>
  - <span data-ttu-id="8fe76-119">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-119">Az.Storage</span></span>
  - <span data-ttu-id="8fe76-120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-120">Az.Websites</span></span>
* <span data-ttu-id="8fe76-121">A következő három új PowerShell-modul lett bevezetve, amelyek használhatók az Azure Stack Hubbal: Az.Databox, Az.IotHub és Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-121">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="8fe76-122">A parancsok viszonylag változatlanok maradnak, kisebb módosításokkal. Például az Az helyébe az AzureRM lép.</span><span class="sxs-lookup"><span data-stu-id="8fe76-122">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="8fe76-123">Az Azure Stack Hubhoz kapcsolódó PowerShell-dokumentáció frissített hivatkozását [itt](/azure-stack/operator/powershell-install-az-module) találja</span><span class="sxs-lookup"><span data-stu-id="8fe76-123">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8fe76-124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-124">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-125">Frissítés ADAL-ról MSAL-re</span><span class="sxs-lookup"><span data-stu-id="8fe76-125">Upgrade from ADAL to MSAL</span></span>


## <a name="370---march-2020"></a><span data-ttu-id="8fe76-126">3.7.0 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="8fe76-126">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8fe76-127">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-127">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-128">Ki lett javítva az a hiba, hogy a Get-AzTenant/Get-AzDefault/Set-AzDefault parancs NullReferenceException hibát ad vissza kijelentkezett állapotban [#10292]</span><span class="sxs-lookup"><span data-stu-id="8fe76-128">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-129">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-129">Az.Compute</span></span>
* <span data-ttu-id="8fe76-130">A következő paraméterek lettek hozzáadva a New-AzDiskConfig parancsmaghoz:</span><span class="sxs-lookup"><span data-stu-id="8fe76-130">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="8fe76-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="8fe76-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="8fe76-132">Engedélyezve lett a New-AzGalleryImageVersion parancsmag célparaméterének titkosítási tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="8fe76-132">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="8fe76-133">Ki lett javítva a tempDisk hibája a Set-AzVmss -Reimage és az Invoke-AzVMReimage parancsmag esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-133">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="8fe76-134">[#11354]</span><span class="sxs-lookup"><span data-stu-id="8fe76-134">[#11354]</span></span>
* <span data-ttu-id="8fe76-135">Az alábbi parancsmagok mostantól támogatottak az új SAP-bővítmény esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-135">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="8fe76-136">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8fe76-136">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="8fe76-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8fe76-137">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="8fe76-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8fe76-138">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="8fe76-139">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="8fe76-139">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="8fe76-140">Ki lettek javítva a súgódokumentáció példáinak hibái</span><span class="sxs-lookup"><span data-stu-id="8fe76-140">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="8fe76-141">Táblázatos formátumban jelenítette meg a sztring pontos értékét a PowerState virtuális gép esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-141">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="8fe76-142">New-AzVmssConfig: ki lett javítva az AutomaticRepairs tulajdonság szerializálása a SinglePlacementGroup letiltott állapota esetén.</span><span class="sxs-lookup"><span data-stu-id="8fe76-142">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="8fe76-143">[#11257]</span><span class="sxs-lookup"><span data-stu-id="8fe76-143">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8fe76-144">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fe76-144">Az.DataFactory</span></span>
* <span data-ttu-id="8fe76-145">Az ADF .Net SDK a 4.8.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="8fe76-145">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="8fe76-146">Opcionális paraméterek lettek hozzáadva az Invoke-AzDataFactoryV2Pipeline parancshoz az újrafuttatás támogatásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-146">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8fe76-147">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8fe76-147">Az.DataLakeStore</span></span>
* <span data-ttu-id="8fe76-148">Hozzá lett adva a kompatibilitástörő változás leírása az Export-AzDataLakeStoreItem és az Import-AzDataLakeStoreItem parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-148">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="8fe76-149">A bájtkódolási lehetőség hozzá lett adva a New-AzDataLakeStoreItem, az Add-AzDAtaLakeStoreItemContent és a Get-AzDAtaLakeStoreItemContent parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-149">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8fe76-150">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8fe76-150">Az.HDInsight</span></span>
* <span data-ttu-id="8fe76-151">Fürt létrehozásakor a minimálisan támogatott TLS-verzió megadása támogatott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-151">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8fe76-152">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-152">Az.IotHub</span></span>
* <span data-ttu-id="8fe76-153">Hozzá lett adva az elosztott beállítások eszközönkénti felügyeletének támogatása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-153">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="8fe76-154">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="8fe76-154">New Cmdlets are:</span></span>
    - <span data-ttu-id="8fe76-155">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="8fe76-155">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="8fe76-156">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="8fe76-156">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8fe76-157">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8fe76-157">Az.KeyVault</span></span>
* <span data-ttu-id="8fe76-158">Kompatibilitástörő változást okozó attribútumok lettek hozzáadva a New-AzKeyVault parancshoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-158">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8fe76-159">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8fe76-159">Az.Monitor</span></span>
* <span data-ttu-id="8fe76-160">Frissült a New-AzScheduledQueryRuleLogMetricTrigger dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8fe76-160">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-161">Az.Network</span></span>
* <span data-ttu-id="8fe76-162">Frissültek a parancsmagok a több-bérlős VirtualHubVnetConnections engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-162">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="8fe76-163">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-163">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="8fe76-164">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-164">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="8fe76-165">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-165">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="8fe76-166">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-166">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="8fe76-167">Az SQL Management SDK-függőség el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8fe76-167">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8fe76-168">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8fe76-168">Az.PolicyInsights</span></span>
* <span data-ttu-id="8fe76-169">Továbbfejlesztett hibaüzenetek</span><span class="sxs-lookup"><span data-stu-id="8fe76-169">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-170">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-171">Hozzá lett adva az Azure Site Recovery-támogatás az Azure Diskkel titkosított virtuális gépek védelmének újbóli beállítása és frissített virtuálisgép-tulajdonságai esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-171">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="8fe76-172">Hozzá lett adva az Azure Site Recovery VmwareToAzure tulajdonságainak vészhelyreállítási monitorozása</span><span class="sxs-lookup"><span data-stu-id="8fe76-172">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="8fe76-173">Hozzá lett adva az Azure Backup-támogatás a sikertelen elemekre vonatkozó szabályzatfrissítés újbóli végrehajtása esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-173">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="8fe76-174">Hozzá lett adva az Azure Backup-támogatás a lemezkizárási beállításokhoz a biztonsági mentés és a visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="8fe76-174">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="8fe76-175">Hozzá lett adva az Azure Backup-támogatás több fájl/mappa visszaállításához az AzureFileShare-ben</span><span class="sxs-lookup"><span data-stu-id="8fe76-175">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="8fe76-176">Hozzá lett adva az Azure Backup-támogatás a felhasználó által megadott erőforráscsoport támogatásához az IaasVM-szabályzat frissítésekor</span><span class="sxs-lookup"><span data-stu-id="8fe76-176">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-177">Az.Resources</span></span>
* <span data-ttu-id="8fe76-178">Ki lett javítva a Get-AzResource-ResourceGroupName-Name-ExpandProperties-ResourceType parancs, hogy ezentúl az erőforrások aktuális API-verzióját használja az alapértelmezett verzió helyett [#11267]</span><span class="sxs-lookup"><span data-stu-id="8fe76-178">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="8fe76-179">Hozzá lett adva a CorrelationId-naplózás a hibaforgatókönyvek esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-179">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="8fe76-180">A Get-AzResourceLock dokumentációjában kisebb módosítás történt.</span><span class="sxs-lookup"><span data-stu-id="8fe76-180">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="8fe76-181">Példa hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-181">Added example.</span></span>
* <span data-ttu-id="8fe76-182">A szimpla idézőjel fel lett oldva a Get-AzADUser paraméterértékében [#11317]</span><span class="sxs-lookup"><span data-stu-id="8fe76-182">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="8fe76-183">Új parancsmagok lettek hozzáadva az üzembehelyezési szkriptekhez (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript)</span><span class="sxs-lookup"><span data-stu-id="8fe76-183">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-184">Az.Sql</span></span>
* <span data-ttu-id="8fe76-185">Olvasható másodlagos paraméter lett hozzáadva az Invoke-AzSqlDatabaseFailover parancshoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-185">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="8fe76-186">A Disable-AzSqlServerActiveDirectoryOnlyAuthentication parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="8fe76-186">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="8fe76-187">Az érzékenységi besorolás mentése megtörténik az adatbázis oszlopainak osztályozásakor.</span><span class="sxs-lookup"><span data-stu-id="8fe76-187">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="8fe76-188">Az.Support</span><span class="sxs-lookup"><span data-stu-id="8fe76-188">Az.Support</span></span>
* <span data-ttu-id="8fe76-189">Az Az.Support modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="8fe76-189">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-190">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-190">Az.Websites</span></span>
* <span data-ttu-id="8fe76-191">Mostantól támogatott a webalkalmazások forgalom-útválasztási szabályainak az alábbi új parancsmagokkal történő használata</span><span class="sxs-lookup"><span data-stu-id="8fe76-191">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="8fe76-192">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="8fe76-192">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="8fe76-193">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="8fe76-193">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="8fe76-194">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="8fe76-194">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="8fe76-195">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="8fe76-195">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="8fe76-196">3.6.1 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="8fe76-196">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8fe76-197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-197">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-198">Azure PowerShell felmérési oldal megnyitása itt: Send-Feedback [#11020]</span><span class="sxs-lookup"><span data-stu-id="8fe76-198">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="8fe76-199">Azure PowerShell-felmérés URL-címének megjelenítése itt: Resolve-Error [#11021]</span><span class="sxs-lookup"><span data-stu-id="8fe76-199">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="8fe76-200">Az-verzió hozzáadva az UserAgenthez</span><span class="sxs-lookup"><span data-stu-id="8fe76-200">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8fe76-201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8fe76-201">Az.ApiManagement</span></span>
* <span data-ttu-id="8fe76-202">Mostantól támogatott az egyéni tartomány lekérése és konfigurálása a DeveloperPortal végpontján [#11007]</span><span class="sxs-lookup"><span data-stu-id="8fe76-202">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="8fe76-203">Export-AzApiManagementAPi – Mostantól támogatott az Api-definíció Json formátumban való letöltése [#9987]</span><span class="sxs-lookup"><span data-stu-id="8fe76-203">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="8fe76-204">Import-AzApiManagementApi – Az OpenAPI 3.0-definíció Json-dokumentumokból való importálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-204">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="8fe76-205">New-AzApiManagementIdentityProvider és Set-AzApiManagementIdentityProvider – A Signin Tenant konfigurálása az AAD B2C-szolgáltató esetében mostantól támogatott. [#9784]</span><span class="sxs-lookup"><span data-stu-id="8fe76-205">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8fe76-206">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8fe76-206">Az.DataLakeStore</span></span>
* <span data-ttu-id="8fe76-207">A System.Buffershez hivatkozásának explicit hozzáadása a következőkben: csproj és psd1</span><span class="sxs-lookup"><span data-stu-id="8fe76-207">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8fe76-208">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-208">Az.IotHub</span></span>
* <span data-ttu-id="8fe76-209">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-209">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="8fe76-210">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="8fe76-210">New Cmdlets are:</span></span>
    - <span data-ttu-id="8fe76-211">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8fe76-211">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8fe76-212">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8fe76-212">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8fe76-213">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8fe76-213">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8fe76-214">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8fe76-214">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="8fe76-215">A cél IoT-eszközökön lévő modulok IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-215">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="8fe76-216">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="8fe76-216">New Cmdlets are:</span></span>
    - <span data-ttu-id="8fe76-217">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="8fe76-217">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="8fe76-218">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="8fe76-218">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="8fe76-219">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="8fe76-219">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="8fe76-220">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="8fe76-220">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="8fe76-221">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-221">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="8fe76-222">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz modulja kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-222">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="8fe76-223">Az IoT-eszközök szülő eszközének lekérése/beállítása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-223">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="8fe76-224">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="8fe76-224">New Cmdlets are:</span></span>
    - <span data-ttu-id="8fe76-225">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="8fe76-225">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="8fe76-226">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8fe76-226">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="8fe76-227">Az eszközök szülő-gyermek kapcsolatainak kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-227">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8fe76-228">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8fe76-228">Az.Monitor</span></span>
* <span data-ttu-id="8fe76-229">A Get-AzMetricDefinition kimeneti értéke javítva [#9714]</span><span class="sxs-lookup"><span data-stu-id="8fe76-229">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-230">Az.Network</span></span>
* <span data-ttu-id="8fe76-231">SQL Management SDK frissítve.</span><span class="sxs-lookup"><span data-stu-id="8fe76-231">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="8fe76-232">Kijavítottuk a PrivateLinkServiceConnectionState osztály eltérő elnevezéssel kapcsolatos hibáját.</span><span class="sxs-lookup"><span data-stu-id="8fe76-232">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="8fe76-233">Az ActionsRequired mező leképezése a követezőre: ActionRequired</span><span class="sxs-lookup"><span data-stu-id="8fe76-233">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="8fe76-234">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="8fe76-234">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-235">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-235">Az.Resources</span></span>
* <span data-ttu-id="8fe76-236">A Get-AzRoleAssignment null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="8fe76-236">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="8fe76-237">A -Force és a -PassThru kapcsoló nem kötelezőként lett megjelölve a Remove-AzADGroup esetében [#10849]</span><span class="sxs-lookup"><span data-stu-id="8fe76-237">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="8fe76-238">Javítva a hiba, amely miatt a MailNickname nem lett visszaadva Remove-AzADGroup esetében [#11167]</span><span class="sxs-lookup"><span data-stu-id="8fe76-238">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="8fe76-239">A Remove-AzADGroup folyamatművelet működési hibája kijavítva [#11171]</span><span class="sxs-lookup"><span data-stu-id="8fe76-239">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="8fe76-240">A GetAzureRoleAssignmentCommand null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="8fe76-240">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="8fe76-241">Kompatibilitástörő változás hozzáadva a szabályzati parancsmagok soron következő változásaihoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-241">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="8fe76-242">Frissült a Get-AzResourceGroup az erőforráscsoport-címke kiszolgálóoldali szűrésének elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-242">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="8fe76-243">A címkeparancsmagok kiterjesztése a -ResourceID elfogadása érdekében</span><span class="sxs-lookup"><span data-stu-id="8fe76-243">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="8fe76-244">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fe76-244">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="8fe76-245">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fe76-245">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="8fe76-246">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fe76-246">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="8fe76-247">Új címkeparancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-247">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="8fe76-248">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fe76-248">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="8fe76-249">A ScopedDeployment áthozva az SDK 3.3.0-ból</span><span class="sxs-lookup"><span data-stu-id="8fe76-249">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-250">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-250">Az.Sql</span></span>
* <span data-ttu-id="8fe76-251">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="8fe76-251">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="8fe76-252">Támogatás hozzáadva a biztonsági másolatok hosszú távú megőrzési konfigurációjához a felügyelt adatbázisok esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-252">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="8fe76-253">LTR-szabályzat lekérése/beállítása felügyelt adatbázison</span><span class="sxs-lookup"><span data-stu-id="8fe76-253">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="8fe76-254">LTR biztonsági másolat(ok) lekérése felügyelt adatbázis, felügyelt példány vagy hely szerint</span><span class="sxs-lookup"><span data-stu-id="8fe76-254">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="8fe76-255">LTR biztonsági másolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-255">Remove an LTR backup</span></span>
    - <span data-ttu-id="8fe76-256">LTR biztonsági másolat visszaállítása új felügyelt adatbázis létrehozásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-256">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="8fe76-257">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="8fe76-257">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="8fe76-258">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlInstance és Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8fe76-258">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="8fe76-259">Az SQL SDK-verzió felléptetése a következőhöz: AZ.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-259">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-260">Az.Storage</span></span>
* <span data-ttu-id="8fe76-261">Támogatott AllowProtectedAppendWrite a következőben: ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8fe76-261">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="8fe76-262">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8fe76-262">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="8fe76-263">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet az AzureStorageTable típusának módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="8fe76-263">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="8fe76-264">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="8fe76-264">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="8fe76-265">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="8fe76-265">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-266">Az.Websites</span></span>
* <span data-ttu-id="8fe76-267">Címke paraméter hozzáadva a következőkhöz: New-AzAppServicePlan és Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8fe76-267">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="8fe76-268">A parancsmag végrehajtásának leállítása, ha egy egyéni tartomány webhelyhez történő hozzáadásakor a rendszer kivételt ad vissza</span><span class="sxs-lookup"><span data-stu-id="8fe76-268">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="8fe76-269">Támogatás hozzáadva az olyan App Services műveletek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag</span><span class="sxs-lookup"><span data-stu-id="8fe76-269">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="8fe76-270">Hozzáférési korlátozás alkalmazva a különböző erőforráscsoportokban lévő webalkalmazásokra/függvényekre</span><span class="sxs-lookup"><span data-stu-id="8fe76-270">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="8fe76-271">Az egyéni WebAppSlots-gazdanevek beállítására vonatkozó hiba kijavítva</span><span class="sxs-lookup"><span data-stu-id="8fe76-271">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="8fe76-272">3.5.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="8fe76-272">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8fe76-273">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="8fe76-273">Highlights since the last major release</span></span>
* <span data-ttu-id="8fe76-274">Frissült az ügyféloldali telemetria.</span><span class="sxs-lookup"><span data-stu-id="8fe76-274">Updated client side telemetry.</span></span>
* <span data-ttu-id="8fe76-275">Az.IotHub: parancsmagok hozzáadva az eszközkezelés támogatásához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-275">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="8fe76-276">Az.SqlVirtualMachine: parancsmagok hozzáadva a rendelkezésreállási csoport figyelőjéhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-276">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8fe76-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-277">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-278">A SubscriptionId, a TenantId és a végrehajtási idő hozzáadva az ügyféloldali telemetria adataihoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-278">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8fe76-279">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8fe76-279">Az.Automation</span></span>
* <span data-ttu-id="8fe76-280">Ki lett javítva a „New-AzAutomationSoftwareUpdateConfiguration” referenciadokumentációjának 1. példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="8fe76-280">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8fe76-281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-281">Az.CognitiveServices</span></span>
* <span data-ttu-id="8fe76-282">Az SDK a 7.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="8fe76-282">Updated SDK to 7.0</span></span>
* <span data-ttu-id="8fe76-283">Tovább lett fejlesztve a hibaüzenet, amely akkor jelenik meg, ha a kiszolgáló üres törzset ad vissza válaszként</span><span class="sxs-lookup"><span data-stu-id="8fe76-283">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-284">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-284">Az.Compute</span></span>
* <span data-ttu-id="8fe76-285">A ProximityPlacementGroupId mostantól üres értékkel is rendelkezhet a frissítés során</span><span class="sxs-lookup"><span data-stu-id="8fe76-285">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8fe76-286">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8fe76-286">Az.FrontDoor</span></span>
* <span data-ttu-id="8fe76-287">Új parancsmag hozzáadva a WAF-ban használható felügyelt szabálydefiníciók lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-287">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8fe76-288">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-288">Az.IotHub</span></span>
* <span data-ttu-id="8fe76-289">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-289">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="8fe76-290">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="8fe76-290">New Cmdlets are:</span></span>
    - <span data-ttu-id="8fe76-291">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8fe76-291">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8fe76-292">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8fe76-292">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8fe76-293">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8fe76-293">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8fe76-294">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8fe76-294">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8fe76-295">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8fe76-295">Az.KeyVault</span></span>
* <span data-ttu-id="8fe76-296">Ki lett javítva az Add-AzKeyVaultKey.md duplikált szövege</span><span class="sxs-lookup"><span data-stu-id="8fe76-296">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8fe76-297">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8fe76-297">Az.Monitor</span></span>
* <span data-ttu-id="8fe76-298">Ki lett javítva a Get-AzLog parancsmag leírása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-298">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="8fe76-299">Egy új, ActionGroupId nevű paraméter lett hozzáadva a „New-AzMetricAlertRuleV2” parancshoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-299">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="8fe76-300">A felhasználó a következőket adhatja meg: ActionGroupId(string) vagy ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="8fe76-300">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-301">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-301">Az.Network</span></span>
* <span data-ttu-id="8fe76-302">Hozzá lett adva egy extra paramétermegjegyzés a „New-AzPrivateLinkService” parancsmag „-EnableProxyProtocol” paraméteréhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-302">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="8fe76-303">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-303">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="8fe76-304">Hozzá lett adva egy csomagrögzítési példa a Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és Start-AzVirtualnetworkGatewayPacketCapture.md minden belső és külső csomagjának rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-304">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="8fe76-305">Az Azure Firewall-szabályzat mostantól támogatott a Vnet-tűzfalakon</span><span class="sxs-lookup"><span data-stu-id="8fe76-305">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="8fe76-306">Nem lettek hozzáadva új parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="8fe76-306">No new cmdlets are added.</span></span> <span data-ttu-id="8fe76-307">Enyhítve lettek a tűzfalszabályzat korlátozásai a Vnet-tűzfalak esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-307">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-308">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-309">A fájlokként történő visszaállítás mostantól támogatott az SQL-adatbázisok esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-309">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-310">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-310">Az.Resources</span></span>
* <span data-ttu-id="8fe76-311">Újra lettek tervezve a sablonalapú üzembehelyezési parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8fe76-311">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="8fe76-312">Új parancsmagok lettek hozzáadva a felügyeleti csoportban való üzembe helyezés kezeléséhez: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8fe76-312">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="8fe76-313">Új parancsmagok lettek hozzáadva a bérlői hatókörben való üzembe helyezés kezeléséhez: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8fe76-313">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="8fe76-314">Az \*-AzDeployment parancsmagok kifejezetten az előfizetési hatókörben való működéshez lettek újratervezve</span><span class="sxs-lookup"><span data-stu-id="8fe76-314">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="8fe76-315">Az \*-AzSubscriptionDeployment aliasok lettek létrehozva az \*-AzDeployment parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-315">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="8fe76-316">Ki lett javítva az „Update-AzADApplication” nem beállított „AvailableToOtherTenants” paraméter esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-316">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="8fe76-317">Az ApplicationObjectWithoutCredentialParameterSet el lett távolítva az AmbiguousParameterSetException elkerülése érdekében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-317">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="8fe76-318">A súgófájlok újra létre lettek hozva</span><span class="sxs-lookup"><span data-stu-id="8fe76-318">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-319">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-319">Az.Sql</span></span>
* <span data-ttu-id="8fe76-320">Az előfizetések közötti időponthoz kötött visszaállítás mostantól támogatott a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="8fe76-320">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="8fe76-321">A már meglévő felügyelt SQL-példány hardvergenerációjának módosítása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="8fe76-321">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="8fe76-322">Ki lettek javítva az „Update-AzSqlServerVulnerabilityAssessmentSetting” súgópéldái: paraméter/tulajdonságkimenet – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="8fe76-322">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="8fe76-323">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8fe76-323">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="8fe76-324">Parancsmagokat hozzáadva a rendelkezésreállási csoport figyelőjéhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-324">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8fe76-325">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8fe76-325">Az.StorageSync</span></span>
* <span data-ttu-id="8fe76-326">Frissültek az „Invoke-AzStorageSyncCompatibilityCheck” támogatott karakterkészletei.</span><span class="sxs-lookup"><span data-stu-id="8fe76-326">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="8fe76-327">3.4.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="8fe76-327">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8fe76-328">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="8fe76-328">Highlights since the last major release</span></span>
* <span data-ttu-id="8fe76-329">Megjelent az Az.CosmosDB 0.1.0-s kezdeti verziója</span><span class="sxs-lookup"><span data-stu-id="8fe76-329">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="8fe76-330">Az.Network ConnectionMonitor V2 támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="8fe76-330">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8fe76-331">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-331">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-332">A környezet automatikus mentésének letiltása, ha az AzureRmContext.json nem érhető el</span><span class="sxs-lookup"><span data-stu-id="8fe76-332">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="8fe76-333">Az Azure Powershell Common referenciájának frissítése 1.3.5-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="8fe76-333">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8fe76-334">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8fe76-334">Az.ApiManagement</span></span>
* <span data-ttu-id="8fe76-335">**Get-AzApiManagementApiSchema** Az API-val társított Open-API séma kijavítása   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="8fe76-335">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="8fe76-336">**New-AzApiManagementProduct** _ és _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="8fe76-336">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="8fe76-337"> https://github.com/Azure/azure-powershell/issues/10472 dokumentációja kijavítva</span><span class="sxs-lookup"><span data-stu-id="8fe76-337">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="8fe76-338">**Set-AzApiManagementApi** A ServiceUrl parancsmaggal való frissítését bemutató példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-338">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-339">Az.Compute</span></span>
* <span data-ttu-id="8fe76-340">A virtuális gép állapotának korlátozása 100 értékre, hogy ne legyen szabályozás, ha a Get-AzVM -Status a virtuális gép neve nélkül lett végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-340">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="8fe76-341">Update-AzDiskEncryptionSet parancsmagok hozzáadása</span><span class="sxs-lookup"><span data-stu-id="8fe76-341">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="8fe76-342">Az EncryptionType és a DiskEncryptionSetId paraméterek hozzáadása a következő parancsmagokhoz:</span><span class="sxs-lookup"><span data-stu-id="8fe76-342">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="8fe76-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="8fe76-344">A ColocationStatus paraméter hozzáadva a Get-AzProximityPlacementGroup parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-344">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8fe76-345">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fe76-345">Az.DataFactory</span></span>
* <span data-ttu-id="8fe76-346">Az ADF .Net SDK frissítve lett a 4.7.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="8fe76-346">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="8fe76-347">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="8fe76-347">Az.DeploymentManager</span></span>
* <span data-ttu-id="8fe76-348">LIST műveletek hozzáadása az erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-348">Adds LIST operations for resources</span></span>
* <span data-ttu-id="8fe76-349">Műveletek végrehajtásának lehetősége az állapotellenőrzés lépésein</span><span class="sxs-lookup"><span data-stu-id="8fe76-349">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8fe76-350">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8fe76-350">Az.HDInsight</span></span>
* <span data-ttu-id="8fe76-351">A New-AzHDInsightCluster dokumentációs hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-351">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8fe76-352">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8fe76-352">Az.KeyVault</span></span>
* <span data-ttu-id="8fe76-353">Name alias hozzáadása a VaultName attribútumhoz, hogy a Remove-AzureKeyVault konzisztens legyen a New-AzureKeyVault paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="8fe76-353">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-354">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-354">Az.Network</span></span>
* <span data-ttu-id="8fe76-355">Új példa hozzáadva a Set-AzNetworkWatcherConfigFlowLog.md fájlhoz a Traffic Analytics-letiltási forgatókönyv szemléltetésére.</span><span class="sxs-lookup"><span data-stu-id="8fe76-355">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="8fe76-356">Felügyeleti IP-konfiguráció támogatás hozzáadva az Azure Firewallhoz – egy dedikált alhálózat és nyilvános IP-cím, amelyet a tűzfal a forgalom felügyeléséhez használni fog</span><span class="sxs-lookup"><span data-stu-id="8fe76-356">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="8fe76-357">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="8fe76-357">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="8fe76-358">Hozzá lett adva a (nem kötelező) -PublicIpAddress-ManagementPublicIpAddress paraméter, amely egy nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="8fe76-358">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="8fe76-359">Hozzá lett adva a SetManagementIpConfiguration metódus a tűzfalobjektumok esetében – nyilvános IP-cím-objektumokat fogad el bemeneti adatként – az alhálózat nevének AzureFirewallManagementSubnet értéknek kell lennie</span><span class="sxs-lookup"><span data-stu-id="8fe76-359">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="8fe76-360">A Get-AzNetworkSecurityGroup példái javítva, hogy hálózati biztonsági csoportok példáit tartalmazzák hálózati adapterek helyett.</span><span class="sxs-lookup"><span data-stu-id="8fe76-360">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="8fe76-361">Javítottunk egy elírást a New-AzVpnSite parancsban, amely megakadályozta, hogy az erőforrásazonosító-kiegészítő kiegészítsen egy paramétert.</span><span class="sxs-lookup"><span data-stu-id="8fe76-361">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="8fe76-362">Az Application Gateway szabály-újraírási műveletkészletének URL-konfigurálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-362">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="8fe76-363">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="8fe76-363">New cmdlets added:</span></span>
        - <span data-ttu-id="8fe76-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fe76-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="8fe76-365">A parancsmagok frissültek a nem kötelező UrlConfiguration paraméterrel</span><span class="sxs-lookup"><span data-stu-id="8fe76-365">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="8fe76-366">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8fe76-366">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="8fe76-367">A Network Watcher Connection Monitor 2-es verziójú erőforrások támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-367">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8fe76-368">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8fe76-368">Az.PolicyInsights</span></span>
* <span data-ttu-id="8fe76-369">A javítandó erőforrások azonosítása előtti megfelelőségértékelés támogatása</span><span class="sxs-lookup"><span data-stu-id="8fe76-369">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="8fe76-370">-ResourceDiscoverMode paraméter hozzáadása a Start-AzPolicyRemediation parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-370">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="8fe76-371">A szabályzatok metaadat-erőforrásainak elérésére szolgáló Get-AzPolicyMetadata parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="8fe76-371">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="8fe76-372">A Get-AzPolicyState és a Get-AzPolicyStateSummary frissült a 2019-10-01 API-verzióhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-372">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-373">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-373">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-374">Azure Site Recovery-támogatás a replikált lemezek eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-374">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="8fe76-375">Hozzáadott Azure Backup-támogatás a helyreállítási tárak létrehozása közbeni címkehozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-375">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-376">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-376">Az.Resources</span></span>
* <span data-ttu-id="8fe76-377">A -Scope választható a \*-AzPolicyAssignment parancsmagokban; az alapértelmezett érték a környezeti előfizetés</span><span class="sxs-lookup"><span data-stu-id="8fe76-377">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="8fe76-378">Az ADServicePrincipal jelszó és kulcs típusú hitelesítő adatokkal való létrehozását szemléltető példák hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-378">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-379">Az.Sql</span></span>
<span data-ttu-id="8fe76-380">A New-AzSqlDatabaseSecondary parancsmag javítva, hogy a PartnerDatabaseName létezését ellenőrizze a DatabaseName létezése helyett.</span><span class="sxs-lookup"><span data-stu-id="8fe76-380">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-381">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-381">Az.Storage</span></span>
* <span data-ttu-id="8fe76-382">A Table/Queue Encryption Keytype készlet beállításának támogatása Storage-fiók létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="8fe76-382">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="8fe76-383">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe76-383">New-AzStorageAccount</span></span>
* <span data-ttu-id="8fe76-384">RequestId megjelenítése, ha a StorageException nem rendelkezik ExtendedErrorInformation paraméterrel</span><span class="sxs-lookup"><span data-stu-id="8fe76-384">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="8fe76-385">A Start-AzStorageBlobCopy parancsmag 6. példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-385">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-386">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-386">Az.Websites</span></span>
* <span data-ttu-id="8fe76-387">A Set-AzWebapp és a Set-AzWebappSlot támogatja az AlwaysOn, a MinTls és a FtpsState tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="8fe76-387">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="8fe76-388">Javítva a hiba, amely miatt a HttpsOnly és az AppservicePlan Set-AzWebApp paranccsal történő egyidejű módosításakor a HttpsOnly paraméter alaphelyzetbe állt.</span><span class="sxs-lookup"><span data-stu-id="8fe76-388">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="8fe76-389">3.3.0 – 2020. január</span><span class="sxs-lookup"><span data-stu-id="8fe76-389">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8fe76-390">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-390">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-391">Frissítve lettek az Add-AzEnvironment és Set-AzEnvironment parancsmagok, amelyek mostantól elfogadják az AzureAttestationServiceEndpointResourceId és AzureAttestationServiceEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="8fe76-391">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8fe76-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8fe76-392">Az.Cdn</span></span>
* <span data-ttu-id="8fe76-393">A hibaválasz részleteinek láthatóvá tétele a New-AzCdnEndpoint parancsmagban</span><span class="sxs-lookup"><span data-stu-id="8fe76-393">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-394">Az.Compute</span></span>
* <span data-ttu-id="8fe76-395">Javítva lett a Set-AzVMCustomScriptExtension parancsmag az olyan virtuális gépek esetében, amelyek felügyelt operációsrendszer-lemeze nem rendelkezik operációsrendszer-profillal.</span><span class="sxs-lookup"><span data-stu-id="8fe76-395">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="8fe76-396">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8fe76-396">Az.ContainerInstance</span></span>
* <span data-ttu-id="8fe76-397">Javítva lettek a New-AzContainerGroup parancsmagpélda által használt paraméternevek</span><span class="sxs-lookup"><span data-stu-id="8fe76-397">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="8fe76-398">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="8fe76-398">Az.DataBoxEdge</span></span>
* <span data-ttu-id="8fe76-399">Hozzá lett adva a Get-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="8fe76-399">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8fe76-400">Az Edge Storage-tároló lekérése</span><span class="sxs-lookup"><span data-stu-id="8fe76-400">Get the Edge Storage Container</span></span>
* <span data-ttu-id="8fe76-401">Hozzá lett adva a New-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="8fe76-401">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8fe76-402">Új Edge Storage-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="8fe76-402">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="8fe76-403">Hozzá lett adva a Remove-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="8fe76-403">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8fe76-404">Az Edge Storage-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-404">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="8fe76-405">Hozzá lett adva az Invoke-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="8fe76-405">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8fe76-406">Meghívási művelet az Edge Storage-tárolóban lévő adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-406">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="8fe76-407">Hozzá lett adva a Get-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="8fe76-407">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="8fe76-408">Az Edge Storage-fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="8fe76-408">Get the Edge Storage Account</span></span>
* <span data-ttu-id="8fe76-409">Hozzá lett adva a New-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="8fe76-409">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="8fe76-410">Új Edge Storage-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="8fe76-410">Create new Edge Storage Account</span></span>
* <span data-ttu-id="8fe76-411">Hozzá lett adva a Remove-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="8fe76-411">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="8fe76-412">Az Edge Storage-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-412">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="8fe76-413">Hozzá lett adva az Invoke-AzDataBoxEdgeShare parancsmag</span><span class="sxs-lookup"><span data-stu-id="8fe76-413">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="8fe76-414">Meghívási művelet a megosztott adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-414">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="8fe76-415">Hozzá lett adva a Set-AzDataBoxEdgeStorageAccountCredential parancsmag</span><span class="sxs-lookup"><span data-stu-id="8fe76-415">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="8fe76-416">Az Az.DataBoxEdge tárfiók hitelesítő adatainak beállítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-416">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8fe76-417">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fe76-417">Az.DataFactory</span></span>
* <span data-ttu-id="8fe76-418">Hozzá lettek adva az AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId és VersionStatus tulajdonságok a Get-AzDataFactoryV2IntegrationRuntime parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-418">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="8fe76-419">Az ADF .Net SDK frissítve lett a 4.6.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="8fe76-419">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="8fe76-420">A PublicIPs paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz statikus nyilvános IP-címekkel rendelkező Azure-SSIS IR létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-420">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="8fe76-421">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="8fe76-421">Az.DevTestLabs</span></span>
* <span data-ttu-id="8fe76-422">A hibás hivatkozás el lett távolítva a Get-AzDtlAllowedVMSizesPolicy.md parancsmagból</span><span class="sxs-lookup"><span data-stu-id="8fe76-422">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8fe76-423">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-423">Az.EventHub</span></span>
* <span data-ttu-id="8fe76-424">A 10634-es hiba javítása: Ki lett javítva a nullértékű objektumhivatkozás a remove eventhubnamespace esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-424">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8fe76-425">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8fe76-425">Az.HDInsight</span></span>
* <span data-ttu-id="8fe76-426">Ki lett javítva az Invoke-AzHDInsightHiveJob.md hibája.</span><span class="sxs-lookup"><span data-stu-id="8fe76-426">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8fe76-427">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8fe76-427">Az.MachineLearning</span></span>
* <span data-ttu-id="8fe76-428">El lettek távolítva az alábbi parancsmagok, mivel a MachineLearningCompute már nem érhető el</span><span class="sxs-lookup"><span data-stu-id="8fe76-428">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="8fe76-429">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8fe76-429">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="8fe76-430">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="8fe76-430">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="8fe76-431">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8fe76-431">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="8fe76-432">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8fe76-432">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="8fe76-433">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8fe76-433">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="8fe76-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="8fe76-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="8fe76-435">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="8fe76-435">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-436">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-436">Az.Network</span></span>
* <span data-ttu-id="8fe76-437">Frissítve lett a Microsoft.Azure.Management.Sql függősége: 1.36-preview helyett 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="8fe76-437">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-439">Módosított Azure Site Recovery-támogatás azon felügyelt lemezeken található, inaktív állapotban titkosított virtuális gépeknél, amelyekhez felhasználó által kezelt kulcsok tartoznak a következő esetében: Azure – Azure-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="8fe76-439">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="8fe76-440">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a védelem engedélyezése során a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="8fe76-440">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="8fe76-441">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a lemez szintjén a védelem engedélyezéséhez a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="8fe76-441">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="8fe76-442">Azure Site Recovery-támogatás a Replikációval védett, lemeztitkosítási csoportleképezéssel ellátott elemek frissítéséhez a következő esetében: HyperV – Azure.</span><span class="sxs-lookup"><span data-stu-id="8fe76-442">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-443">Az.Resources</span></span>
* <span data-ttu-id="8fe76-444">Javítva lett egy hiba a Remove-AzTag súgódokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="8fe76-444">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-445">Az.Sql</span></span>
* <span data-ttu-id="8fe76-446">Javítva lett a sebezhetőségi felmérés csoportszintű alapkonfigurációs parancsmagjainak működése: az Azure-adatbázis főadatbázisában használható, a felügyelt példányok rendszeradatbázisaiban korlátozott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-446">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="8fe76-447">Ki lett javítva egy hiba az SQL-példányok feladatátvételi csoportjainak létrehozása esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-447">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="8fe76-448">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8fe76-448">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="8fe76-449">Hozzá lett adva a DR, mint új érvényes licenctípus</span><span class="sxs-lookup"><span data-stu-id="8fe76-449">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-450">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-450">Az.Storage</span></span>
* <span data-ttu-id="8fe76-451">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet a DefaultAction értékének módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="8fe76-451">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="8fe76-452">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fe76-452">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="8fe76-453">Támogatott a tárfiók legutóbbi szinkronizálási időpontjának lekérése a get-AzureRMStorageAccount parancsmag -IncludeGeoReplicationStats paraméterrel való futtatásával</span><span class="sxs-lookup"><span data-stu-id="8fe76-453">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="8fe76-454">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe76-454">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="8fe76-455">3.2.0 – 2019. december</span><span class="sxs-lookup"><span data-stu-id="8fe76-455">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="8fe76-456">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="8fe76-456">General</span></span>
* <span data-ttu-id="8fe76-457">A .psd1 hivatkozásai frissítve, hogy minden modulhoz a relatív elérési utat használják</span><span class="sxs-lookup"><span data-stu-id="8fe76-457">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8fe76-458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-458">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-459">A megfelelő felhasználói ügynök beállítva az ügyféloldali telemetriához az Az 4.0 előzetes verziójában</span><span class="sxs-lookup"><span data-stu-id="8fe76-459">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="8fe76-460">Felhasználóbarát hibaüzenet megjelenítése, ha az Az 4.0 előzetes verziójában a környezet null értékű</span><span class="sxs-lookup"><span data-stu-id="8fe76-460">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8fe76-461">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8fe76-461">Az.Batch</span></span>
* <span data-ttu-id="8fe76-462">Ki lett javítva a [10602-es](https://github.com/Azure/azure-powershell/issues/10602) számú hiba, amely miatt a **New-AzBatchPool** nem megfelelően küldte el a „VirtualMachineConfiguration.ContainerConfiguration” és a „VirtualMachineConfiguration.DataDisks” paramétereket a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="8fe76-462">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8fe76-463">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fe76-463">Az.DataFactory</span></span>
* <span data-ttu-id="8fe76-464">Az ADF .Net SDK a 4.5.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="8fe76-464">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8fe76-465">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8fe76-465">Az.FrontDoor</span></span>
* <span data-ttu-id="8fe76-466">A WAF felügyeleti szabályok kizárása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="8fe76-466">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="8fe76-467">Hozzá lett adva a SocketAddr automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="8fe76-467">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8fe76-468">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8fe76-468">Az.HealthcareApis</span></span>
* <span data-ttu-id="8fe76-469">Kivételkezelés</span><span class="sxs-lookup"><span data-stu-id="8fe76-469">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8fe76-470">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8fe76-470">Az.KeyVault</span></span>
* <span data-ttu-id="8fe76-471">Ki lett javítva az esetleg nem beállított értékek hozzáférésével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="8fe76-471">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="8fe76-472">Az elliptikus görbéjű titkosítási tanúsítványok kezelése</span><span class="sxs-lookup"><span data-stu-id="8fe76-472">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="8fe76-473">A görbe tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="8fe76-473">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8fe76-474">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8fe76-474">Az.Monitor</span></span>
* <span data-ttu-id="8fe76-475">Opcionális argumentum hozzáadva a Diagnosztikai beállítások hozzáadása parancshoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-475">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="8fe76-476">Ez egy kapcsoló argumentum, amely megléte esetén azt jelzi, hogy a Log Analyticsbe történő exportálást egy rögzített séma (más néven</span><span class="sxs-lookup"><span data-stu-id="8fe76-476">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="8fe76-477">dedikált adattípus) szerint kell végrehajtani</span><span class="sxs-lookup"><span data-stu-id="8fe76-477">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-478">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-478">Az.Network</span></span>
* <span data-ttu-id="8fe76-479">Támogatás az Ip-csoportok számára az AzureFirewall alkalmazás, valamint a Nat- és a hálózati szabályok esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-479">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-480">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-480">Az.Resources</span></span>
* <span data-ttu-id="8fe76-481">Ki lett javítva az a hiba, amely miatt a sablonalapú üzembe helyezés során a sablonparamétert nem lehet olvasni, ha a sablonparaméter és egy beépített paraméter neve között névütközés áll fenn.</span><span class="sxs-lookup"><span data-stu-id="8fe76-481">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="8fe76-482">Frissültek a szabályzat parancsmagjai a 2019. 09. 01. dátumú új API-verzió használatára, amely bevezeti a szabályzatkészlet-definíciókon belüli csoportos támogatást.</span><span class="sxs-lookup"><span data-stu-id="8fe76-482">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-483">Az.Sql</span></span>
* <span data-ttu-id="8fe76-484">Frissítve lett a sebezhetőségi felmérés automatikus engedélyezéséhez szükséges tárterület létrehozása a Storagev2-ben</span><span class="sxs-lookup"><span data-stu-id="8fe76-484">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-485">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-485">Az.Storage</span></span>
* <span data-ttu-id="8fe76-486">A blob-/tárolóidentitás-alapú SAS-token Oauth-hitelesítésen alapuló Storage-környezettel való létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="8fe76-486">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="8fe76-487">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="8fe76-487">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="8fe76-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8fe76-488">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="8fe76-489">Támogatott lett a tárfiókhoz tartozó felhasználódelegálási kulcsok visszavonása, így minden identitásalapú SAS-token visszavonható</span><span class="sxs-lookup"><span data-stu-id="8fe76-489">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="8fe76-490">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="8fe76-490">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="8fe76-491">Frissítés a Microsoft.Azure.Management.Storage 14.2.0-s verziójára az új API-verzió (2019. 06. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-491">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="8fe76-492">A QuotaGiB (gigabájtban megadott megosztási kvóta) esetében támogatottak az 5120-nál nagyobb értékek a fájlmegosztási parancsmagok felügyeleti síkján, és hozzá lett adva a Quota paraméteralias a QuotaGiB paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-492">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="8fe76-493">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8fe76-493">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="8fe76-494">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8fe76-494">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="8fe76-495">A „QuotaGiB” paraméteralias hozzáadva a „kvóta” paraméterhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-495">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="8fe76-496">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="8fe76-496">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="8fe76-497">Ki lett javítva az a hiba, amely miatt a Set-AzStorageContainerAcl parancsmag el tudta távolítani a tárolt hozzáférési szabályzatot</span><span class="sxs-lookup"><span data-stu-id="8fe76-497">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="8fe76-498">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="8fe76-498">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="8fe76-499">3.1.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="8fe76-499">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8fe76-500">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="8fe76-500">Highlights since the last major release</span></span>
* <span data-ttu-id="8fe76-501">Az.DataBoxEdge 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-501">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="8fe76-502">Az.SqlVirtualMachine 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-502">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-503">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-503">Az.Compute</span></span>
* <span data-ttu-id="8fe76-504">A virtuális gépek Reapply funkciója</span><span class="sxs-lookup"><span data-stu-id="8fe76-504">VM Reapply feature</span></span>
    - <span data-ttu-id="8fe76-505">A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-505">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="8fe76-506">A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:</span><span class="sxs-lookup"><span data-stu-id="8fe76-506">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="8fe76-507">Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8fe76-507">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="8fe76-508">Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-508">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="8fe76-509">A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-509">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="8fe76-510">A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-510">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="8fe76-511">A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező</span><span class="sxs-lookup"><span data-stu-id="8fe76-511">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="8fe76-512">A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="8fe76-512">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="8fe76-513">A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban</span><span class="sxs-lookup"><span data-stu-id="8fe76-513">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="8fe76-514">A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-514">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="8fe76-515">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="8fe76-515">Az.DataBoxEdge</span></span>
* <span data-ttu-id="8fe76-516">A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="8fe76-516">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8fe76-517">Megrendelés lekérése</span><span class="sxs-lookup"><span data-stu-id="8fe76-517">Get the Order</span></span>
* <span data-ttu-id="8fe76-518">A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="8fe76-518">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8fe76-519">Új megrendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="8fe76-519">Create new Order</span></span>
* <span data-ttu-id="8fe76-520">A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="8fe76-520">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8fe76-521">Megrendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-521">Remove the Order</span></span>
* <span data-ttu-id="8fe76-522">`New-AzDataBoxEdgeShare` parancsmag módosítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-522">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="8fe76-523">Mostantól helyi megosztást hoz létre</span><span class="sxs-lookup"><span data-stu-id="8fe76-523">Now creates Local Share</span></span>
* <span data-ttu-id="8fe76-524">A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="8fe76-524">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="8fe76-525">Mostantól az IotRole leképezhető a Share-re</span><span class="sxs-lookup"><span data-stu-id="8fe76-525">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="8fe76-526">A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="8fe76-526">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="8fe76-527">Frissítések keresésének, letöltésének, telepítésének indítása az eszközön</span><span class="sxs-lookup"><span data-stu-id="8fe76-527">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="8fe76-528">A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="8fe76-528">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8fe76-529">Triggerek információinak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="8fe76-529">Gets the information about Triggers</span></span>
* <span data-ttu-id="8fe76-530">A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="8fe76-530">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8fe76-531">Új triggerek létrehozása</span><span class="sxs-lookup"><span data-stu-id="8fe76-531">Create new Triggers</span></span>
* <span data-ttu-id="8fe76-532">A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="8fe76-532">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8fe76-533">Triggerek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-533">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8fe76-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fe76-534">Az.DataFactory</span></span>
* <span data-ttu-id="8fe76-535">Az ADF .Net SDK a 4.4.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="8fe76-535">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="8fe76-536">Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-536">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8fe76-537">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8fe76-537">Az.DataLakeStore</span></span>
* <span data-ttu-id="8fe76-538">Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8fe76-538">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8fe76-539">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-539">Az.EventHub</span></span>
* <span data-ttu-id="8fe76-540">A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-540">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8fe76-541">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8fe76-541">Az.FrontDoor</span></span>
* <span data-ttu-id="8fe76-542">Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="8fe76-542">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="8fe76-543">A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="8fe76-543">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="8fe76-544">Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-544">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="8fe76-545">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="8fe76-545">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-546">Az.Network</span></span>
* <span data-ttu-id="8fe76-547">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.</span><span class="sxs-lookup"><span data-stu-id="8fe76-547">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="8fe76-548">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="8fe76-548">Az.PrivateDns</span></span>
* <span data-ttu-id="8fe76-549">A PrivateDns .net sdk frissült az 1.0.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="8fe76-549">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-551">Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="8fe76-551">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="8fe76-552">Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-552">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="8fe76-553">SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-553">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8fe76-554">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8fe76-554">Az.RedisCache</span></span>
* <span data-ttu-id="8fe76-555">A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="8fe76-555">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="8fe76-556">Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-556">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="8fe76-557">Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-557">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-558">Az.Resources</span></span>
- <span data-ttu-id="8fe76-559">Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.</span><span class="sxs-lookup"><span data-stu-id="8fe76-559">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="8fe76-560">Frissült a létrehozási szabályzat definíciójának súgóbeli példája</span><span class="sxs-lookup"><span data-stu-id="8fe76-560">Updated create policy definition help example</span></span>
- <span data-ttu-id="8fe76-561">Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.</span><span class="sxs-lookup"><span data-stu-id="8fe76-561">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="8fe76-562">Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.</span><span class="sxs-lookup"><span data-stu-id="8fe76-562">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="8fe76-563">A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="8fe76-563">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-564">Az.Sql</span></span>
* <span data-ttu-id="8fe76-565">Az adatbázisbeli ReadReplicaCount mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-565">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="8fe76-566">A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén</span><span class="sxs-lookup"><span data-stu-id="8fe76-566">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="8fe76-567">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="8fe76-567">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="8fe76-568">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="8fe76-568">General</span></span>
* <span data-ttu-id="8fe76-569">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8fe76-569">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8fe76-570">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-570">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-571">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-571">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8fe76-572">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8fe76-572">Az.Advisor</span></span>
* <span data-ttu-id="8fe76-573">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-573">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8fe76-574">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8fe76-574">Az.Batch</span></span>
* <span data-ttu-id="8fe76-575">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="8fe76-575">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="8fe76-576">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="8fe76-576">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="8fe76-577">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="8fe76-577">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="8fe76-578">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="8fe76-578">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="8fe76-579">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-579">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="8fe76-580">Ezek az **New-AzBatchTask**`-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="8fe76-580">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="8fe76-581">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="8fe76-581">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="8fe76-582">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="8fe76-582">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="8fe76-583">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="8fe76-583">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="8fe76-584">A `PSApplication`**Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-584">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="8fe76-585">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="8fe76-585">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="8fe76-586">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="8fe76-586">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="8fe76-587">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-587">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="8fe76-588">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="8fe76-588">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="8fe76-589">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="8fe76-589">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="8fe76-590">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-590">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="8fe76-591">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-591">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="8fe76-592">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="8fe76-592">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="8fe76-593">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-593">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="8fe76-594">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-594">This operation is no longer supported.</span></span>
* <span data-ttu-id="8fe76-595">`PSCloudServiceConfiguration``TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-595">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="8fe76-596">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-596">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="8fe76-597">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="8fe76-597">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="8fe76-598">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="8fe76-598">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="8fe76-599">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="8fe76-599">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="8fe76-600">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="8fe76-600">New non-verified images are also now returned.</span></span> <span data-ttu-id="8fe76-601">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="8fe76-601">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="8fe76-602">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="8fe76-602">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="8fe76-603">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="8fe76-603">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="8fe76-604">Ez a `PSNetworkSecurityGroupRule``SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="8fe76-604">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="8fe76-605">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="8fe76-605">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="8fe76-606">Ezt a `PSTaskContainerSettings``WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="8fe76-606">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="8fe76-607">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="8fe76-607">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="8fe76-608">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="8fe76-608">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="8fe76-609">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="8fe76-609">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="8fe76-610">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="8fe76-610">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8fe76-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8fe76-611">Az.Cdn</span></span>
* <span data-ttu-id="8fe76-612">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="8fe76-612">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="8fe76-613">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="8fe76-613">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-614">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-614">Az.Compute</span></span>
* <span data-ttu-id="8fe76-615">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="8fe76-615">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="8fe76-616">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="8fe76-616">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="8fe76-617">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8fe76-617">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="8fe76-618">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-618">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8fe76-619">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-619">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="8fe76-620">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="8fe76-620">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="8fe76-621">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-621">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="8fe76-622">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="8fe76-622">Breaking changes</span></span>
    - <span data-ttu-id="8fe76-623">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="8fe76-623">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="8fe76-624">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="8fe76-624">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8fe76-625">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fe76-625">Az.DataFactory</span></span>
* <span data-ttu-id="8fe76-626">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="8fe76-626">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8fe76-627">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8fe76-627">Az.DataLakeStore</span></span>
* <span data-ttu-id="8fe76-628">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="8fe76-628">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="8fe76-629">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="8fe76-629">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="8fe76-630">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="8fe76-630">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="8fe76-631">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="8fe76-631">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="8fe76-632">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-632">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="8fe76-633">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-633">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8fe76-634">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8fe76-634">Az.FrontDoor</span></span>
* <span data-ttu-id="8fe76-635">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="8fe76-635">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8fe76-636">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8fe76-636">Az.HDInsight</span></span>
* <span data-ttu-id="8fe76-637">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-637">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="8fe76-638">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-638">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="8fe76-639">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="8fe76-639">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="8fe76-640">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="8fe76-640">Removed five cmdlets:</span></span>
    - <span data-ttu-id="8fe76-641">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8fe76-641">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8fe76-642">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8fe76-642">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8fe76-643">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8fe76-643">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8fe76-644">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8fe76-644">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="8fe76-645">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8fe76-645">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="8fe76-646">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="8fe76-646">Added three cmdlets:</span></span>
    - <span data-ttu-id="8fe76-647">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="8fe76-647">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="8fe76-648">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="8fe76-648">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="8fe76-649">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="8fe76-649">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="8fe76-650">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="8fe76-650">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="8fe76-651">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="8fe76-651">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="8fe76-652">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="8fe76-652">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="8fe76-653">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="8fe76-653">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="8fe76-654">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-654">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="8fe76-655">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-655">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="8fe76-656">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-656">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="8fe76-657">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-657">Added some scenario test cases.</span></span>
* <span data-ttu-id="8fe76-658">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="8fe76-658">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8fe76-659">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-659">Az.IotHub</span></span>
* <span data-ttu-id="8fe76-660">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="8fe76-660">Breaking changes:</span></span>
    - <span data-ttu-id="8fe76-661">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-661">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8fe76-662">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-662">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8fe76-663">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-663">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8fe76-664">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-664">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8fe76-665">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-665">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="8fe76-666">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-666">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="8fe76-667">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="8fe76-667">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="8fe76-668">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="8fe76-668">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="8fe76-669">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-669">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8fe76-670">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-670">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8fe76-671">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-671">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8fe76-672">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-672">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-673">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-673">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-674">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="8fe76-674">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="8fe76-675">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="8fe76-675">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="8fe76-676">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="8fe76-676">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="8fe76-677">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="8fe76-677">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="8fe76-678">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="8fe76-678">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="8fe76-679">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="8fe76-679">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="8fe76-680">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="8fe76-680">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="8fe76-681">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="8fe76-681">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="8fe76-682">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="8fe76-682">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-683">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-683">Az.Resources</span></span>
* <span data-ttu-id="8fe76-684">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="8fe76-684">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-685">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-685">Az.Network</span></span>
* <span data-ttu-id="8fe76-686">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-686">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="8fe76-687">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="8fe76-687">Updated cmdlet:</span></span>
        - <span data-ttu-id="8fe76-688">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-688">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8fe76-689">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-689">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8fe76-690">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-690">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8fe76-691">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-691">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8fe76-692">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-692">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8fe76-693">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-693">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="8fe76-694">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="8fe76-694">New cmdlet:</span></span>
        - <span data-ttu-id="8fe76-695">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="8fe76-695">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="8fe76-696">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-696">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="8fe76-697">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="8fe76-697">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="8fe76-698">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="8fe76-698">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="8fe76-699">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="8fe76-699">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="8fe76-700">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="8fe76-700">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="8fe76-701">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-701">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="8fe76-702">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-702">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="8fe76-703">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="8fe76-703">New cmdlets added:</span></span>
        - <span data-ttu-id="8fe76-704">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="8fe76-704">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="8fe76-705">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8fe76-705">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8fe76-706">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8fe76-706">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8fe76-707">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8fe76-707">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8fe76-708">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-708">Set-AzVirtualHub</span></span>
* <span data-ttu-id="8fe76-709">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-709">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="8fe76-710">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="8fe76-710">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8fe76-711">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-711">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="8fe76-712">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-712">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="8fe76-713">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-713">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="8fe76-714">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-714">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="8fe76-715">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-715">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="8fe76-716">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="8fe76-716">New cmdlets added:</span></span>
        - <span data-ttu-id="8fe76-717">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-717">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="8fe76-718">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="8fe76-718">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8fe76-719">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-719">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8fe76-720">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-720">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8fe76-721">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-721">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8fe76-722">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-722">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8fe76-723">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-723">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="8fe76-724">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-724">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="8fe76-725">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="8fe76-725">New cmdlets added:</span></span>
        - <span data-ttu-id="8fe76-726">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="8fe76-726">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="8fe76-727">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="8fe76-727">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="8fe76-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="8fe76-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="8fe76-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="8fe76-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="8fe76-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="8fe76-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="8fe76-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fe76-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="8fe76-732">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="8fe76-732">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8fe76-733">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-733">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="8fe76-734">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-734">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="8fe76-735">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="8fe76-735">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="8fe76-736">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-736">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="8fe76-737">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="8fe76-737">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8fe76-738">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-738">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="8fe76-739">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-739">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="8fe76-740">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="8fe76-740">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="8fe76-741">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="8fe76-741">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="8fe76-742">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-742">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="8fe76-743">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="8fe76-743">New cmdlets added:</span></span>
        - <span data-ttu-id="8fe76-744">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8fe76-744">New-AzIpGroup</span></span>
        - <span data-ttu-id="8fe76-745">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8fe76-745">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="8fe76-746">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8fe76-746">Get-AzIpGroup</span></span>
        - <span data-ttu-id="8fe76-747">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8fe76-747">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8fe76-748">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8fe76-748">Az.ServiceFabric</span></span>
* <span data-ttu-id="8fe76-749">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="8fe76-749">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-750">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-750">Az.Sql</span></span>
* <span data-ttu-id="8fe76-751">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="8fe76-751">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="8fe76-752">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="8fe76-752">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="8fe76-753">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="8fe76-753">Removed deprecated aliases:</span></span>
* <span data-ttu-id="8fe76-754">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="8fe76-754">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="8fe76-755">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="8fe76-755">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="8fe76-756">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="8fe76-756">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8fe76-757">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="8fe76-757">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="8fe76-758">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="8fe76-758">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="8fe76-759">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="8fe76-759">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-760">Az.Storage</span></span>
* <span data-ttu-id="8fe76-761">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="8fe76-761">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="8fe76-762">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe76-762">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8fe76-763">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe76-763">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8fe76-764">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="8fe76-764">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="8fe76-765">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8fe76-765">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="8fe76-766">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8fe76-766">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="8fe76-767">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="8fe76-767">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="8fe76-768">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="8fe76-768">General</span></span>
* <span data-ttu-id="8fe76-769">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="8fe76-769">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8fe76-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-770">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-771">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-771">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8fe76-772">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8fe76-772">Az.ApiManagement</span></span>
* <span data-ttu-id="8fe76-773">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8fe76-773">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="8fe76-774">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="8fe76-774">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8fe76-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8fe76-775">Az.Automation</span></span>
* <span data-ttu-id="8fe76-776">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="8fe76-776">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8fe76-777">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8fe76-777">Az.Batch</span></span>
* <span data-ttu-id="8fe76-778">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="8fe76-778">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-779">Az.Compute</span></span>
* <span data-ttu-id="8fe76-780">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-780">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="8fe76-781">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-781">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="8fe76-782">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="8fe76-782">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="8fe76-783">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-783">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8fe76-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fe76-784">Az.DataFactory</span></span>
* <span data-ttu-id="8fe76-785">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="8fe76-785">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="8fe76-786">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="8fe76-786">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="8fe76-787">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="8fe76-787">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8fe76-788">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8fe76-788">Az.DataLakeStore</span></span>
* <span data-ttu-id="8fe76-789">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="8fe76-789">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8fe76-790">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8fe76-790">Az.HealthcareApis</span></span>
* <span data-ttu-id="8fe76-791">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="8fe76-791">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="8fe76-792">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="8fe76-792">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="8fe76-793">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-793">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="8fe76-794">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="8fe76-794">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8fe76-795">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-795">Az.IotHub</span></span>
* <span data-ttu-id="8fe76-796">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="8fe76-796">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="8fe76-797">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="8fe76-797">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8fe76-798">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8fe76-798">Az.Monitor</span></span>
* <span data-ttu-id="8fe76-799">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="8fe76-799">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="8fe76-800">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="8fe76-800">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="8fe76-801">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="8fe76-801">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="8fe76-802">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="8fe76-802">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-803">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-803">Az.Network</span></span>
* <span data-ttu-id="8fe76-804">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="8fe76-804">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="8fe76-805">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-805">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="8fe76-806">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="8fe76-806">New cmdlets added:</span></span>
        - <span data-ttu-id="8fe76-807">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="8fe76-807">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="8fe76-808">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-808">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8fe76-809">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="8fe76-809">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="8fe76-810">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="8fe76-810">Updated cmdlets:</span></span>
        - <span data-ttu-id="8fe76-811">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-811">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8fe76-812">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-812">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8fe76-813">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-813">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8fe76-814">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="8fe76-814">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="8fe76-815">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="8fe76-815">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="8fe76-816">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="8fe76-816">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="8fe76-817">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="8fe76-817">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8fe76-818">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8fe76-818">Az.RedisCache</span></span>
* <span data-ttu-id="8fe76-819">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="8fe76-819">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-820">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-820">Az.Sql</span></span>
* <span data-ttu-id="8fe76-821">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="8fe76-821">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-822">Az.Storage</span></span>
* <span data-ttu-id="8fe76-823">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="8fe76-823">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="8fe76-824">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="8fe76-824">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8fe76-825">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8fe76-825">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="8fe76-826">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="8fe76-826">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8fe76-827">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe76-827">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8fe76-828">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8fe76-828">Az.StorageSync</span></span>
* <span data-ttu-id="8fe76-829">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-829">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-830">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-830">Az.Websites</span></span>
* <span data-ttu-id="8fe76-831">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="8fe76-831">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="8fe76-832">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="8fe76-832">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8fe76-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8fe76-833">Az.ApiManagement</span></span>
* <span data-ttu-id="8fe76-834">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="8fe76-834">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="8fe76-835">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="8fe76-835">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="8fe76-836">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="8fe76-836">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8fe76-837">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8fe76-837">Az.Automation</span></span>
* <span data-ttu-id="8fe76-838">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="8fe76-838">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="8fe76-839">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-839">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="8fe76-840">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="8fe76-840">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-841">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-841">Az.Compute</span></span>
* <span data-ttu-id="8fe76-842">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-842">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="8fe76-843">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-843">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8fe76-844">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="8fe76-844">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="8fe76-845">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-845">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="8fe76-846">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-846">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="8fe76-847">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="8fe76-847">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="8fe76-848">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="8fe76-848">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="8fe76-849">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-849">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="8fe76-850">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-850">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8fe76-851">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fe76-851">Az.DataFactory</span></span>
* <span data-ttu-id="8fe76-852">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="8fe76-852">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="8fe76-853">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="8fe76-853">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8fe76-854">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8fe76-854">Az.HDInsight</span></span>
* <span data-ttu-id="8fe76-855">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="8fe76-855">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8fe76-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-856">Az.IotHub</span></span>
* <span data-ttu-id="8fe76-857">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-857">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="8fe76-858">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-858">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="8fe76-859">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="8fe76-859">New cmdlets are:</span></span>
    - <span data-ttu-id="8fe76-860">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8fe76-860">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8fe76-861">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8fe76-861">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8fe76-862">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8fe76-862">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8fe76-863">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8fe76-863">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8fe76-864">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8fe76-864">Az.Monitor</span></span>
* <span data-ttu-id="8fe76-865">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="8fe76-865">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="8fe76-866">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="8fe76-866">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="8fe76-867">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="8fe76-867">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="8fe76-868">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="8fe76-868">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="8fe76-869">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-869">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="8fe76-870">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="8fe76-870">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="8fe76-871">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="8fe76-871">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="8fe76-872">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="8fe76-872">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="8fe76-873">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="8fe76-873">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8fe76-874">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="8fe76-874">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="8fe76-875">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="8fe76-875">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8fe76-876">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="8fe76-876">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="8fe76-877">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-877">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="8fe76-878">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="8fe76-878">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="8fe76-879">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="8fe76-879">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="8fe76-880">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="8fe76-880">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="8fe76-881">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="8fe76-881">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="8fe76-882">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="8fe76-882">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="8fe76-883">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-883">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="8fe76-884">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="8fe76-884">Overall improved help files</span></span>
* <span data-ttu-id="8fe76-885">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="8fe76-885">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-886">Az.Network</span></span>
* <span data-ttu-id="8fe76-887">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="8fe76-887">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="8fe76-888">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="8fe76-888">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="8fe76-889">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="8fe76-889">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="8fe76-890">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="8fe76-890">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="8fe76-891">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="8fe76-891">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="8fe76-892">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="8fe76-892">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="8fe76-893">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-893">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="8fe76-894">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-894">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="8fe76-895">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-895">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="8fe76-896">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="8fe76-896">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="8fe76-897">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-897">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="8fe76-898">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="8fe76-898">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="8fe76-899">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8fe76-899">New cmdlets</span></span>
        - <span data-ttu-id="8fe76-900">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="8fe76-900">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="8fe76-901">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-901">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="8fe76-902">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="8fe76-902">Updated cmdlet:</span></span>
        - <span data-ttu-id="8fe76-903">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="8fe76-903">New-VpnSite</span></span>
        - <span data-ttu-id="8fe76-904">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="8fe76-904">Update-VpnSite</span></span>
        - <span data-ttu-id="8fe76-905">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-905">New-VpnConnection</span></span>
        - <span data-ttu-id="8fe76-906">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-906">Update-VpnConnection</span></span>
* <span data-ttu-id="8fe76-907">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="8fe76-907">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-908">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-908">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-909">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="8fe76-909">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="8fe76-910">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="8fe76-910">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-911">Az.Resources</span></span>
* <span data-ttu-id="8fe76-912">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="8fe76-912">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8fe76-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8fe76-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="8fe76-914">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="8fe76-914">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="8fe76-915">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="8fe76-915">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="8fe76-916">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8fe76-916">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8fe76-917">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8fe76-917">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8fe76-918">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8fe76-918">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8fe76-919">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="8fe76-919">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="8fe76-920">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8fe76-920">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8fe76-921">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8fe76-921">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8fe76-922">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8fe76-922">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8fe76-923">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8fe76-923">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8fe76-924">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="8fe76-924">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="8fe76-925">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8fe76-925">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8fe76-926">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8fe76-926">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8fe76-927">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8fe76-927">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8fe76-928">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="8fe76-928">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="8fe76-929">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="8fe76-929">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8fe76-930">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8fe76-930">Az.SignalR</span></span>
* <span data-ttu-id="8fe76-931">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8fe76-931">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-932">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-932">Az.Sql</span></span>
* <span data-ttu-id="8fe76-933">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="8fe76-933">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="8fe76-934">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="8fe76-934">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="8fe76-935">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="8fe76-935">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="8fe76-936">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="8fe76-936">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="8fe76-937">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="8fe76-937">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-938">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-938">Az.Storage</span></span>
* <span data-ttu-id="8fe76-939">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="8fe76-939">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="8fe76-940">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-940">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="8fe76-941">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8fe76-941">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="8fe76-942">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8fe76-942">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="8fe76-943">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-943">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="8fe76-944">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8fe76-944">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="8fe76-945">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="8fe76-945">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="8fe76-946">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8fe76-946">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8fe76-947">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8fe76-947">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8fe76-948">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8fe76-948">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8fe76-949">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8fe76-949">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-950">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-950">Az.Websites</span></span>
* <span data-ttu-id="8fe76-951">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="8fe76-951">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="8fe76-952">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="8fe76-952">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="8fe76-953">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="8fe76-953">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="8fe76-954">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="8fe76-954">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="8fe76-955">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="8fe76-955">General</span></span>
* <span data-ttu-id="8fe76-956">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="8fe76-956">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8fe76-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-957">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-958">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="8fe76-958">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="8fe76-959">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8fe76-959">Az.Aks</span></span>
* <span data-ttu-id="8fe76-960">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="8fe76-960">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="8fe76-961">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="8fe76-961">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8fe76-962">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8fe76-962">Az.ApiManagement</span></span>
* <span data-ttu-id="8fe76-963">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="8fe76-963">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="8fe76-964">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="8fe76-964">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="8fe76-965">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-965">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="8fe76-966">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="8fe76-966">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="8fe76-967">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="8fe76-967">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8fe76-968">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8fe76-968">Az.Batch</span></span>
* <span data-ttu-id="8fe76-969">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="8fe76-969">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8fe76-970">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8fe76-970">Az.Cdn</span></span>
* <span data-ttu-id="8fe76-971">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="8fe76-971">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-972">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-972">Az.Compute</span></span>
* <span data-ttu-id="8fe76-973">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-973">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="8fe76-974">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-974">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="8fe76-975">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-975">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="8fe76-976">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="8fe76-976">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="8fe76-977">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="8fe76-977">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="8fe76-978">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-978">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="8fe76-979">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="8fe76-979">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="8fe76-980">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="8fe76-980">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8fe76-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fe76-981">Az.DataFactory</span></span>
* <span data-ttu-id="8fe76-982">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="8fe76-982">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="8fe76-983">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="8fe76-983">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="8fe76-984">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="8fe76-984">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="8fe76-985">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="8fe76-985">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8fe76-986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8fe76-986">Az.DataLakeStore</span></span>
* <span data-ttu-id="8fe76-987">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="8fe76-987">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8fe76-988">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-988">Az.EventHub</span></span>
* <span data-ttu-id="8fe76-989">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="8fe76-989">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="8fe76-990">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="8fe76-990">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="8fe76-991">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-991">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="8fe76-992">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="8fe76-992">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="8fe76-993">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8fe76-993">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8fe76-994">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="8fe76-994">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8fe76-995">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8fe76-995">Az.Monitor</span></span>
* <span data-ttu-id="8fe76-996">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="8fe76-996">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-997">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-997">Az.Network</span></span>
* <span data-ttu-id="8fe76-998">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-998">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="8fe76-999">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="8fe76-999">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="8fe76-1000">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1000">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="8fe76-1001">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="8fe76-1001">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="8fe76-1002">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1002">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="8fe76-1003">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1003">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="8fe76-1004">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1004">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8fe76-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8fe76-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="8fe76-1006">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8fe76-1006">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="8fe76-1007">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1007">Added example</span></span>
    - <span data-ttu-id="8fe76-1008">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="8fe76-1008">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="8fe76-1009">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1009">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="8fe76-1010">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1010">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-1011">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1011">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-1012">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="8fe76-1012">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-1013">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-1013">Az.Resources</span></span>
* <span data-ttu-id="8fe76-1014">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="8fe76-1014">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="8fe76-1015">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1015">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="8fe76-1016">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="8fe76-1016">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="8fe76-1017">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1017">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8fe76-1018">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8fe76-1018">Az.ServiceBus</span></span>
* <span data-ttu-id="8fe76-1019">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="8fe76-1019">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="8fe76-1020">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="8fe76-1020">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="8fe76-1021">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="8fe76-1021">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8fe76-1022">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8fe76-1022">Az.ServiceFabric</span></span>
* <span data-ttu-id="8fe76-1023">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1023">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="8fe76-1024">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1024">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="8fe76-1025">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="8fe76-1025">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="8fe76-1026">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1026">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="8fe76-1027">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="8fe76-1027">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="8fe76-1028">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="8fe76-1028">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-1029">Az.Sql</span></span>
* <span data-ttu-id="8fe76-1030">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1030">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-1031">Az.Storage</span></span>
* <span data-ttu-id="8fe76-1032">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="8fe76-1032">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="8fe76-1033">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1033">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="8fe76-1034">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8fe76-1034">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="8fe76-1035">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8fe76-1035">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="8fe76-1036">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="8fe76-1036">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="8fe76-1037">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8fe76-1037">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-1038">Az.Websites</span></span>
* <span data-ttu-id="8fe76-1039">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1039">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="8fe76-1040">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="8fe76-1040">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8fe76-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-1041">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-1042">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1042">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="8fe76-1043">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8fe76-1043">Az.ApplicationInsights</span></span>
* <span data-ttu-id="8fe76-1044">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1044">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8fe76-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8fe76-1045">Az.Automation</span></span>
* <span data-ttu-id="8fe76-1046">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1046">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8fe76-1047">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1047">Az.CognitiveServices</span></span>
* <span data-ttu-id="8fe76-1048">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1048">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-1049">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-1049">Az.Compute</span></span>
* <span data-ttu-id="8fe76-1050">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1050">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8fe76-1051">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8fe76-1051">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8fe76-1052">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1052">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="8fe76-1053">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="8fe76-1053">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8fe76-1054">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fe76-1054">Az.DataFactory</span></span>
* <span data-ttu-id="8fe76-1055">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="8fe76-1055">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="8fe76-1056">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1056">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8fe76-1057">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-1057">Az.EventHub</span></span>
* <span data-ttu-id="8fe76-1058">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="8fe76-1058">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8fe76-1059">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="8fe76-1059">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8fe76-1060">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8fe76-1060">Az.KeyVault</span></span>
* <span data-ttu-id="8fe76-1061">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1061">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8fe76-1062">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8fe76-1062">Az.LogicApp</span></span>
* <span data-ttu-id="8fe76-1063">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="8fe76-1063">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="8fe76-1064">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1064">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="8fe76-1065">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1065">Az.ManagedServices</span></span>
* <span data-ttu-id="8fe76-1066">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1066">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-1067">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-1067">Az.Network</span></span>
* <span data-ttu-id="8fe76-1068">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1068">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="8fe76-1069">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8fe76-1069">New cmdlets</span></span>
        - <span data-ttu-id="8fe76-1070">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fe76-1070">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8fe76-1071">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8fe76-1071">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8fe76-1072">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-1072">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8fe76-1073">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-1073">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8fe76-1074">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-1074">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8fe76-1075">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-1075">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8fe76-1076">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="8fe76-1076">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="8fe76-1077">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8fe76-1077">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="8fe76-1078">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="8fe76-1078">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="8fe76-1079">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="8fe76-1079">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="8fe76-1080">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1080">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="8fe76-1081">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1081">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="8fe76-1082">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1082">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="8fe76-1083">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1083">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="8fe76-1084">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8fe76-1084">Updated cmdlets</span></span>
        - <span data-ttu-id="8fe76-1085">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-1085">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8fe76-1086">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-1086">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8fe76-1087">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-1087">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8fe76-1088">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="8fe76-1088">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8fe76-1089">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1089">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="8fe76-1090">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1090">Updated cmdlet:</span></span>
        - <span data-ttu-id="8fe76-1091">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-1091">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8fe76-1092">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-1092">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8fe76-1093">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-1093">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="8fe76-1094">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1094">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="8fe76-1095">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1095">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="8fe76-1096">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1096">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8fe76-1097">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8fe76-1097">Az.OperationalInsights</span></span>
* <span data-ttu-id="8fe76-1098">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1098">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="8fe76-1099">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="8fe76-1099">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-1100">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1100">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-1101">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1101">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8fe76-1102">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1102">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="8fe76-1103">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1103">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="8fe76-1104">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1104">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8fe76-1105">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1105">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="8fe76-1106">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1106">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8fe76-1107">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1107">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="8fe76-1108">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1108">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8fe76-1109">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1109">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="8fe76-1110">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1110">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-1111">Az.Resources</span></span>
- <span data-ttu-id="8fe76-1112">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1112">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="8fe76-1113">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="8fe76-1113">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8fe76-1114">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8fe76-1114">Az.ServiceBus</span></span>
* <span data-ttu-id="8fe76-1115">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="8fe76-1115">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8fe76-1116">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="8fe76-1116">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-1117">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-1117">Az.Sql</span></span>
* <span data-ttu-id="8fe76-1118">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1118">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="8fe76-1119">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1119">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="8fe76-1120">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1120">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-1121">Az.Storage</span></span>
* <span data-ttu-id="8fe76-1122">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="8fe76-1122">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8fe76-1123">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8fe76-1123">Az.StorageSync</span></span>
* <span data-ttu-id="8fe76-1124">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1124">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="8fe76-1125">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1125">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-1126">Az.Websites</span></span>
* <span data-ttu-id="8fe76-1127">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="8fe76-1127">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="8fe76-1128">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1128">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="8fe76-1129">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1129">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="8fe76-1130">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="8fe76-1130">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8fe76-1131">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-1131">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-1132">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1132">Add support for profile cmdlets</span></span>
* <span data-ttu-id="8fe76-1133">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1133">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="8fe76-1134">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="8fe76-1134">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8fe76-1135">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8fe76-1135">Az.Advisor</span></span>
* <span data-ttu-id="8fe76-1136">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1136">GA release of Az.Advisor</span></span>
* <span data-ttu-id="8fe76-1137">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="8fe76-1137">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8fe76-1138">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8fe76-1138">Az.ApiManagement</span></span>
* <span data-ttu-id="8fe76-1139">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="8fe76-1139">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="8fe76-1140">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8fe76-1140">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="8fe76-1141">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1141">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="8fe76-1142">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1142">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="8fe76-1143">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="8fe76-1143">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="8fe76-1144">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8fe76-1144">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="8fe76-1145">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="8fe76-1145">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8fe76-1146">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8fe76-1146">Az.Automation</span></span>
* <span data-ttu-id="8fe76-1147">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1147">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-1148">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-1148">Az.Compute</span></span>
* <span data-ttu-id="8fe76-1149">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1149">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8fe76-1150">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fe76-1150">Az.DataFactory</span></span>
* <span data-ttu-id="8fe76-1151">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1151">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8fe76-1152">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8fe76-1152">Az.EventGrid</span></span>
* <span data-ttu-id="8fe76-1153">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="8fe76-1153">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8fe76-1154">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-1154">Az.IotHub</span></span>
* <span data-ttu-id="8fe76-1155">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1155">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-1156">Az.Network</span></span>
* <span data-ttu-id="8fe76-1157">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1157">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="8fe76-1158">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="8fe76-1158">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8fe76-1159">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8fe76-1159">Az.PolicyInsights</span></span>
* <span data-ttu-id="8fe76-1160">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="8fe76-1160">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="8fe76-1161">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="8fe76-1161">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8fe76-1162">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8fe76-1162">Az.OperationalInsights</span></span>
* <span data-ttu-id="8fe76-1163">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="8fe76-1163">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-1165">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1165">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-1166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-1166">Az.Resources</span></span>
    - <span data-ttu-id="8fe76-1167">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1167">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="8fe76-1168">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1168">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="8fe76-1169">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1169">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="8fe76-1170">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1170">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8fe76-1171">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8fe76-1171">Az.ServiceBus</span></span>
* <span data-ttu-id="8fe76-1172">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="8fe76-1172">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-1173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-1173">Az.Sql</span></span>
* <span data-ttu-id="8fe76-1174">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1174">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="8fe76-1175">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1175">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="8fe76-1176">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8fe76-1176">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8fe76-1177">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8fe76-1177">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8fe76-1178">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8fe76-1178">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8fe76-1179">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8fe76-1179">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8fe76-1180">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8fe76-1180">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8fe76-1181">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8fe76-1181">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="8fe76-1182">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="8fe76-1182">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-1183">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-1183">Az.Storage</span></span>
* <span data-ttu-id="8fe76-1184">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1184">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="8fe76-1185">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8fe76-1185">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="8fe76-1186">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="8fe76-1186">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="8fe76-1187">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="8fe76-1187">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="8fe76-1188">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="8fe76-1188">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="8fe76-1189">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe76-1189">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8fe76-1190">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe76-1190">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8fe76-1191">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1191">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="8fe76-1192">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8fe76-1192">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="8fe76-1193">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8fe76-1193">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8fe76-1194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8fe76-1194">Az.StorageSync</span></span>
* <span data-ttu-id="8fe76-1195">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="8fe76-1195">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="8fe76-1196">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="8fe76-1196">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8fe76-1197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-1197">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-1198">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1198">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="8fe76-1199">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="8fe76-1199">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="8fe76-1200">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1200">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="8fe76-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8fe76-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="8fe76-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="8fe76-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-1203">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-1203">Az.Compute</span></span>
* <span data-ttu-id="8fe76-1204">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1204">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="8fe76-1205">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="8fe76-1205">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="8fe76-1206">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8fe76-1206">Az.Dns</span></span>
* <span data-ttu-id="8fe76-1207">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1207">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8fe76-1208">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8fe76-1208">Az.EventGrid</span></span>
* <span data-ttu-id="8fe76-1209">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1209">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="8fe76-1210">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1210">New cmdlets:</span></span>
    - <span data-ttu-id="8fe76-1211">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8fe76-1211">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8fe76-1212">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1212">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8fe76-1213">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8fe76-1213">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8fe76-1214">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1214">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="8fe76-1215">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8fe76-1215">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8fe76-1216">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1216">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8fe76-1217">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8fe76-1217">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8fe76-1218">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1218">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8fe76-1219">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8fe76-1219">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8fe76-1220">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1220">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="8fe76-1221">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1221">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8fe76-1222">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1222">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="8fe76-1223">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8fe76-1223">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="8fe76-1224">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="8fe76-1224">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="8fe76-1225">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1225">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8fe76-1226">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1226">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="8fe76-1227">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1227">Updated cmdlets:</span></span>
    - <span data-ttu-id="8fe76-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="8fe76-1229">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1229">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8fe76-1230">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1230">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8fe76-1231">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1231">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="8fe76-1232">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1232">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="8fe76-1233">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="8fe76-1233">Event subscription expiration date,</span></span>
            - <span data-ttu-id="8fe76-1234">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1234">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="8fe76-1235">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1235">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="8fe76-1236">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1236">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="8fe76-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="8fe76-1238">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1238">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="8fe76-1239">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8fe76-1239">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="8fe76-1240">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1240">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="8fe76-1241">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1241">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8fe76-1242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8fe76-1242">Az.FrontDoor</span></span>
* <span data-ttu-id="8fe76-1243">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="8fe76-1243">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="8fe76-1244">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="8fe76-1244">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="8fe76-1245">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="8fe76-1245">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="8fe76-1246">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1246">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-1247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-1247">Az.Network</span></span>
* <span data-ttu-id="8fe76-1248">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1248">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="8fe76-1249">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8fe76-1249">New cmdlets</span></span>
        - <span data-ttu-id="8fe76-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="8fe76-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="8fe76-1251">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1251">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="8fe76-1252">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8fe76-1252">New cmdlets</span></span>
        - <span data-ttu-id="8fe76-1253">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8fe76-1253">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="8fe76-1254">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1254">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="8fe76-1255">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8fe76-1255">New cmdlets</span></span>
        - <span data-ttu-id="8fe76-1256">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8fe76-1256">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8fe76-1257">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8fe76-1257">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8fe76-1258">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8fe76-1258">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8fe76-1259">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-1259">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="8fe76-1260">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-1260">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8fe76-1261">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1261">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="8fe76-1262">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8fe76-1262">New cmdlets</span></span>
        - <span data-ttu-id="8fe76-1263">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fe76-1263">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8fe76-1264">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fe76-1264">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8fe76-1265">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fe76-1265">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8fe76-1266">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="8fe76-1266">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="8fe76-1267">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="8fe76-1267">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="8fe76-1268">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1268">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="8fe76-1269">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1269">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="8fe76-1270">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1270">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="8fe76-1271">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1271">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="8fe76-1272">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="8fe76-1272">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="8fe76-1273">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="8fe76-1273">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="8fe76-1274">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1274">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="8fe76-1275">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1275">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="8fe76-1276">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1276">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="8fe76-1277">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1277">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="8fe76-1278">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1278">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="8fe76-1279">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="8fe76-1279">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="8fe76-1280">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1280">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="8fe76-1281">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1281">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="8fe76-1282">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="8fe76-1282">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="8fe76-1283">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="8fe76-1283">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="8fe76-1284">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="8fe76-1284">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="8fe76-1285">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="8fe76-1285">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="8fe76-1286">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1286">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="8fe76-1287">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1287">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8fe76-1288">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1288">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8fe76-1289">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1289">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8fe76-1290">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8fe76-1290">Az.OperationalInsights</span></span>
* <span data-ttu-id="8fe76-1291">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1291">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-1292">Az.Resources</span></span>
* <span data-ttu-id="8fe76-1293">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1293">Support for additional Template Export options</span></span>
    - <span data-ttu-id="8fe76-1294">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1294">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8fe76-1295">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1295">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8fe76-1296">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1296">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8fe76-1297">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8fe76-1297">Az.ServiceFabric</span></span>
* <span data-ttu-id="8fe76-1298">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="8fe76-1298">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-1299">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-1299">Az.Sql</span></span>
* <span data-ttu-id="8fe76-1300">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="8fe76-1300">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="8fe76-1301">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="8fe76-1301">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="8fe76-1302">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1302">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="8fe76-1303">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8fe76-1303">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8fe76-1304">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8fe76-1304">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8fe76-1305">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8fe76-1305">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8fe76-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8fe76-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="8fe76-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8fe76-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-1308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-1308">Az.Storage</span></span>
* <span data-ttu-id="8fe76-1309">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="8fe76-1309">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="8fe76-1310">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe76-1310">New-AzStorageAccount</span></span>
* <span data-ttu-id="8fe76-1311">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1311">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="8fe76-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8fe76-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-1313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-1313">Az.Websites</span></span>
* <span data-ttu-id="8fe76-1314">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="8fe76-1314">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="8fe76-1315">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1315">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="8fe76-1316">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="8fe76-1316">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="8fe76-1317">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8fe76-1317">Az.Cdn</span></span>
* <span data-ttu-id="8fe76-1318">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="8fe76-1318">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-1319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-1319">Az.Compute</span></span>
* <span data-ttu-id="8fe76-1320">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1320">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="8fe76-1321">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8fe76-1321">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8fe76-1322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-1322">Az.EventHub</span></span>
* <span data-ttu-id="8fe76-1323">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="8fe76-1323">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="8fe76-1324">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="8fe76-1324">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-1325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-1325">Az.Network</span></span>
* <span data-ttu-id="8fe76-1326">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="8fe76-1326">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="8fe76-1327">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1327">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8fe76-1328">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8fe76-1328">Az.PolicyInsights</span></span>
* <span data-ttu-id="8fe76-1329">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="8fe76-1329">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-1330">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1330">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-1331">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="8fe76-1331">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8fe76-1332">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8fe76-1332">Az.ServiceBus</span></span>
* <span data-ttu-id="8fe76-1333">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="8fe76-1333">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8fe76-1334">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8fe76-1334">Az.ServiceFabric</span></span>
* <span data-ttu-id="8fe76-1335">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1335">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="8fe76-1336">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1336">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-1337">Az.Sql</span></span>
* <span data-ttu-id="8fe76-1338">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1338">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="8fe76-1339">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1339">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8fe76-1340">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="8fe76-1340">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="8fe76-1341">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1341">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-1342">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-1342">Az.Websites</span></span>
* <span data-ttu-id="8fe76-1343">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="8fe76-1343">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="8fe76-1344">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="8fe76-1344">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8fe76-1345">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8fe76-1345">Az.ApiManagement</span></span>
* <span data-ttu-id="8fe76-1346">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1346">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="8fe76-1347">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1347">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="8fe76-1348">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1348">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="8fe76-1349">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="8fe76-1349">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="8fe76-1350">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1350">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="8fe76-1351">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1351">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="8fe76-1352">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="8fe76-1352">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="8fe76-1353">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="8fe76-1353">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="8fe76-1354">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1354">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="8fe76-1355">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1355">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="8fe76-1356">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="8fe76-1356">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="8fe76-1357">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1357">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="8fe76-1358">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1358">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="8fe76-1359">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1359">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="8fe76-1360">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1360">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="8fe76-1361">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1361">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="8fe76-1362">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1362">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="8fe76-1363">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1363">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="8fe76-1364">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1364">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="8fe76-1365">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1365">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="8fe76-1366">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1366">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="8fe76-1367">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1367">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="8fe76-1368">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1368">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="8fe76-1369">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1369">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="8fe76-1370">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="8fe76-1370">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="8fe76-1371">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="8fe76-1371">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="8fe76-1372">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1372">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="8fe76-1373">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1373">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="8fe76-1374">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1374">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="8fe76-1375">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1375">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="8fe76-1376">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1376">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="8fe76-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="8fe76-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="8fe76-1378">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1378">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="8fe76-1379">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1379">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8fe76-1380">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="8fe76-1380">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="8fe76-1381">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1381">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="8fe76-1382">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1382">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="8fe76-1383">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1383">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="8fe76-1384">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1384">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="8fe76-1385">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1385">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8fe76-1386">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="8fe76-1386">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8fe76-1387">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="8fe76-1387">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="8fe76-1388">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="8fe76-1388">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="8fe76-1389">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="8fe76-1389">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="8fe76-1390">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1390">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8fe76-1391">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="8fe76-1391">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8fe76-1392">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="8fe76-1392">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="8fe76-1393">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="8fe76-1393">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="8fe76-1394">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1394">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="8fe76-1395">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="8fe76-1395">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="8fe76-1396">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="8fe76-1396">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="8fe76-1397">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1397">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="8fe76-1398">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="8fe76-1398">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="8fe76-1399">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1399">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="8fe76-1400">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="8fe76-1400">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="8fe76-1401">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1401">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="8fe76-1402">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1402">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8fe76-1403">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1403">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8fe76-1404">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1404">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8fe76-1405">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1405">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8fe76-1406">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1406">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8fe76-1407">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1407">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8fe76-1408">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1408">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8fe76-1409">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1409">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8fe76-1410">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1410">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="8fe76-1411">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8fe76-1411">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="8fe76-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="8fe76-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="8fe76-1413">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="8fe76-1413">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="8fe76-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="8fe76-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="8fe76-1415">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8fe76-1415">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="8fe76-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="8fe76-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="8fe76-1417">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="8fe76-1417">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="8fe76-1418">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8fe76-1418">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="8fe76-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="8fe76-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="8fe76-1420">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8fe76-1420">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="8fe76-1421">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8fe76-1421">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="8fe76-1422">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8fe76-1422">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8fe76-1423">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8fe76-1423">Az.Automation</span></span>
* <span data-ttu-id="8fe76-1424">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1424">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="8fe76-1425">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="8fe76-1425">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="8fe76-1426">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="8fe76-1426">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="8fe76-1427">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="8fe76-1427">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="8fe76-1428">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="8fe76-1428">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="8fe76-1429">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1429">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="8fe76-1430">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1430">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-1431">Az.Compute</span></span>
* <span data-ttu-id="8fe76-1432">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1432">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="8fe76-1433">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="8fe76-1433">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8fe76-1434">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8fe76-1434">Az.DataLakeStore</span></span>
* <span data-ttu-id="8fe76-1435">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="8fe76-1435">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8fe76-1436">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8fe76-1436">Az.Monitor</span></span>
* <span data-ttu-id="8fe76-1437">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="8fe76-1437">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-1438">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-1438">Az.Network</span></span>
* <span data-ttu-id="8fe76-1439">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1439">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="8fe76-1440">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1440">Updated cmdlet:</span></span>
        - <span data-ttu-id="8fe76-1441">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="8fe76-1441">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="8fe76-1442">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="8fe76-1442">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-1443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-1443">Az.Resources</span></span>
* <span data-ttu-id="8fe76-1444">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1444">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-1445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-1445">Az.Sql</span></span>
* <span data-ttu-id="8fe76-1446">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1446">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="8fe76-1447">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="8fe76-1447">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8fe76-1448">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-1448">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-1449">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1449">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8fe76-1450">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1450">Az.CognitiveServices</span></span>
* <span data-ttu-id="8fe76-1451">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1451">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="8fe76-1452">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1452">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-1453">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-1453">Az.Compute</span></span>
* <span data-ttu-id="8fe76-1454">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1454">Proximity placement group feature.</span></span>
    - <span data-ttu-id="8fe76-1455">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8fe76-1455">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="8fe76-1456">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-1456">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="8fe76-1457">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1457">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="8fe76-1458">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1458">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="8fe76-1459">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1459">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="8fe76-1460">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="8fe76-1460">Breaking changes</span></span>
    - <span data-ttu-id="8fe76-1461">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1461">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="8fe76-1462">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1462">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="8fe76-1463">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="8fe76-1463">Az.DeploymentManager</span></span>
* <span data-ttu-id="8fe76-1464">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1464">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="8fe76-1465">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8fe76-1465">Az.Dns</span></span>
* <span data-ttu-id="8fe76-1466">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="8fe76-1466">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="8fe76-1467">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1467">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="8fe76-1468">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1468">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8fe76-1469">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8fe76-1469">Az.FrontDoor</span></span>
* <span data-ttu-id="8fe76-1470">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1470">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="8fe76-1471">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="8fe76-1471">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="8fe76-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8fe76-1472">Az.HDInsight</span></span>
* <span data-ttu-id="8fe76-1473">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1473">Removed two cmdlets:</span></span>
    - <span data-ttu-id="8fe76-1474">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8fe76-1474">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="8fe76-1475">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8fe76-1475">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8fe76-1476">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="8fe76-1476">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8fe76-1477">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1477">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="8fe76-1478">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1478">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="8fe76-1479">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1479">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8fe76-1480">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8fe76-1480">Az.Monitor</span></span>
* <span data-ttu-id="8fe76-1481">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="8fe76-1481">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="8fe76-1482">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="8fe76-1482">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="8fe76-1483">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="8fe76-1483">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="8fe76-1484">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="8fe76-1484">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="8fe76-1485">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="8fe76-1485">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="8fe76-1486">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="8fe76-1486">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="8fe76-1487">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="8fe76-1487">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="8fe76-1488">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8fe76-1488">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8fe76-1489">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8fe76-1489">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8fe76-1490">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8fe76-1490">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8fe76-1491">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8fe76-1491">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8fe76-1492">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8fe76-1492">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8fe76-1493">[További](/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="8fe76-1493">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="8fe76-1494">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="8fe76-1494">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-1495">Az.Network</span></span>
* <span data-ttu-id="8fe76-1496">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1496">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="8fe76-1497">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8fe76-1497">New cmdlets</span></span>
        - <span data-ttu-id="8fe76-1498">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8fe76-1498">New-AzNatGateway</span></span>
        - <span data-ttu-id="8fe76-1499">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8fe76-1499">Get-AzNatGateway</span></span>
        - <span data-ttu-id="8fe76-1500">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8fe76-1500">Set-AzNatGateway</span></span>
        - <span data-ttu-id="8fe76-1501">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8fe76-1501">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="8fe76-1502">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8fe76-1502">Updated cmdlets</span></span>
        - <span data-ttu-id="8fe76-1503">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8fe76-1503">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="8fe76-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8fe76-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="8fe76-1505">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1505">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="8fe76-1506">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1506">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="8fe76-1507">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1507">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8fe76-1508">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8fe76-1508">Az.PolicyInsights</span></span>
* <span data-ttu-id="8fe76-1509">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1509">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="8fe76-1510">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1510">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="8fe76-1511">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1511">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-1512">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1512">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-1513">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1513">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="8fe76-1514">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1514">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="8fe76-1515">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1515">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="8fe76-1516">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1516">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="8fe76-1517">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1517">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="8fe76-1518">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1518">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="8fe76-1519">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8fe76-1519">Az.Relay</span></span>
* <span data-ttu-id="8fe76-1520">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="8fe76-1520">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8fe76-1521">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8fe76-1521">Az.ServiceBus</span></span>
* <span data-ttu-id="8fe76-1522">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="8fe76-1522">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-1523">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-1523">Az.Storage</span></span>
* <span data-ttu-id="8fe76-1524">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="8fe76-1524">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="8fe76-1525">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1525">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="8fe76-1526">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1526">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="8fe76-1527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe76-1527">New-AzStorageAccount</span></span>
* <span data-ttu-id="8fe76-1528">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="8fe76-1528">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="8fe76-1529">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe76-1529">New-AzStorageAccount</span></span>
    - <span data-ttu-id="8fe76-1530">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe76-1530">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="8fe76-1531">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe76-1531">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-1532">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-1532">Az.Websites</span></span>
* <span data-ttu-id="8fe76-1533">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1533">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="8fe76-1534">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="8fe76-1534">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="8fe76-1535">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="8fe76-1535">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8fe76-1536">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="8fe76-1536">Highlights since the last major release</span></span>
* <span data-ttu-id="8fe76-1537">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1537">General availability of `Az` module</span></span>
* <span data-ttu-id="8fe76-1538">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8fe76-1538">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8fe76-1539">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8fe76-1539">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8fe76-1540">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1540">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8fe76-1541">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1541">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8fe76-1542">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1542">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8fe76-1543">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1543">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8fe76-1544">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-1544">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-1545">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1545">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8fe76-1546">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8fe76-1546">Az.Batch</span></span>
* <span data-ttu-id="8fe76-1547">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1547">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8fe76-1548">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8fe76-1548">Az.Cdn</span></span>
* <span data-ttu-id="8fe76-1549">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1549">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8fe76-1550">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1550">Az.CognitiveServices</span></span>
* <span data-ttu-id="8fe76-1551">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1551">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-1552">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-1552">Az.Compute</span></span>
* <span data-ttu-id="8fe76-1553">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="8fe76-1553">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="8fe76-1554">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1554">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8fe76-1555">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8fe76-1555">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8fe76-1556">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fe76-1556">Az.DataFactory</span></span>
* <span data-ttu-id="8fe76-1557">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1557">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8fe76-1558">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8fe76-1558">Az.DataLakeStore</span></span>
* <span data-ttu-id="8fe76-1559">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1559">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8fe76-1560">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8fe76-1560">Az.EventGrid</span></span>
* <span data-ttu-id="8fe76-1561">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1561">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8fe76-1562">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-1562">Az.EventHub</span></span>
* <span data-ttu-id="8fe76-1563">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="8fe76-1563">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8fe76-1564">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8fe76-1564">Az.HDInsight</span></span>
* <span data-ttu-id="8fe76-1565">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1565">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8fe76-1566">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-1566">Az.IotHub</span></span>
* <span data-ttu-id="8fe76-1567">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1567">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8fe76-1568">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8fe76-1568">Az.KeyVault</span></span>
* <span data-ttu-id="8fe76-1569">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8fe76-1570">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8fe76-1570">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8fe76-1571">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8fe76-1571">Az.MachineLearning</span></span>
* <span data-ttu-id="8fe76-1572">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1572">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="8fe76-1573">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8fe76-1573">Az.Media</span></span>
* <span data-ttu-id="8fe76-1574">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8fe76-1575">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8fe76-1575">Az.Monitor</span></span>
  * <span data-ttu-id="8fe76-1576">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8fe76-1576">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="8fe76-1577">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="8fe76-1577">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="8fe76-1578">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="8fe76-1578">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="8fe76-1579">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8fe76-1579">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8fe76-1580">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8fe76-1580">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8fe76-1581">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8fe76-1581">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="8fe76-1582">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="8fe76-1582">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-1583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-1583">Az.Network</span></span>
* <span data-ttu-id="8fe76-1584">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1584">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8fe76-1585">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8fe76-1585">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="8fe76-1586">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8fe76-1586">Az.NotificationHubs</span></span>
* <span data-ttu-id="8fe76-1587">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1587">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8fe76-1588">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8fe76-1588">Az.OperationalInsights</span></span>
* <span data-ttu-id="8fe76-1589">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="8fe76-1590">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8fe76-1590">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="8fe76-1591">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1591">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-1593">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1593">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8fe76-1594">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="8fe76-1594">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="8fe76-1595">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1595">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="8fe76-1596">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="8fe76-1596">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8fe76-1597">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8fe76-1597">Az.RedisCache</span></span>
* <span data-ttu-id="8fe76-1598">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1598">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-1599">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-1599">Az.Resources</span></span>
* <span data-ttu-id="8fe76-1600">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8fe76-1600">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-1601">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-1601">Az.Sql</span></span>
* <span data-ttu-id="8fe76-1602">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="8fe76-1602">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="8fe76-1603">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1603">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8fe76-1604">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1604">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="8fe76-1605">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1605">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="8fe76-1606">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1606">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="8fe76-1607">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1607">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="8fe76-1608">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8fe76-1608">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-1609">Az.Websites</span></span>
* <span data-ttu-id="8fe76-1610">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="8fe76-1610">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="8fe76-1611">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1611">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8fe76-1612">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1612">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="8fe76-1613">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1613">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="8fe76-1614">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="8fe76-1614">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8fe76-1615">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="8fe76-1615">Highlights since the last major release</span></span>
* <span data-ttu-id="8fe76-1616">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1616">General availability of `Az` module</span></span>
* <span data-ttu-id="8fe76-1617">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8fe76-1617">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8fe76-1618">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8fe76-1618">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8fe76-1619">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1619">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8fe76-1620">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1620">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8fe76-1621">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1621">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8fe76-1622">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1622">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8fe76-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-1623">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-1624">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1624">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8fe76-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1625">Az.AnalysisServices</span></span>
* <span data-ttu-id="8fe76-1626">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1626">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="8fe76-1627">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1627">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8fe76-1628">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8fe76-1628">Az.Automation</span></span>
* <span data-ttu-id="8fe76-1629">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1629">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="8fe76-1630">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1630">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="8fe76-1631">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1631">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-1632">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-1632">Az.Compute</span></span>
* <span data-ttu-id="8fe76-1633">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1633">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8fe76-1634">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1634">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="8fe76-1635">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8fe76-1635">Az.ContainerInstance</span></span>
* <span data-ttu-id="8fe76-1636">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="8fe76-1636">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8fe76-1637">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fe76-1637">Az.DataFactory</span></span>
* <span data-ttu-id="8fe76-1638">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1638">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="8fe76-1639">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1639">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-1640">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-1640">Az.Resources</span></span>
* <span data-ttu-id="8fe76-1641">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="8fe76-1641">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="8fe76-1642">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1642">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="8fe76-1643">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="8fe76-1643">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="8fe76-1644">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8fe76-1644">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="8fe76-1645">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1645">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="8fe76-1646">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8fe76-1646">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-1647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-1647">Az.Sql</span></span>
* <span data-ttu-id="8fe76-1648">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1648">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-1649">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-1649">Az.Storage</span></span>
* <span data-ttu-id="8fe76-1650">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="8fe76-1650">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="8fe76-1651">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8fe76-1651">New-AzStorageContext</span></span>
* <span data-ttu-id="8fe76-1652">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="8fe76-1652">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="8fe76-1653">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8fe76-1653">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8fe76-1654">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8fe76-1654">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8fe76-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8fe76-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="8fe76-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8fe76-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="8fe76-1657">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1657">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="8fe76-1658">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8fe76-1658">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8fe76-1659">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8fe76-1659">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8fe76-1660">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8fe76-1660">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="8fe76-1661">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8fe76-1661">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="8fe76-1662">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="8fe76-1662">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8fe76-1663">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="8fe76-1663">Highlights since the last major release</span></span>
* <span data-ttu-id="8fe76-1664">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1664">General availability of `Az` module</span></span>
* <span data-ttu-id="8fe76-1665">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8fe76-1665">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8fe76-1666">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8fe76-1666">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8fe76-1667">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1667">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8fe76-1668">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1668">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8fe76-1669">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1669">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8fe76-1670">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1670">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8fe76-1671">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8fe76-1671">Az.Automation</span></span>
* <span data-ttu-id="8fe76-1672">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1672">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="8fe76-1673">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="8fe76-1673">Dynamic grouping</span></span>
    * <span data-ttu-id="8fe76-1674">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="8fe76-1674">Pre-Post script</span></span>
    * <span data-ttu-id="8fe76-1675">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="8fe76-1675">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-1676">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-1676">Az.Compute</span></span>
* <span data-ttu-id="8fe76-1677">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1677">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="8fe76-1678">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="8fe76-1678">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8fe76-1679">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8fe76-1679">Az.KeyVault</span></span>
* <span data-ttu-id="8fe76-1680">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1680">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-1681">Az.Network</span></span>
* <span data-ttu-id="8fe76-1682">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1682">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="8fe76-1683">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1683">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-1684">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1684">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-1685">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1685">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="8fe76-1686">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1686">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-1687">Az.Resources</span></span>
* <span data-ttu-id="8fe76-1688">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1688">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="8fe76-1689">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1689">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-1690">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-1690">Az.Sql</span></span>
* <span data-ttu-id="8fe76-1691">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1691">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-1692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-1692">Az.Storage</span></span>
* <span data-ttu-id="8fe76-1693">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1693">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="8fe76-1694">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8fe76-1694">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8fe76-1695">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8fe76-1695">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8fe76-1696">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8fe76-1696">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8fe76-1697">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="8fe76-1697">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="8fe76-1698">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="8fe76-1698">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="8fe76-1699">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8fe76-1699">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-1700">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-1700">Az.Websites</span></span>
* <span data-ttu-id="8fe76-1701">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1701">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="8fe76-1702">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="8fe76-1702">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8fe76-1703">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-1703">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-1704">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1704">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="8fe76-1705">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1705">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8fe76-1706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8fe76-1706">Az.Automation</span></span>
* <span data-ttu-id="8fe76-1707">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1707">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="8fe76-1708">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1708">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="8fe76-1709">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="8fe76-1709">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8fe76-1710">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8fe76-1710">Az.Cdn</span></span>
* <span data-ttu-id="8fe76-1711">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="8fe76-1711">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-1712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-1712">Az.Compute</span></span>
* <span data-ttu-id="8fe76-1713">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1713">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8fe76-1714">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fe76-1714">Az.DataFactory</span></span>
* <span data-ttu-id="8fe76-1715">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="8fe76-1715">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8fe76-1716">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8fe76-1716">Az.LogicApp</span></span>
* <span data-ttu-id="8fe76-1717">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="8fe76-1717">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-1718">Az.Network</span></span>
* <span data-ttu-id="8fe76-1719">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1719">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-1720">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1720">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-1721">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1721">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="8fe76-1722">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="8fe76-1722">SDK Update</span></span>
* <span data-ttu-id="8fe76-1723">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="8fe76-1723">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="8fe76-1724">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1724">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-1725">Az.Resources</span></span>
* <span data-ttu-id="8fe76-1726">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1726">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="8fe76-1727">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="8fe76-1727">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="8fe76-1728">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="8fe76-1728">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="8fe76-1729">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="8fe76-1729">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="8fe76-1730">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="8fe76-1730">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="8fe76-1731">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="8fe76-1731">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-1732">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-1732">Az.Sql</span></span>
* <span data-ttu-id="8fe76-1733">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1733">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="8fe76-1734">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1734">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-1735">Az.Storage</span></span>
* <span data-ttu-id="8fe76-1736">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fe76-1736">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="8fe76-1737">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="8fe76-1737">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="8fe76-1738">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1738">Az.AnalysisServices</span></span>
* <span data-ttu-id="8fe76-1739">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="8fe76-1739">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8fe76-1740">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8fe76-1740">Az.Automation</span></span>
* <span data-ttu-id="8fe76-1741">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1741">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="8fe76-1742">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1742">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="8fe76-1743">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1743">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8fe76-1744">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1744">Az.CognitiveServices</span></span>
* <span data-ttu-id="8fe76-1745">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1745">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-1746">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-1746">Az.Compute</span></span>
* <span data-ttu-id="8fe76-1747">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="8fe76-1747">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="8fe76-1748">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1748">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="8fe76-1749">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1749">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="8fe76-1750">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1750">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8fe76-1751">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8fe76-1751">Az.DataLakeStore</span></span>
* <span data-ttu-id="8fe76-1752">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1752">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8fe76-1753">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-1753">Az.EventHub</span></span>
* <span data-ttu-id="8fe76-1754">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="8fe76-1754">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8fe76-1755">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8fe76-1755">Az.KeyVault</span></span>
* <span data-ttu-id="8fe76-1756">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1756">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8fe76-1757">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8fe76-1757">Az.LogicApp</span></span>
* <span data-ttu-id="8fe76-1758">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="8fe76-1758">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="8fe76-1759">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="8fe76-1759">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="8fe76-1760">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="8fe76-1760">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="8fe76-1761">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8fe76-1761">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8fe76-1762">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8fe76-1762">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8fe76-1763">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8fe76-1763">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8fe76-1764">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8fe76-1764">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="8fe76-1765">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1765">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="8fe76-1766">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fe76-1766">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8fe76-1767">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fe76-1767">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8fe76-1768">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fe76-1768">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8fe76-1769">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fe76-1769">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="8fe76-1770">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="8fe76-1770">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8fe76-1771">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8fe76-1771">Az.Monitor</span></span>
* <span data-ttu-id="8fe76-1772">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1772">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-1773">Az.Network</span></span>
* <span data-ttu-id="8fe76-1774">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="8fe76-1774">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8fe76-1775">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8fe76-1775">Az.OperationalInsights</span></span>
* <span data-ttu-id="8fe76-1776">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1776">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="8fe76-1777">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1777">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="8fe76-1778">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1778">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-1779">Az.Resources</span></span>
* <span data-ttu-id="8fe76-1780">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8fe76-1780">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8fe76-1781">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8fe76-1781">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="8fe76-1782">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="8fe76-1782">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="8fe76-1783">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="8fe76-1783">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-1784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-1784">Az.Sql</span></span>
* <span data-ttu-id="8fe76-1785">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1785">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="8fe76-1786">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="8fe76-1786">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-1787">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-1787">Az.Websites</span></span>
* <span data-ttu-id="8fe76-1788">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1788">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="8fe76-1789">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="8fe76-1789">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8fe76-1790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-1790">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-1791">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="8fe76-1791">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8fe76-1792">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1792">Az.AnalysisServices</span></span>
<span data-ttu-id="8fe76-1793">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1793">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-1794">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-1794">Az.Compute</span></span>
* <span data-ttu-id="8fe76-1795">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1795">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="8fe76-1796">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1796">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="8fe76-1797">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1797">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-1798">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1798">Az.RecoveryServices</span></span>
<span data-ttu-id="8fe76-1799">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1799">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-1800">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-1800">Az.Resources</span></span>
* <span data-ttu-id="8fe76-1801">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1801">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="8fe76-1802">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8fe76-1802">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8fe76-1803">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1803">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="8fe76-1804">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8fe76-1804">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-1805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-1805">Az.Sql</span></span>
* <span data-ttu-id="8fe76-1806">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1806">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="8fe76-1807">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1807">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="8fe76-1808">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1808">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="8fe76-1809">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="8fe76-1809">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8fe76-1810">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-1810">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-1811">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="8fe76-1811">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8fe76-1812">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1812">Az.AnalysisServices</span></span>
* <span data-ttu-id="8fe76-1813">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="8fe76-1813">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-1814">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1814">Az.RecoveryServices</span></span>
* <span data-ttu-id="8fe76-1815">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="8fe76-1815">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="8fe76-1816">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="8fe76-1816">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8fe76-1817">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-1817">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-1818">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1818">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8fe76-1819">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1819">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8fe76-1820">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="8fe76-1820">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="8fe76-1821">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8fe76-1821">Az.Aks</span></span>
* <span data-ttu-id="8fe76-1822">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1822">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8fe76-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8fe76-1823">Az.Automation</span></span>
* <span data-ttu-id="8fe76-1824">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1824">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="8fe76-1825">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1825">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8fe76-1826">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8fe76-1826">Az.Cdn</span></span>
* <span data-ttu-id="8fe76-1827">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1827">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-1828">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-1828">Az.Compute</span></span>
* <span data-ttu-id="8fe76-1829">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1829">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="8fe76-1830">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1830">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="8fe76-1831">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1831">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8fe76-1832">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8fe76-1832">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8fe76-1833">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1833">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8fe76-1834">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fe76-1834">Az.DataFactory</span></span>
* <span data-ttu-id="8fe76-1835">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1835">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8fe76-1836">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8fe76-1836">Az.DataLakeStore</span></span>
* <span data-ttu-id="8fe76-1837">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1837">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="8fe76-1838">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="8fe76-1838">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="8fe76-1839">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1839">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8fe76-1840">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-1840">Az.IotHub</span></span>
* <span data-ttu-id="8fe76-1841">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1841">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8fe76-1842">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8fe76-1842">Az.KeyVault</span></span>
* <span data-ttu-id="8fe76-1843">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1843">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-1844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-1844">Az.Network</span></span>
* <span data-ttu-id="8fe76-1845">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1845">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-1846">Az.Resources</span></span>
* <span data-ttu-id="8fe76-1847">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1847">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="8fe76-1848">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1848">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="8fe76-1849">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1849">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="8fe76-1850">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="8fe76-1850">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="8fe76-1851">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="8fe76-1851">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="8fe76-1852">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1852">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="8fe76-1853">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="8fe76-1853">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8fe76-1854">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8fe76-1854">Az.ServiceFabric</span></span>
* <span data-ttu-id="8fe76-1855">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1855">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="8fe76-1856">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1856">Fix some error messages.</span></span>
* <span data-ttu-id="8fe76-1857">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1857">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="8fe76-1858">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1858">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8fe76-1859">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8fe76-1859">Az.SignalR</span></span>
* <span data-ttu-id="8fe76-1860">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1860">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-1861">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-1861">Az.Sql</span></span>
* <span data-ttu-id="8fe76-1862">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1862">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8fe76-1863">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1863">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="8fe76-1864">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1864">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="8fe76-1865">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="8fe76-1865">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-1866">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-1866">Az.Storage</span></span>
* <span data-ttu-id="8fe76-1867">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1867">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8fe76-1868">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1868">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="8fe76-1869">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8fe76-1869">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="8fe76-1870">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="8fe76-1870">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="8fe76-1871">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8fe76-1871">Az.TrafficManager</span></span>
* <span data-ttu-id="8fe76-1872">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1872">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-1873">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-1873">Az.Websites</span></span>
* <span data-ttu-id="8fe76-1874">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1874">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8fe76-1875">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1875">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="8fe76-1876">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1876">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="8fe76-1877">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="8fe76-1877">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8fe76-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-1878">Az.Accounts</span></span>
* <span data-ttu-id="8fe76-1879">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1879">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-1880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-1880">Az.Compute</span></span>
* <span data-ttu-id="8fe76-1881">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="8fe76-1881">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="8fe76-1882">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="8fe76-1882">Updated the description of ID in help files</span></span>
* <span data-ttu-id="8fe76-1883">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8fe76-1884">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8fe76-1884">Az.DataLakeStore</span></span>
* <span data-ttu-id="8fe76-1885">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1885">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="8fe76-1886">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1886">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8fe76-1887">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8fe76-1887">Az.EventGrid</span></span>
* <span data-ttu-id="8fe76-1888">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1888">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="8fe76-1889">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="8fe76-1889">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="8fe76-1890">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1890">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8fe76-1891">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="8fe76-1891">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8fe76-1892">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="8fe76-1892">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8fe76-1893">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1893">Dead letter endpoint.</span></span>
    - <span data-ttu-id="8fe76-1894">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1894">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8fe76-1895">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="8fe76-1895">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8fe76-1896">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="8fe76-1896">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8fe76-1897">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1897">Dead letter endpoint.</span></span>
* <span data-ttu-id="8fe76-1898">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1898">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="8fe76-1899">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1899">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8fe76-1900">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8fe76-1900">Az.IotHub</span></span>
* <span data-ttu-id="8fe76-1901">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="8fe76-1901">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8fe76-1902">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8fe76-1902">Az.LogicApp</span></span>
* <span data-ttu-id="8fe76-1903">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="8fe76-1903">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-1904">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-1904">Az.Resources</span></span>
* <span data-ttu-id="8fe76-1905">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="8fe76-1905">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="8fe76-1906">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="8fe76-1906">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="8fe76-1907">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="8fe76-1907">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8fe76-1908">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="8fe76-1908">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="8fe76-1909">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-1909">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="8fe76-1910">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="8fe76-1910">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8fe76-1911">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8fe76-1911">Az.SignalR</span></span>
* <span data-ttu-id="8fe76-1912">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1912">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-1913">Az.Sql</span></span>
* <span data-ttu-id="8fe76-1914">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1914">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8fe76-1915">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-1915">Az.Storage</span></span>
* <span data-ttu-id="8fe76-1916">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1916">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="8fe76-1917">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8fe76-1917">New-AzStorageContext</span></span>
* <span data-ttu-id="8fe76-1918">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1918">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="8fe76-1919">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8fe76-1919">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-1920">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-1920">Az.Websites</span></span>
* <span data-ttu-id="8fe76-1921">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="8fe76-1921">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="8fe76-1922">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="8fe76-1922">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="8fe76-1923">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="8fe76-1923">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="8fe76-1924">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="8fe76-1924">General</span></span>

- <span data-ttu-id="8fe76-1925">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="8fe76-1925">General Availability of Az Module</span></span>
- <span data-ttu-id="8fe76-1926">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1926">Online help for each module</span></span>
- <span data-ttu-id="8fe76-1927">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="8fe76-1927">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="8fe76-1928">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8fe76-1928">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="8fe76-1929">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-1929">Az.Accounts</span></span>
- <span data-ttu-id="8fe76-1930">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="8fe76-1930">Changed from Az.Profile</span></span>
- <span data-ttu-id="8fe76-1931">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1931">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8fe76-1932">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8fe76-1932">Az.ApiManagement</span></span>
- <span data-ttu-id="8fe76-1933">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="8fe76-1933">Fixes for #7002</span></span>
- <span data-ttu-id="8fe76-1934">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8fe76-1934">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="8fe76-1935">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8fe76-1935">Az.Batch</span></span>
- <span data-ttu-id="8fe76-1936">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1936">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="8fe76-1937">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1937">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="8fe76-1938">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8fe76-1938">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="8fe76-1939">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8fe76-1939">Az.Billing</span></span>
- <span data-ttu-id="8fe76-1940">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1940">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="8fe76-1941">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1941">Az.CognitivServices</span></span>
- <span data-ttu-id="8fe76-1942">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1942">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="8fe76-1943">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1943">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8fe76-1944">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8fe76-1944">Az.ContainerInstance</span></span>
- <span data-ttu-id="8fe76-1945">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="8fe76-1945">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="8fe76-1946">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8fe76-1946">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="8fe76-1947">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8fe76-1947">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8fe76-1948">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8fe76-1948">Az.DataLakeStore</span></span>
- <span data-ttu-id="8fe76-1949">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8fe76-1949">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="8fe76-1950">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8fe76-1950">Az.Monitor</span></span>
- <span data-ttu-id="8fe76-1951">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8fe76-1951">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="8fe76-1952">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8fe76-1952">Az.KeyVault</span></span>
- <span data-ttu-id="8fe76-1953">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1953">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="8fe76-1954">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8fe76-1954">Az.MachineLearning</span></span>
- <span data-ttu-id="8fe76-1955">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="8fe76-1955">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="8fe76-1956">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8fe76-1956">Az.Media</span></span>
- <span data-ttu-id="8fe76-1957">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="8fe76-1957">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8fe76-1958">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-1958">Az.Network</span></span>
<span data-ttu-id="8fe76-1959">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1959">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="8fe76-1960">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="8fe76-1960">New cmdlets added:</span></span>
        - <span data-ttu-id="8fe76-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fe76-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8fe76-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fe76-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8fe76-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fe76-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8fe76-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fe76-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8fe76-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fe76-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8fe76-1966">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8fe76-1966">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="8fe76-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8fe76-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="8fe76-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fe76-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="8fe76-1969">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8fe76-1969">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="8fe76-1970">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8fe76-1970">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="8fe76-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8fe76-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8fe76-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8fe76-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8fe76-1973">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-1973">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="8fe76-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="8fe76-1975">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="8fe76-1975">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="8fe76-1976">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8fe76-1976">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="8fe76-1977">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8fe76-1977">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8fe76-1978">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8fe76-1978">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8fe76-1979">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8fe76-1979">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="8fe76-1980">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="8fe76-1980">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="8fe76-1981">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8fe76-1981">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="8fe76-1982">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8fe76-1982">Az.OperationalInsights</span></span>
- <span data-ttu-id="8fe76-1983">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8fe76-1983">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="8fe76-1984">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8fe76-1984">Az.Profile</span></span>
- <span data-ttu-id="8fe76-1985">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8fe76-1985">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-1986">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-1986">Az.RecoveryServices</span></span>
- <span data-ttu-id="8fe76-1987">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8fe76-1987">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="8fe76-1988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-1988">Az.Resources</span></span>
- <span data-ttu-id="8fe76-1989">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8fe76-1989">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8fe76-1990">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8fe76-1990">Az.ServiceFabric</span></span>
- <span data-ttu-id="8fe76-1991">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="8fe76-1991">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="8fe76-1992">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8fe76-1992">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="8fe76-1993">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8fe76-1993">Az.SIgnalR</span></span>
- <span data-ttu-id="8fe76-1994">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="8fe76-1994">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="8fe76-1995">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-1995">Az.Sql</span></span>
- <span data-ttu-id="8fe76-1996">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-1996">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="8fe76-1997">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="8fe76-1997">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="8fe76-1998">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8fe76-1998">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="8fe76-1999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-1999">Az.Storage</span></span>
- <span data-ttu-id="8fe76-2000">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8fe76-2000">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8fe76-2001">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-2001">Az.Websites</span></span>
- <span data-ttu-id="8fe76-2002">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="8fe76-2002">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="8fe76-2003">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="8fe76-2003">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="8fe76-2004">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="8fe76-2004">General</span></span>

* <span data-ttu-id="8fe76-2005">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-2005">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="8fe76-2006">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-2006">Az.Compute</span></span>

* <span data-ttu-id="8fe76-2007">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2007">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8fe76-2008">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8fe76-2008">Az.DataLakeStore</span></span>

* <span data-ttu-id="8fe76-2009">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="8fe76-2009">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="8fe76-2010">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8fe76-2010">Az.FrontDoor</span></span>

* <span data-ttu-id="8fe76-2011">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-2011">Fixed some broken links</span></span>
    - <span data-ttu-id="8fe76-2012">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2012">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="8fe76-2013">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2013">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8fe76-2014">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-2014">Az.RecoveryServices</span></span>

* <span data-ttu-id="8fe76-2015">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2015">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="8fe76-2016">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2016">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="8fe76-2017">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-2017">Az.Resources</span></span>

* <span data-ttu-id="8fe76-2018">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-2018">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="8fe76-2019">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2019">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="8fe76-2020">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-2020">Az.Sql</span></span>

* <span data-ttu-id="8fe76-2021">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-2021">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="8fe76-2022">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="8fe76-2022">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="8fe76-2023">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2023">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="8fe76-2024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-2024">Az.Storage</span></span>

* <span data-ttu-id="8fe76-2025">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-2025">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="8fe76-2026">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2026">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="8fe76-2027">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8fe76-2027">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8fe76-2028">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="8fe76-2028">Support Static Website configuration</span></span>
    - <span data-ttu-id="8fe76-2029">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8fe76-2029">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="8fe76-2030">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8fe76-2030">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8fe76-2031">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-2031">Az.Websites</span></span>

* <span data-ttu-id="8fe76-2032">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8fe76-2032">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="8fe76-2033">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2033">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="8fe76-2034">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2034">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="8fe76-2035">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="8fe76-2035">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8fe76-2036">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8fe76-2036">Az.ApiManagement</span></span>
* <span data-ttu-id="8fe76-2037">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2037">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="8fe76-2038">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8fe76-2038">Az.Automation</span></span>
* <span data-ttu-id="8fe76-2039">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2039">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="8fe76-2040">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2040">Added Update Management cmdlets</span></span>
* <span data-ttu-id="8fe76-2041">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2041">Added Source Control cmdlets</span></span>
* <span data-ttu-id="8fe76-2042">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2042">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="8fe76-2043">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2043">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="8fe76-2044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-2044">Az.Compute</span></span>
* <span data-ttu-id="8fe76-2045">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2045">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="8fe76-2046">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2046">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8fe76-2047">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8fe76-2047">Az.ContainerInstance</span></span>
* <span data-ttu-id="8fe76-2048">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2048">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="8fe76-2049">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8fe76-2049">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8fe76-2050">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2050">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8fe76-2051">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-2051">Az.Network</span></span>
* <span data-ttu-id="8fe76-2052">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2052">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="8fe76-2053">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2053">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="8fe76-2054">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2054">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="8fe76-2055">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2055">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="8fe76-2056">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8fe76-2056">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8fe76-2057">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2057">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="8fe76-2058">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2058">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="8fe76-2059">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8fe76-2059">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8fe76-2060">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2060">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="8fe76-2061">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2061">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="8fe76-2062">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8fe76-2062">Az.Relay</span></span>
* <span data-ttu-id="8fe76-2063">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2063">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="8fe76-2064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-2064">Az.Resources</span></span>
* <span data-ttu-id="8fe76-2065">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2065">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="8fe76-2066">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2066">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="8fe76-2067">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2067">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8fe76-2068">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8fe76-2068">Az.ServiceFabric</span></span>
* <span data-ttu-id="8fe76-2069">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2069">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="8fe76-2070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-2070">Az.Sql</span></span>
* <span data-ttu-id="8fe76-2071">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2071">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="8fe76-2072">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8fe76-2072">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8fe76-2073">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8fe76-2073">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8fe76-2074">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8fe76-2074">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8fe76-2075">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8fe76-2075">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8fe76-2076">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8fe76-2076">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8fe76-2077">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8fe76-2077">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8fe76-2078">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8fe76-2078">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8fe76-2079">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8fe76-2079">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="8fe76-2080">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2080">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="8fe76-2081">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2081">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="8fe76-2082">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2082">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="8fe76-2083">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2083">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8fe76-2084">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2084">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8fe76-2085">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2085">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="8fe76-2086">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2086">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="8fe76-2087">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2087">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="8fe76-2088">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="8fe76-2088">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8fe76-2089">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="8fe76-2089">General</span></span>
* <span data-ttu-id="8fe76-2090">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2090">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="8fe76-2091">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8fe76-2091">Az.Profile</span></span>
* <span data-ttu-id="8fe76-2092">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2092">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="8fe76-2093">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="8fe76-2093">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="8fe76-2094">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="8fe76-2094">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="8fe76-2095">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="8fe76-2095">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="8fe76-2096">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="8fe76-2096">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="8fe76-2097">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="8fe76-2097">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="8fe76-2098">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="8fe76-2098">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="8fe76-2099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-2099">Az.CognitiveServices</span></span>
* <span data-ttu-id="8fe76-2100">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2100">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-2101">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-2101">Az.Compute</span></span>
* <span data-ttu-id="8fe76-2102">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="8fe76-2102">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="8fe76-2103">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="8fe76-2103">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="8fe76-2104">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2104">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8fe76-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8fe76-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="8fe76-2106">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2106">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="8fe76-2107">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2107">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="8fe76-2108">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="8fe76-2108">Az.Insights</span></span>
* <span data-ttu-id="8fe76-2109">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="8fe76-2109">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="8fe76-2110">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="8fe76-2110">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="8fe76-2111">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="8fe76-2111">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="8fe76-2112">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="8fe76-2112">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-2113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-2113">Az.Network</span></span>
* <span data-ttu-id="8fe76-2114">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="8fe76-2114">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="8fe76-2115">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8fe76-2115">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="8fe76-2116">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8fe76-2116">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="8fe76-2117">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8fe76-2117">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="8fe76-2118">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8fe76-2118">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8fe76-2119">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8fe76-2119">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8fe76-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8fe76-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8fe76-2121">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8fe76-2121">Az.PolicyInsights</span></span>
* <span data-ttu-id="8fe76-2122">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-2122">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-2123">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-2123">Az.Resources</span></span>
* <span data-ttu-id="8fe76-2124">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="8fe76-2124">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="8fe76-2125">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="8fe76-2125">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8fe76-2126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8fe76-2126">Az.ServiceBus</span></span>
* <span data-ttu-id="8fe76-2127">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2127">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8fe76-2128">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8fe76-2128">Az.ServiceFabric</span></span>
* <span data-ttu-id="8fe76-2129">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2129">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="8fe76-2130">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="8fe76-2130">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="8fe76-2131">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="8fe76-2131">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="8fe76-2132">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="8fe76-2132">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="8fe76-2133">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2133">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="8fe76-2134">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="8fe76-2134">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="8fe76-2135">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8fe76-2135">Az.Profile</span></span>
* <span data-ttu-id="8fe76-2136">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2136">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="8fe76-2137">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2137">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-2138">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-2138">Az.Compute</span></span>
* <span data-ttu-id="8fe76-2139">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2139">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="8fe76-2140">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2140">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8fe76-2141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8fe76-2141">Az.DataLakeStore</span></span>
* <span data-ttu-id="8fe76-2142">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="8fe76-2142">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="8fe76-2143">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2143">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="8fe76-2144">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2144">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8fe76-2145">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2145">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8fe76-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-2147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-2147">Az.Network</span></span>
* <span data-ttu-id="8fe76-2148">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2148">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="8fe76-2149">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2149">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-2150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-2150">Az.Resources</span></span>
* <span data-ttu-id="8fe76-2151">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="8fe76-2151">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="8fe76-2152">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2152">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="8fe76-2153">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="8fe76-2153">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="8fe76-2154">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8fe76-2154">Azure.Storage</span></span>
* <span data-ttu-id="8fe76-2155">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="8fe76-2155">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="8fe76-2156">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8fe76-2156">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="8fe76-2157">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8fe76-2157">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8fe76-2158">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2158">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="8fe76-2159">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8fe76-2159">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8fe76-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8fe76-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="8fe76-2161">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2161">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8fe76-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8fe76-2162">Az.Compute</span></span>
* <span data-ttu-id="8fe76-2163">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2163">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="8fe76-2164">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2164">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="8fe76-2165">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="8fe76-2165">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="8fe76-2166">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8fe76-2166">Az.DataFactoryV2</span></span>
* <span data-ttu-id="8fe76-2167">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2167">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8fe76-2168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8fe76-2168">Az.Network</span></span>
* <span data-ttu-id="8fe76-2169">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2169">Added NetworkProfile functionality.</span></span> <span data-ttu-id="8fe76-2170">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="8fe76-2170">new cmdlets added</span></span>
    - <span data-ttu-id="8fe76-2171">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8fe76-2171">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="8fe76-2172">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8fe76-2172">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="8fe76-2173">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8fe76-2173">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="8fe76-2174">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8fe76-2174">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="8fe76-2175">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-2175">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="8fe76-2176">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="8fe76-2176">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="8fe76-2177">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="8fe76-2177">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="8fe76-2178">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="8fe76-2178">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="8fe76-2179">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="8fe76-2179">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8fe76-2180">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8fe76-2180">Az.RedisCache</span></span>
* <span data-ttu-id="8fe76-2181">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="8fe76-2181">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="8fe76-2182">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-2182">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="8fe76-2183">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8fe76-2183">Az.Resources</span></span>
* <span data-ttu-id="8fe76-2184">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="8fe76-2184">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8fe76-2185">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="8fe76-2185">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="8fe76-2186">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8fe76-2186">Az.Sql</span></span>
* <span data-ttu-id="8fe76-2187">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="8fe76-2187">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8fe76-2188">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8fe76-2188">Az.Websites</span></span>
* <span data-ttu-id="8fe76-2189">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="8fe76-2189">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="8fe76-2190">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="8fe76-2190">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="8fe76-2191">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="8fe76-2191">0.2.0 - September 2018</span></span>
 <span data-ttu-id="8fe76-2192">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="8fe76-2192">Initial Release</span></span>