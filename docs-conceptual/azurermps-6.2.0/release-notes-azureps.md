---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: f90c77d8c9cd78315264fb0a0a58e047aefc5041
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821870"
---
# <a name="release-notes"></a><span data-ttu-id="2a419-103">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="2a419-103">Release notes</span></span>

<span data-ttu-id="2a419-104">Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.</span><span class="sxs-lookup"><span data-stu-id="2a419-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="620---june-2018"></a><span data-ttu-id="2a419-105">6.2.0 – 2018. június</span><span class="sxs-lookup"><span data-stu-id="2a419-105">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2a419-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2a419-106">AzureRM.Profile</span></span>
* <span data-ttu-id="2a419-107">Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során</span><span class="sxs-lookup"><span data-stu-id="2a419-107">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2a419-108">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2a419-108">AzureRM.Compute</span></span>
* <span data-ttu-id="2a419-109">VMSS VM frissítési funkciója</span><span class="sxs-lookup"><span data-stu-id="2a419-109">VMSS VM Update feature</span></span>
    - <span data-ttu-id="2a419-110">Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="2a419-110">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="2a419-111">A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez</span><span class="sxs-lookup"><span data-stu-id="2a419-111">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2a419-112">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2a419-112">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2a419-113">Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="2a419-113">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="2a419-114">Hozzá lett adva a gyári adattár konfigurálási művelete</span><span class="sxs-lookup"><span data-stu-id="2a419-114">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="2a419-115">Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez</span><span class="sxs-lookup"><span data-stu-id="2a419-115">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="2a419-116">Több modelltípus is frissült, a SecretBase-től az objektumig</span><span class="sxs-lookup"><span data-stu-id="2a419-116">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="2a419-117">A rendszer blobesemény-indítókkal bővült</span><span class="sxs-lookup"><span data-stu-id="2a419-117">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="2a419-118">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2a419-118">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2a419-119">A dokumentáció kimeneti példával bővült</span><span class="sxs-lookup"><span data-stu-id="2a419-119">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="2a419-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2a419-120">AzureRM.Network</span></span>
* <span data-ttu-id="2a419-121">Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon</span><span class="sxs-lookup"><span data-stu-id="2a419-121">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2a419-122">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2a419-122">AzureRM.Resources</span></span>
* <span data-ttu-id="2a419-123">Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát</span><span class="sxs-lookup"><span data-stu-id="2a419-123">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="2a419-124">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="2a419-124">AzureRM.Scheduler</span></span>
* <span data-ttu-id="2a419-125">Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat</span><span class="sxs-lookup"><span data-stu-id="2a419-125">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="2a419-126">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2a419-126">AzureRM.Sql</span></span>
* <span data-ttu-id="2a419-127">A következő parancsmagok az opcionális LicenseType paraméterrel frissültek</span><span class="sxs-lookup"><span data-stu-id="2a419-127">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="2a419-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2a419-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="2a419-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2a419-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="2a419-130">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="2a419-130">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="2a419-131">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2a419-131">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="2a419-132">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2a419-132">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2a419-133">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2a419-133">AzureRM.Websites</span></span>
* <span data-ttu-id="2a419-134">Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.</span><span class="sxs-lookup"><span data-stu-id="2a419-134">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="2a419-135">6.1.0 – 2018. május</span><span class="sxs-lookup"><span data-stu-id="2a419-135">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2a419-136">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2a419-136">AzureRM.Profile</span></span>
* <span data-ttu-id="2a419-137">Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven</span><span class="sxs-lookup"><span data-stu-id="2a419-137">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="2a419-138">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2a419-138">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2a419-139">Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="2a419-139">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="2a419-140">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2a419-140">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="2a419-141">Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="2a419-141">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="2a419-142">A Service Fabric háttérrendszer mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="2a419-142">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="2a419-143">Az Application Insights naplózó mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="2a419-143">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="2a419-144">Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="2a419-144">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="2a419-145">A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="2a419-145">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="2a419-146">Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="2a419-146">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="2a419-147">Az MSI-identitások mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="2a419-147">Added support for MSI identity</span></span>
* <span data-ttu-id="2a419-148">A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban</span><span class="sxs-lookup"><span data-stu-id="2a419-148">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="2a419-149">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="2a419-149">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="2a419-150">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a419-150">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="2a419-151">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="2a419-151">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="2a419-152">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="2a419-152">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="2a419-153">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="2a419-153">AzureRM.Batch</span></span>
* <span data-ttu-id="2a419-154">Új Get-AzureBatchPoolNodeCounts parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="2a419-154">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="2a419-155">Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása</span><span class="sxs-lookup"><span data-stu-id="2a419-155">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="2a419-156">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="2a419-156">AzureRM.Consumption</span></span>
* <span data-ttu-id="2a419-157">A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="2a419-157">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2a419-158">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2a419-158">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2a419-159">Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="2a419-159">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="2a419-160">A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása</span><span class="sxs-lookup"><span data-stu-id="2a419-160">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="2a419-161">A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása</span><span class="sxs-lookup"><span data-stu-id="2a419-161">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="2a419-162">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2a419-162">AzureRM.Network</span></span>
* <span data-ttu-id="2a419-163">A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra</span><span class="sxs-lookup"><span data-stu-id="2a419-163">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="2a419-164">Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához</span><span class="sxs-lookup"><span data-stu-id="2a419-164">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="2a419-165">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a419-165">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="2a419-166">Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.</span><span class="sxs-lookup"><span data-stu-id="2a419-166">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="2a419-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2a419-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="2a419-168">Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.</span><span class="sxs-lookup"><span data-stu-id="2a419-168">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="2a419-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2a419-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="2a419-170">Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="2a419-170">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="2a419-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2a419-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="2a419-172">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2a419-172">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="2a419-173">A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="2a419-173">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2a419-174">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2a419-174">AzureRM.Sql</span></span>
* <span data-ttu-id="2a419-175">A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását</span><span class="sxs-lookup"><span data-stu-id="2a419-175">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="2a419-176">A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="2a419-176">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="2a419-177">Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.</span><span class="sxs-lookup"><span data-stu-id="2a419-177">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="2a419-178">Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.</span><span class="sxs-lookup"><span data-stu-id="2a419-178">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="2a419-179">A frissített parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="2a419-179">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="2a419-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2a419-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="2a419-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2a419-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="2a419-182">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="2a419-182">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="2a419-183">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2a419-183">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="2a419-184">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2a419-184">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2a419-185">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2a419-185">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2a419-186">A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.</span><span class="sxs-lookup"><span data-stu-id="2a419-186">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>