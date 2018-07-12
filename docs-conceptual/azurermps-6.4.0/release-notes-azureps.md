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
ms.openlocfilehash: 255e26aea5ea3cea866faa0d095cdf643c8ef0a8
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406483"
---
# <a name="release-notes"></a><span data-ttu-id="5c6e3-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="5c6e3-103">Release notes</span></span>

<span data-ttu-id="5c6e3-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="640---july-2018"></a><span data-ttu-id="5c6e3-105">6.4.0 – 2018. július</span><span class="sxs-lookup"><span data-stu-id="5c6e3-105">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="5c6e3-106">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="5c6e3-106">General</span></span>
* <span data-ttu-id="5c6e3-107">Az OutputType attribútum formázása javítva a legtöbb modul súgófájljaiban</span><span class="sxs-lookup"><span data-stu-id="5c6e3-107">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="5c6e3-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5c6e3-108">AzureRM.Profile</span></span>
* <span data-ttu-id="5c6e3-109">A Ps1Xml attribútum hozzáadva az alapszintű kimenettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="5c6e3-109">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="5c6e3-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="5c6e3-110">AzureRM.Compute</span></span>
* <span data-ttu-id="5c6e3-111">A VMSS IP-címke funkciója</span><span class="sxs-lookup"><span data-stu-id="5c6e3-111">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="5c6e3-112">A „New-AzureRmVmssIpTagConfig” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="5c6e3-112">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="5c6e3-113">Az IpTag paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="5c6e3-113">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="5c6e3-114">A VMSS automatikus operációsrendszer-visszaállítási funkciója</span><span class="sxs-lookup"><span data-stu-id="5c6e3-114">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="5c6e3-115">A DisableAutoRollback-paraméterek hozzáadva a New-AzureRmVmssConfig és az Update-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="5c6e3-115">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="5c6e3-116">A VMSS operációsrendszer-frissítési előzmények funkciója</span><span class="sxs-lookup"><span data-stu-id="5c6e3-116">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="5c6e3-117">Az OSUpgradeHistory kapcsolóparaméter hozzáadva a Get-AzureRmVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="5c6e3-117">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="5c6e3-118">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="5c6e3-118">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="5c6e3-119">Katalógushozzáférés-vezérlési listák támogatása hozzáadva az alábbi parancsokhoz:</span><span class="sxs-lookup"><span data-stu-id="5c6e3-119">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="5c6e3-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5c6e3-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="5c6e3-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5c6e3-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="5c6e3-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5c6e3-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="5c6e3-123">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c6e3-123">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="5c6e3-124">Megszakítás támogatása és az előrehaladás nyomon követése hozzáadva a Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry és Set-AzureRmDataLakeStoreItemAcl parancshoz</span><span class="sxs-lookup"><span data-stu-id="5c6e3-124">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="5c6e3-125">Megszakítás támogatása hozzáadva az Export-AzureRmDataLakeStoreChildItemProperties parancshoz</span><span class="sxs-lookup"><span data-stu-id="5c6e3-125">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="5c6e3-126">A rekurzív műveleteket végző parancsmagok hibakeresési üzeneteinek kiürítése javítva</span><span class="sxs-lookup"><span data-stu-id="5c6e3-126">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="5c6e3-127">A DataLake-parancsmagok tesztelési helye javítva</span><span class="sxs-lookup"><span data-stu-id="5c6e3-127">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="5c6e3-128">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c6e3-128">AzureRM.EventHub</span></span>
* <span data-ttu-id="5c6e3-129">Opcionális MaxCount paraméter hozzáadva a Get-AzureRmEventHub és a Get-AzureRmEventHubConsumerGroup listaműveleti parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="5c6e3-129">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="5c6e3-130">Ki lett javítva egy probléma a New-AzureRmEventHub parancsmagban, ahol legalább egy paramétert meg kellett adni az új EventHub létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-130">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="5c6e3-131">Az alapértelmezett paraméterkészlet rendelkezésre áll.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-131">Provided Default Parameter set.</span></span>
* <span data-ttu-id="5c6e3-132">-KeyValue opcionális paraméter hozzáadva a New-AzureRmEventHubKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-132">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="5c6e3-133">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c6e3-133">AzureRM.KeyVault</span></span>
* <span data-ttu-id="5c6e3-134">Ki lett javítva az a probléma, hogy a Get-AzureRmKeyVault -Tag paramétere az összes erőforrást visszaadta</span><span class="sxs-lookup"><span data-stu-id="5c6e3-134">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="5c6e3-135">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="5c6e3-135">AzureRM.Network</span></span>
* <span data-ttu-id="5c6e3-136">Új termékváltozatok közzététele a zónaredundáns VirtualNetworkGatewayshez</span><span class="sxs-lookup"><span data-stu-id="5c6e3-136">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="5c6e3-137">Új parancsok hozzáadva a következő funkcióhoz: ExpressRoute-partner API-k az ARM-en keresztül</span><span class="sxs-lookup"><span data-stu-id="5c6e3-137">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="5c6e3-138">Get-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="5c6e3-138">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="5c6e3-139">Set-AzureRmExpressRouteCrossConnection hozzáadva</span><span class="sxs-lookup"><span data-stu-id="5c6e3-139">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="5c6e3-140">Add-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="5c6e3-140">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="5c6e3-141">Get-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="5c6e3-141">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="5c6e3-142">Remove-AzureRmExpressRouteCrossConnectionPeering hozzáadva</span><span class="sxs-lookup"><span data-stu-id="5c6e3-142">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="5c6e3-143">Get-AzureRMExpressRouteCrossConnectionArpTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="5c6e3-143">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="5c6e3-144">Get-AzureRMExpressRouteCrossConnectionRouteTable hozzáadva</span><span class="sxs-lookup"><span data-stu-id="5c6e3-144">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="5c6e3-145">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hozzáadva</span><span class="sxs-lookup"><span data-stu-id="5c6e3-145">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="5c6e3-146">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="5c6e3-146">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="5c6e3-147">Get-AzureRmRecoveryServicesBackupStatus parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-147">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="5c6e3-148">Ez a parancsmag egy virtuális gép azonosítójának használatával ellenőrzi, hogy a virtuális gépet védi-e tároló az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-148">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="5c6e3-149">Ha van ilyen tároló, a parancsmag megjeleníti annak részleteit.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-149">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="5c6e3-150">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="5c6e3-150">AzureRM.Resources</span></span>
* <span data-ttu-id="5c6e3-151">Frissültek a Get-AzureRmPolicyAssignment-parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="5c6e3-151">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="5c6e3-152">-Scope-értékek listázásának támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="5c6e3-152">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="5c6e3-153">-Scope-értékekkel történő egyedi hozzárendelések lekérésének támogatása hozzáadva a felügyeleti csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="5c6e3-153">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="5c6e3-154">-Effective és -All kapcsoló hozzáadva a vezérlő paraméterhez</span><span class="sxs-lookup"><span data-stu-id="5c6e3-154">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="5c6e3-155">Frissültek a Get/New/Remove/Set-AzureRmPolicyDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="5c6e3-155">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="5c6e3-156">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="5c6e3-156">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="5c6e3-157">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="5c6e3-157">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="5c6e3-158">Frissültek a Get/New/Remove/Set-AzureRmPolicySetDefinition-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="5c6e3-158">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="5c6e3-159">-ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="5c6e3-159">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="5c6e3-160">-SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="5c6e3-160">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="5c6e3-161">KeyVault titkoskulcs-referencia paraméterekben történő használatának támogatása hozzáadva a TemplateParameterObject használatakor a New-AzureRmResourceGroupDeployment parancsmagban</span><span class="sxs-lookup"><span data-stu-id="5c6e3-161">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="5c6e3-162">Ki lett javítva egy probléma, amelynek során a rendszer nem vette figyelembe a New-AzureRmADAppCredential parancsmag -EndDate paraméterét</span><span class="sxs-lookup"><span data-stu-id="5c6e3-162">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="5c6e3-163">Ki lett javítva egy probléma, amelynek során az Add-AzureRmADGroupMember parancsmag nem megfelelő URL-címet használt a kérések elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="5c6e3-163">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="5c6e3-164">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c6e3-164">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="5c6e3-165">A -KeyValue opcionális paraméter hozzáadva a New-AzureRmServiceBusKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-165">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="5c6e3-166">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="5c6e3-166">AzureRM.Sql</span></span>
* <span data-ttu-id="5c6e3-167">Tisztázva lettek az SQLDW felhasználó által meghatározott visszaállítási pontjai a New-AzureRmSqlDatabaseRestorePoint súgójában</span><span class="sxs-lookup"><span data-stu-id="5c6e3-167">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="5c6e3-168">Frissült a -ComputeGeneration paraméter dokumentációja több parancsmagban</span><span class="sxs-lookup"><span data-stu-id="5c6e3-168">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="5c6e3-169">6.3.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="5c6e3-169">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="5c6e3-170">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5c6e3-170">AzureRM.Profile</span></span>
* <span data-ttu-id="5c6e3-171">Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek</span><span class="sxs-lookup"><span data-stu-id="5c6e3-171">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="5c6e3-172">Egy környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut</span><span class="sxs-lookup"><span data-stu-id="5c6e3-172">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="5c6e3-173">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="5c6e3-173">Azure.Storage</span></span>
* <span data-ttu-id="5c6e3-174">További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-174">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="5c6e3-175">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="5c6e3-175">AzureRM.Compute</span></span>
* <span data-ttu-id="5c6e3-176">A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik</span><span class="sxs-lookup"><span data-stu-id="5c6e3-176">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="5c6e3-177">A Compute ügyfélkódtár-verziója frissült, a következő parancsmagok javítása érdekében</span><span class="sxs-lookup"><span data-stu-id="5c6e3-177">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="5c6e3-178">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="5c6e3-178">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="5c6e3-179">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="5c6e3-179">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="5c6e3-180">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="5c6e3-180">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="5c6e3-181">A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:</span><span class="sxs-lookup"><span data-stu-id="5c6e3-181">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="5c6e3-182">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5c6e3-182">Start-AzureRmVM</span></span>
    - <span data-ttu-id="5c6e3-183">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5c6e3-183">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="5c6e3-184">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5c6e3-184">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="5c6e3-185">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5c6e3-185">Set-AzureRmVM</span></span>
    - <span data-ttu-id="5c6e3-186">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5c6e3-186">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="5c6e3-187">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5c6e3-187">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="5c6e3-188">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="5c6e3-188">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="5c6e3-189">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="5c6e3-189">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="5c6e3-190">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5c6e3-190">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="5c6e3-191">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5c6e3-191">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="5c6e3-192">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5c6e3-192">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="5c6e3-193">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5c6e3-193">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="5c6e3-194">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="5c6e3-194">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="5c6e3-195">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="5c6e3-195">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="5c6e3-196">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="5c6e3-196">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="5c6e3-197">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="5c6e3-197">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="5c6e3-198">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="5c6e3-198">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="5c6e3-199">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="5c6e3-199">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="5c6e3-200">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5c6e3-200">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="5c6e3-201">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5c6e3-201">AzureRM.EventGrid</span></span>
* <span data-ttu-id="5c6e3-202">A ValidateNotNullOrEmpty érvényesítési feltételei az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatók.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-202">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="5c6e3-203">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c6e3-203">AzureRM.KeyVault</span></span>
* <span data-ttu-id="5c6e3-204">Ki lett javítva egy probléma, amelynek során a parancs nem adott vissza címkét a Get-AzureRmKeyVault -Tag futtatásakor</span><span class="sxs-lookup"><span data-stu-id="5c6e3-204">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="5c6e3-205">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c6e3-205">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="5c6e3-206">A Policy Insights-parancsmagok nyilvános kiadása</span><span class="sxs-lookup"><span data-stu-id="5c6e3-206">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="5c6e3-207">A 2018.04.04. dátumú API-verziót használják</span><span class="sxs-lookup"><span data-stu-id="5c6e3-207">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="5c6e3-208">A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez</span><span class="sxs-lookup"><span data-stu-id="5c6e3-208">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="5c6e3-209">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="5c6e3-209">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="5c6e3-210">A -Vault paraméter hozzá lett adva a RecoveryServices.Backup-parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-210">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="5c6e3-211">Ha át van adva, felülbírálja a Set-AzureRmRecoveryServicesContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-211">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="5c6e3-212">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="5c6e3-212">AzureRM.Sql</span></span>
* <span data-ttu-id="5c6e3-213">A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült</span><span class="sxs-lookup"><span data-stu-id="5c6e3-213">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="5c6e3-214">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5c6e3-214">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="5c6e3-215">Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült</span><span class="sxs-lookup"><span data-stu-id="5c6e3-215">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="5c6e3-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="5c6e3-216">AzureRM.Websites</span></span>
* <span data-ttu-id="5c6e3-217">Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor</span><span class="sxs-lookup"><span data-stu-id="5c6e3-217">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="5c6e3-218">Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként</span><span class="sxs-lookup"><span data-stu-id="5c6e3-218">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="5c6e3-219">6.2.1 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="5c6e3-219">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="5c6e3-220">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c6e3-220">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="5c6e3-221">Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja</span><span class="sxs-lookup"><span data-stu-id="5c6e3-221">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="5c6e3-222">6.2.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="5c6e3-222">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="5c6e3-223">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5c6e3-223">AzureRM.Profile</span></span>
* <span data-ttu-id="5c6e3-224">Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során</span><span class="sxs-lookup"><span data-stu-id="5c6e3-224">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="5c6e3-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="5c6e3-225">AzureRM.Compute</span></span>
* <span data-ttu-id="5c6e3-226">VMSS VM frissítési funkciója</span><span class="sxs-lookup"><span data-stu-id="5c6e3-226">VMSS VM Update feature</span></span>
    - <span data-ttu-id="5c6e3-227">Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="5c6e3-227">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="5c6e3-228">A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez</span><span class="sxs-lookup"><span data-stu-id="5c6e3-228">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="5c6e3-229">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5c6e3-229">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="5c6e3-230">Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="5c6e3-230">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="5c6e3-231">Hozzá lett adva a gyári adattár konfigurálási művelete</span><span class="sxs-lookup"><span data-stu-id="5c6e3-231">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="5c6e3-232">Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez</span><span class="sxs-lookup"><span data-stu-id="5c6e3-232">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="5c6e3-233">Több modelltípus is frissült, a SecretBase-től az objektumig</span><span class="sxs-lookup"><span data-stu-id="5c6e3-233">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="5c6e3-234">A rendszer blobesemény-indítókkal bővült</span><span class="sxs-lookup"><span data-stu-id="5c6e3-234">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="5c6e3-235">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c6e3-235">AzureRM.KeyVault</span></span>
* <span data-ttu-id="5c6e3-236">A dokumentáció kimeneti példával bővült</span><span class="sxs-lookup"><span data-stu-id="5c6e3-236">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="5c6e3-237">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="5c6e3-237">AzureRM.Network</span></span>
* <span data-ttu-id="5c6e3-238">Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon</span><span class="sxs-lookup"><span data-stu-id="5c6e3-238">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="5c6e3-239">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="5c6e3-239">AzureRM.Resources</span></span>
* <span data-ttu-id="5c6e3-240">Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát</span><span class="sxs-lookup"><span data-stu-id="5c6e3-240">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="5c6e3-241">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="5c6e3-241">AzureRM.Scheduler</span></span>
* <span data-ttu-id="5c6e3-242">Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat</span><span class="sxs-lookup"><span data-stu-id="5c6e3-242">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="5c6e3-243">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="5c6e3-243">AzureRM.Sql</span></span>
* <span data-ttu-id="5c6e3-244">A következő parancsmagok az opcionális LicenseType paraméterrel frissültek</span><span class="sxs-lookup"><span data-stu-id="5c6e3-244">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="5c6e3-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c6e3-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="5c6e3-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5c6e3-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="5c6e3-247">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="5c6e3-247">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="5c6e3-248">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5c6e3-248">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="5c6e3-249">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c6e3-249">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="5c6e3-250">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="5c6e3-250">AzureRM.Websites</span></span>
* <span data-ttu-id="5c6e3-251">Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-251">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="5c6e3-252">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="5c6e3-252">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="5c6e3-253">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5c6e3-253">AzureRM.Profile</span></span>
* <span data-ttu-id="5c6e3-254">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="5c6e3-254">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="5c6e3-255">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c6e3-255">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="5c6e3-256">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-256">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="5c6e3-257">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c6e3-257">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="5c6e3-258">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="5c6e3-258">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="5c6e3-259">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="5c6e3-259">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="5c6e3-260">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="5c6e3-260">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="5c6e3-261">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="5c6e3-261">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="5c6e3-262">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="5c6e3-262">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="5c6e3-263">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="5c6e3-263">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="5c6e3-264">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="5c6e3-264">Added support for MSI identity</span></span>
* <span data-ttu-id="5c6e3-265">A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="5c6e3-265">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="5c6e3-266">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="5c6e3-266">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="5c6e3-267">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c6e3-267">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="5c6e3-268">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="5c6e3-268">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="5c6e3-269">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="5c6e3-269">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="5c6e3-270">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="5c6e3-270">AzureRM.Batch</span></span>
* <span data-ttu-id="5c6e3-271">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="5c6e3-271">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="5c6e3-272">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="5c6e3-272">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="5c6e3-273">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="5c6e3-273">AzureRM.Consumption</span></span>
* <span data-ttu-id="5c6e3-274">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="5c6e3-274">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="5c6e3-275">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c6e3-275">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="5c6e3-276">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="5c6e3-276">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="5c6e3-277">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="5c6e3-277">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="5c6e3-278">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="5c6e3-278">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="5c6e3-279">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="5c6e3-279">AzureRM.Network</span></span>
* <span data-ttu-id="5c6e3-280">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="5c6e3-280">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="5c6e3-281">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="5c6e3-281">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="5c6e3-282">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c6e3-282">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="5c6e3-283">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-283">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="5c6e3-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5c6e3-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="5c6e3-285">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-285">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="5c6e3-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5c6e3-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="5c6e3-287">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="5c6e3-287">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="5c6e3-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5c6e3-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="5c6e3-289">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c6e3-289">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="5c6e3-290">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="5c6e3-290">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="5c6e3-291">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="5c6e3-291">AzureRM.Sql</span></span>
* <span data-ttu-id="5c6e3-292">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="5c6e3-292">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="5c6e3-293">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-293">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="5c6e3-294">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-294">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="5c6e3-295">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-295">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="5c6e3-296">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="5c6e3-296">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="5c6e3-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c6e3-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="5c6e3-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5c6e3-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="5c6e3-299">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="5c6e3-299">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="5c6e3-300">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5c6e3-300">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="5c6e3-301">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c6e3-301">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="5c6e3-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5c6e3-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="5c6e3-303">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="5c6e3-303">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>