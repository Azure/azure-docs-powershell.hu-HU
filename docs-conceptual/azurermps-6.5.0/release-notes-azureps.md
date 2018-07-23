---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: e9fa2d75c1c4e6ffaa2f7dd8e400f5b13dd4527d
ms.sourcegitcommit: 8b882d1c27d9e323447ff85f56d11bbf5e244d7f
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2018
ms.locfileid: "39110483"
---
# <a name="release-notes"></a><span data-ttu-id="4fa85-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="4fa85-103">Release notes</span></span>

<span data-ttu-id="4fa85-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="4fa85-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="650---july-2018"></a><span data-ttu-id="4fa85-105">6.5.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="4fa85-105">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="4fa85-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="4fa85-106">AzureRM.Profile</span></span>
* <span data-ttu-id="4fa85-107">A Get-AzureRmContextAutosaveSetting súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="4fa85-107">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="4fa85-108">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="4fa85-108">Azure.Storage</span></span>
* <span data-ttu-id="4fa85-109">Blob vagy fájl feltöltésének támogatása csak írási SAS-jogkivonattal</span><span class="sxs-lookup"><span data-stu-id="4fa85-109">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="4fa85-110">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4fa85-110">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="4fa85-111">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4fa85-111">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="4fa85-112">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4fa85-112">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="4fa85-113">A kötelező ResourceGroupName tulajdonság hozzáadása az AS-hez.</span><span class="sxs-lookup"><span data-stu-id="4fa85-113">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="4fa85-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="4fa85-114">AzureRM.Automation</span></span>
* <span data-ttu-id="4fa85-115">A súgó frissítése és a New-AzureRMAutomationSchedule példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="4fa85-115">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="4fa85-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="4fa85-116">AzureRM.Compute</span></span>
* <span data-ttu-id="4fa85-117">A -Tag paraméter hozzáadása a következőhöz: Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4fa85-117">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="4fa85-118">Az Add-AzureRmVmssExtension példájának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="4fa85-118">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="4fa85-119">A Remove-AzureRmVmssExtension példáinak hozzáadása</span><span class="sxs-lookup"><span data-stu-id="4fa85-119">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="4fa85-120">A Set-AzureRmVMAccessExtension súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="4fa85-120">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="4fa85-121">A New-AzureRmVmss SimpleParameterSet készletének frissítése, hogy a SinglePlacementGroup alapértelmezés szerint false (hamis) legyen, és a SinglePlacementGroup kapcsolóparaméter hozzáadása, amellyel a felhasználó egyetlen elhelyezési csoportban hozhatja létre a VMSS-t.</span><span class="sxs-lookup"><span data-stu-id="4fa85-121">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="4fa85-122">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="4fa85-122">AzureRM.EventHub</span></span>
* <span data-ttu-id="4fa85-123">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSEventHubDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="4fa85-123">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="4fa85-124">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4fa85-124">AzureRM.KeyVault</span></span>
* <span data-ttu-id="4fa85-125">A Set-AzureRmKeyVaultAccessPolicy hibaüzenetének frissítése</span><span class="sxs-lookup"><span data-stu-id="4fa85-125">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="4fa85-126">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4fa85-126">AzureRM.LogicApp</span></span>
* <span data-ttu-id="4fa85-127">„A paraméterkészlet nem oldható fel” hiba kijavítása a következőben: New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="4fa85-127">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="4fa85-128">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="4fa85-128">AzureRM.Network</span></span>
* <span data-ttu-id="4fa85-129">Társviszony-létesítés engedélyezése több bérlőben lévő virtuális hálózatok között a következőhöz: Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="4fa85-129">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="4fa85-130">Az alábbi parancsmagok frissítése az Application Gatewayhez</span><span class="sxs-lookup"><span data-stu-id="4fa85-130">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="4fa85-131">New-AzureRmApplicationGateway: Hozzáadott EnableFIPS jelző és zónatámogatás</span><span class="sxs-lookup"><span data-stu-id="4fa85-131">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="4fa85-132">New-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="4fa85-132">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="4fa85-133">Set-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k</span><span class="sxs-lookup"><span data-stu-id="4fa85-133">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="4fa85-134">A legújabb generátorverzióval újból létrehozott RouteTable parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4fa85-134">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="4fa85-135">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="4fa85-135">AzureRM.Relay</span></span>
* <span data-ttu-id="4fa85-136">Frissített Markdown-fájlok, a példában lévő paraméternév-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="4fa85-136">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="4fa85-137">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="4fa85-137">AzureRM.Resources</span></span>
* <span data-ttu-id="4fa85-138">A Roleassignment és a roledefinition parancsmagok frissítése:</span><span class="sxs-lookup"><span data-stu-id="4fa85-138">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="4fa85-139">A felesleges roledefinition hívások eltávolítása a lapozás részeként.</span><span class="sxs-lookup"><span data-stu-id="4fa85-139">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="4fa85-140">A Get-AzureRmRoleAssignment parancsmag javítása</span><span class="sxs-lookup"><span data-stu-id="4fa85-140">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="4fa85-141">Az -ExpandPrincipalGroups parancsparaméter működésének javítása</span><span class="sxs-lookup"><span data-stu-id="4fa85-141">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="4fa85-142">A Get-AzureRmResource hibájának kijavítása, ahol a -ResourceType paraméter különbséget tett a kis- és nagybetűk között</span><span class="sxs-lookup"><span data-stu-id="4fa85-142">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="4fa85-143">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4fa85-143">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="4fa85-144">A top és skip paraméter hozzáadása a listázási parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="4fa85-144">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="4fa85-145">Standard – Prémium NameSpace migrálási parancsmagok hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="4fa85-145">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="4fa85-146">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="4fa85-146">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="4fa85-147">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="4fa85-147">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="4fa85-148">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="4fa85-148">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="4fa85-149">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="4fa85-149">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="4fa85-150">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="4fa85-150">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="4fa85-151">A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSServiceBusDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során</span><span class="sxs-lookup"><span data-stu-id="4fa85-151">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="4fa85-152">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4fa85-152">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="4fa85-153">A New-AzureRmServiceFabricCluster példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="4fa85-153">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="4fa85-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="4fa85-154">AzureRM.Sql</span></span>
* <span data-ttu-id="4fa85-155">Új parancsmagok hozzáadása a Management.Sql elemhez, amelyekkel az ügyfelek TDE-tanúsítványt adhatnak az SQL Server-példányhoz vagy egy felügyelt példányhoz</span><span class="sxs-lookup"><span data-stu-id="4fa85-155">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="4fa85-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="4fa85-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="4fa85-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="4fa85-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="4fa85-158">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="4fa85-158">AzureRM.Websites</span></span>
* <span data-ttu-id="4fa85-159">A `Set-AzureRmWebApp -AssignIdentity` és `Set-AzureRmWebAppSlot -AssignIdentity` a false (hamis) érték esetén mostantól eltávolítja az Identitás tulajdonságot a hely object.Removing „előzetes verzió” címkéjéből is.</span><span class="sxs-lookup"><span data-stu-id="4fa85-159">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="4fa85-160">A `Get-AzureRmWebAppMetrics` és a `Get-AzureRmAppServicePlanMetrics` példa frissítése</span><span class="sxs-lookup"><span data-stu-id="4fa85-160">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="4fa85-161">A `Set-AzureRmWebApp -PhpVersion` támogatja az off értéket érvényes PHP-verzióként</span><span class="sxs-lookup"><span data-stu-id="4fa85-161">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="4fa85-162">6.4.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="4fa85-162">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="4fa85-163">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="4fa85-163">General</span></span>
* <span data-ttu-id="4fa85-164">Az OutputType attribútum formázása javítva a legtöbb modul súgófájljaiban</span><span class="sxs-lookup"><span data-stu-id="4fa85-164">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="4fa85-165">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="4fa85-165">AzureRM.Profile</span></span>
* <span data-ttu-id="4fa85-166">A Ps1Xml attribútum hozzáadva az alapszintű kimenettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="4fa85-166">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="4fa85-167">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="4fa85-167">AzureRM.Compute</span></span>
* <span data-ttu-id="4fa85-168">A VMSS IP-címke funkciója</span><span class="sxs-lookup"><span data-stu-id="4fa85-168">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="4fa85-169">A „New-AzureRmVmssIpTagConfig” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4fa85-169">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="4fa85-170">Az IpTag paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4fa85-170">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="4fa85-171">A VMSS automatikus operációsrendszer-visszaállítási funkciója</span><span class="sxs-lookup"><span data-stu-id="4fa85-171">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="4fa85-172">A DisableAutoRollback-paraméterek hozzáadva a New-AzureRmVmssConfig és az Update-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4fa85-172">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="4fa85-173">A VMSS operációsrendszer-frissítési előzmények funkciója</span><span class="sxs-lookup"><span data-stu-id="4fa85-173">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="4fa85-174">Az OSUpgradeHistory kapcsolóparaméter hozzáadva a Get-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4fa85-174">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="4fa85-175">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="4fa85-175">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="4fa85-176">Katalógushozzáférés-vezérlési listák támogatása hozzáadva az alábbi parancsokhoz:</span><span class="sxs-lookup"><span data-stu-id="4fa85-176">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="4fa85-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="4fa85-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="4fa85-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="4fa85-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="4fa85-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="4fa85-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="4fa85-180">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4fa85-180">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="4fa85-181">Megszakítás támogatása és az előrehaladás nyomon követése hozzáadva a Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry és Set-AzureRmDataLakeStoreItemAcl parancshoz</span><span class="sxs-lookup"><span data-stu-id="4fa85-181">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="4fa85-182">Megszakítás támogatása hozzáadva az Export-AzureRmDataLakeStoreChildItemProperties parancshoz</span><span class="sxs-lookup"><span data-stu-id="4fa85-182">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="4fa85-183">A rekurzív műveleteket végző parancsmagok hibakeresési üzeneteinek kiürítése javítva</span><span class="sxs-lookup"><span data-stu-id="4fa85-183">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="4fa85-184">A DataLake-parancsmagok tesztelési helye javítva</span><span class="sxs-lookup"><span data-stu-id="4fa85-184">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="4fa85-185">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="4fa85-185">AzureRM.EventHub</span></span>
* <span data-ttu-id="4fa85-186">Opcionális MaxCount paraméter hozzáadva a Get-AzureRmEventHub és a Get-AzureRmEventHubConsumerGroup listaműveleti parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="4fa85-186">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="4fa85-187">Ki lett javítva egy probléma a New-AzureRmEventHub parancsmagban, ahol legalább egy paramétert meg kellett adni az új EventHub létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="4fa85-187">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="4fa85-188">Az alapértelmezett paraméterkészlet rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="4fa85-188">Provided Default Parameter set.</span></span>
* <span data-ttu-id="4fa85-189">-KeyValue opcionális paraméter hozzáadva a New-AzureRmEventHubKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="4fa85-189">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="4fa85-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4fa85-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="4fa85-191">Ki lett javítva az a probléma, hogy a Get-AzureRmKeyVault -Tag paramétere az összes erőforrást visszaadta</span><span class="sxs-lookup"><span data-stu-id="4fa85-191">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="4fa85-192">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="4fa85-192">AzureRM.Network</span></span>
* <span data-ttu-id="4fa85-193">Új termékváltozatok közzététele a zónaredundáns VirtualNetworkGatewayshez</span><span class="sxs-lookup"><span data-stu-id="4fa85-193">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="4fa85-194">Új parancsok hozzáadva a következő funkcióhoz: ExpressRoute-partner API-k az ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="4fa85-194">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="4fa85-195">Get-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4fa85-195">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="4fa85-196">Set-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4fa85-196">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="4fa85-197">Add-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4fa85-197">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="4fa85-198">Get-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4fa85-198">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="4fa85-199">Remove-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4fa85-199">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="4fa85-200">Get-AzureRMExpressRouteCrossConnectionArpTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4fa85-200">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="4fa85-201">Get-AzureRMExpressRouteCrossConnectionRouteTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4fa85-201">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="4fa85-202">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hozzáadva</span><span class="sxs-lookup"><span data-stu-id="4fa85-202">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="4fa85-203">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="4fa85-203">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="4fa85-204">Get-AzureRmRecoveryServicesBackupStatus parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="4fa85-204">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="4fa85-205">Ez a parancsmag egy virtuális gép azonosítójának használatával ellenőrzi, hogy a virtuális gépet védi-e tároló az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="4fa85-205">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="4fa85-206">Ha van ilyen tároló, a parancsmag megjeleníti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="4fa85-206">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="4fa85-207">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="4fa85-207">AzureRM.Resources</span></span>
* <span data-ttu-id="4fa85-208">Frissültek a Get-AzureRmPolicyAssignment-parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4fa85-208">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="4fa85-209">-Scope-értékek listázásának támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="4fa85-209">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="4fa85-210">-Scope-értékekkel történő egyedi hozzárendelések lekérésének támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="4fa85-210">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="4fa85-211">-Effective és -All kapcsoló hozzáadva a vezérlő paraméterhez</span><span class="sxs-lookup"><span data-stu-id="4fa85-211">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="4fa85-212">Frissültek a Get/New/Remove/Set-AzureRmPolicyDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4fa85-212">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="4fa85-213">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="4fa85-213">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="4fa85-214">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="4fa85-214">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="4fa85-215">Frissültek a Get/New/Remove/Set-AzureRmPolicySetDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4fa85-215">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="4fa85-216">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="4fa85-216">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="4fa85-217">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="4fa85-217">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="4fa85-218">KeyVault titkoskulcs-referencia paraméterekben történő használatának támogatása hozzáadva a TemplateParameterObject használatakor a New-AzureRmResourceGroupDeployment parancsmagban</span><span class="sxs-lookup"><span data-stu-id="4fa85-218">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="4fa85-219">Ki lett javítva egy probléma, amelynek során a rendszer nem vette figyelembe a New-AzureRmADAppCredential parancsmag -EndDate paraméterét</span><span class="sxs-lookup"><span data-stu-id="4fa85-219">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="4fa85-220">Ki lett javítva egy probléma, amelynek során az Add-AzureRmADGroupMember parancsmag nem megfelelő URL-címet használt a kérések elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="4fa85-220">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="4fa85-221">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4fa85-221">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="4fa85-222">A -KeyValue opcionális paraméter hozzáadva a New-AzureRmServiceBusKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="4fa85-222">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="4fa85-223">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="4fa85-223">AzureRM.Sql</span></span>
* <span data-ttu-id="4fa85-224">Tisztázva lettek az SQLDW felhasználó által meghatározott visszaállítási pontjai a New-AzureRmSqlDatabaseRestorePoint súgójában</span><span class="sxs-lookup"><span data-stu-id="4fa85-224">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="4fa85-225">Frissült a -ComputeGeneration paraméter dokumentációja több parancsmagban</span><span class="sxs-lookup"><span data-stu-id="4fa85-225">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="4fa85-226">6.3.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="4fa85-226">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="4fa85-227">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="4fa85-227">AzureRM.Profile</span></span>
* <span data-ttu-id="4fa85-228">Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek</span><span class="sxs-lookup"><span data-stu-id="4fa85-228">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="4fa85-229">Egy környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut</span><span class="sxs-lookup"><span data-stu-id="4fa85-229">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="4fa85-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="4fa85-230">Azure.Storage</span></span>
* <span data-ttu-id="4fa85-231">További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="4fa85-231">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="4fa85-232">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="4fa85-232">AzureRM.Compute</span></span>
* <span data-ttu-id="4fa85-233">A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik</span><span class="sxs-lookup"><span data-stu-id="4fa85-233">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="4fa85-234">A Compute ügyfélkódtár-verziója frissült, a következő parancsmagok javítása érdekében</span><span class="sxs-lookup"><span data-stu-id="4fa85-234">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="4fa85-235">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="4fa85-235">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="4fa85-236">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="4fa85-236">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="4fa85-237">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="4fa85-237">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="4fa85-238">A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:</span><span class="sxs-lookup"><span data-stu-id="4fa85-238">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="4fa85-239">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4fa85-239">Start-AzureRmVM</span></span>
    - <span data-ttu-id="4fa85-240">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4fa85-240">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="4fa85-241">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4fa85-241">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="4fa85-242">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4fa85-242">Set-AzureRmVM</span></span>
    - <span data-ttu-id="4fa85-243">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4fa85-243">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="4fa85-244">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4fa85-244">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="4fa85-245">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="4fa85-245">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="4fa85-246">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="4fa85-246">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="4fa85-247">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4fa85-247">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="4fa85-248">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4fa85-248">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="4fa85-249">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4fa85-249">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="4fa85-250">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4fa85-250">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="4fa85-251">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="4fa85-251">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="4fa85-252">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="4fa85-252">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="4fa85-253">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="4fa85-253">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="4fa85-254">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="4fa85-254">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="4fa85-255">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="4fa85-255">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="4fa85-256">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4fa85-256">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="4fa85-257">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4fa85-257">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="4fa85-258">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4fa85-258">AzureRM.EventGrid</span></span>
* <span data-ttu-id="4fa85-259">A ValidateNotNullOrEmpty érvényesítési feltételei az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="4fa85-259">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="4fa85-260">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4fa85-260">AzureRM.KeyVault</span></span>
* <span data-ttu-id="4fa85-261">Ki lett javítva egy probléma, amelynek során a parancs nem adott vissza címkét a Get-AzureRmKeyVault -Tag futtatásakor</span><span class="sxs-lookup"><span data-stu-id="4fa85-261">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="4fa85-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4fa85-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="4fa85-263">A Policy Insights-parancsmagok nyilvános kiadása</span><span class="sxs-lookup"><span data-stu-id="4fa85-263">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="4fa85-264">A 2018.04.04. dátumú API-verziót használják</span><span class="sxs-lookup"><span data-stu-id="4fa85-264">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="4fa85-265">A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez</span><span class="sxs-lookup"><span data-stu-id="4fa85-265">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="4fa85-266">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="4fa85-266">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="4fa85-267">A -Vault paraméter hozzá lett adva a RecoveryServices.Backup-parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="4fa85-267">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="4fa85-268">Ha át van adva, felülbírálja a Set-AzureRmRecoveryServicesContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4fa85-268">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="4fa85-269">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="4fa85-269">AzureRM.Sql</span></span>
* <span data-ttu-id="4fa85-270">A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült</span><span class="sxs-lookup"><span data-stu-id="4fa85-270">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="4fa85-271">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4fa85-271">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="4fa85-272">Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült</span><span class="sxs-lookup"><span data-stu-id="4fa85-272">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="4fa85-273">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="4fa85-273">AzureRM.Websites</span></span>
* <span data-ttu-id="4fa85-274">Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor</span><span class="sxs-lookup"><span data-stu-id="4fa85-274">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="4fa85-275">Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként</span><span class="sxs-lookup"><span data-stu-id="4fa85-275">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="4fa85-276">6.2.1 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="4fa85-276">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="4fa85-277">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4fa85-277">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="4fa85-278">Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja</span><span class="sxs-lookup"><span data-stu-id="4fa85-278">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="4fa85-279">6.2.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="4fa85-279">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="4fa85-280">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="4fa85-280">AzureRM.Profile</span></span>
* <span data-ttu-id="4fa85-281">Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során</span><span class="sxs-lookup"><span data-stu-id="4fa85-281">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="4fa85-282">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="4fa85-282">AzureRM.Compute</span></span>
* <span data-ttu-id="4fa85-283">VMSS VM frissítési funkciója</span><span class="sxs-lookup"><span data-stu-id="4fa85-283">VMSS VM Update feature</span></span>
    - <span data-ttu-id="4fa85-284">Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="4fa85-284">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="4fa85-285">A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez</span><span class="sxs-lookup"><span data-stu-id="4fa85-285">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="4fa85-286">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4fa85-286">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="4fa85-287">Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="4fa85-287">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="4fa85-288">Hozzá lett adva a gyári adattár konfigurálási művelete</span><span class="sxs-lookup"><span data-stu-id="4fa85-288">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="4fa85-289">Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez</span><span class="sxs-lookup"><span data-stu-id="4fa85-289">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="4fa85-290">Több modelltípus is frissült, a SecretBase-től az objektumig</span><span class="sxs-lookup"><span data-stu-id="4fa85-290">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="4fa85-291">A rendszer blobesemény-indítókkal bővült</span><span class="sxs-lookup"><span data-stu-id="4fa85-291">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="4fa85-292">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4fa85-292">AzureRM.KeyVault</span></span>
* <span data-ttu-id="4fa85-293">A dokumentáció kimeneti példával bővült</span><span class="sxs-lookup"><span data-stu-id="4fa85-293">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="4fa85-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="4fa85-294">AzureRM.Network</span></span>
* <span data-ttu-id="4fa85-295">Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon</span><span class="sxs-lookup"><span data-stu-id="4fa85-295">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="4fa85-296">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="4fa85-296">AzureRM.Resources</span></span>
* <span data-ttu-id="4fa85-297">Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát</span><span class="sxs-lookup"><span data-stu-id="4fa85-297">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="4fa85-298">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="4fa85-298">AzureRM.Scheduler</span></span>
* <span data-ttu-id="4fa85-299">Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat</span><span class="sxs-lookup"><span data-stu-id="4fa85-299">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="4fa85-300">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="4fa85-300">AzureRM.Sql</span></span>
* <span data-ttu-id="4fa85-301">A következő parancsmagok az opcionális LicenseType paraméterrel frissültek</span><span class="sxs-lookup"><span data-stu-id="4fa85-301">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="4fa85-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4fa85-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="4fa85-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4fa85-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="4fa85-304">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4fa85-304">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="4fa85-305">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4fa85-305">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="4fa85-306">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4fa85-306">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="4fa85-307">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="4fa85-307">AzureRM.Websites</span></span>
* <span data-ttu-id="4fa85-308">Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.</span><span class="sxs-lookup"><span data-stu-id="4fa85-308">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="4fa85-309">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="4fa85-309">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="4fa85-310">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="4fa85-310">AzureRM.Profile</span></span>
* <span data-ttu-id="4fa85-311">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="4fa85-311">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="4fa85-312">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4fa85-312">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="4fa85-313">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="4fa85-313">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="4fa85-314">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4fa85-314">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="4fa85-315">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="4fa85-315">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="4fa85-316">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="4fa85-316">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="4fa85-317">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="4fa85-317">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="4fa85-318">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="4fa85-318">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="4fa85-319">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="4fa85-319">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="4fa85-320">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="4fa85-320">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="4fa85-321">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="4fa85-321">Added support for MSI identity</span></span>
* <span data-ttu-id="4fa85-322">A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="4fa85-322">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="4fa85-323">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="4fa85-323">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="4fa85-324">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fa85-324">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="4fa85-325">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="4fa85-325">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="4fa85-326">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="4fa85-326">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="4fa85-327">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="4fa85-327">AzureRM.Batch</span></span>
* <span data-ttu-id="4fa85-328">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="4fa85-328">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="4fa85-329">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="4fa85-329">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="4fa85-330">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="4fa85-330">AzureRM.Consumption</span></span>
* <span data-ttu-id="4fa85-331">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="4fa85-331">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="4fa85-332">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4fa85-332">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="4fa85-333">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="4fa85-333">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="4fa85-334">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="4fa85-334">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="4fa85-335">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="4fa85-335">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="4fa85-336">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="4fa85-336">AzureRM.Network</span></span>
* <span data-ttu-id="4fa85-337">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="4fa85-337">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="4fa85-338">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="4fa85-338">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="4fa85-339">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fa85-339">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="4fa85-340">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="4fa85-340">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="4fa85-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4fa85-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="4fa85-342">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="4fa85-342">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="4fa85-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4fa85-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="4fa85-344">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="4fa85-344">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="4fa85-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4fa85-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="4fa85-346">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4fa85-346">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="4fa85-347">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="4fa85-347">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="4fa85-348">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="4fa85-348">AzureRM.Sql</span></span>
* <span data-ttu-id="4fa85-349">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="4fa85-349">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="4fa85-350">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="4fa85-350">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="4fa85-351">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="4fa85-351">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="4fa85-352">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="4fa85-352">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="4fa85-353">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="4fa85-353">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="4fa85-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4fa85-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="4fa85-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4fa85-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="4fa85-356">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4fa85-356">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="4fa85-357">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4fa85-357">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="4fa85-358">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4fa85-358">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="4fa85-359">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4fa85-359">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="4fa85-360">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="4fa85-360">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>