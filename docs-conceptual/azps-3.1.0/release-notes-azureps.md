---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 2280b594ee9f525b2fa3175c917f6365cea354ba
ms.sourcegitcommit: 45e1823aa1a792840aa4829831b5f67a9d5d24a0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/26/2019
ms.locfileid: "74537121"
---
## <a name="310---november-2019"></a><span data-ttu-id="d4fa6-103">3.1.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="d4fa6-103">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d4fa6-104">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-104">Highlights since the last major release</span></span>
* <span data-ttu-id="d4fa6-105">Az.DataBoxEdge 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-105">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="d4fa6-106">Az.SqlVirtualMachine 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-106">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-107">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-108">A virtuális gépek Reapply funkciója</span><span class="sxs-lookup"><span data-stu-id="d4fa6-108">VM Reapply feature</span></span>
    - <span data-ttu-id="d4fa6-109">A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-109">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="d4fa6-110">A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-110">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="d4fa6-111">Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4fa6-111">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="d4fa6-112">Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-112">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="d4fa6-113">A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-113">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="d4fa6-114">A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-114">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="d4fa6-115">A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező</span><span class="sxs-lookup"><span data-stu-id="d4fa6-115">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="d4fa6-116">A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="d4fa6-116">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="d4fa6-117">A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-117">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="d4fa6-118">A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-118">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="d4fa6-119">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d4fa6-119">Az.DataBoxEdge</span></span>
* <span data-ttu-id="d4fa6-120">A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-120">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d4fa6-121">Megrendelés lekérése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-121">Get the Order</span></span>
* <span data-ttu-id="d4fa6-122">A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-122">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d4fa6-123">Új megrendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-123">Create new Order</span></span>
* <span data-ttu-id="d4fa6-124">A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-124">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d4fa6-125">Megrendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-125">Remove the Order</span></span>
* <span data-ttu-id="d4fa6-126">`New-AzDataBoxEdgeShare` parancsmag módosítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-126">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="d4fa6-127">Mostantól helyi megosztást hoz létre</span><span class="sxs-lookup"><span data-stu-id="d4fa6-127">Now creates Local Share</span></span>
* <span data-ttu-id="d4fa6-128">A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-128">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="d4fa6-129">Mostantól az IotRole leképezhető a Share-re</span><span class="sxs-lookup"><span data-stu-id="d4fa6-129">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="d4fa6-130">A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-130">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="d4fa6-131">Frissítések keresésének, letöltésének, telepítésének indítása az eszközön</span><span class="sxs-lookup"><span data-stu-id="d4fa6-131">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="d4fa6-132">A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-132">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d4fa6-133">Triggerek információinak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-133">Gets the information about Triggers</span></span>
* <span data-ttu-id="d4fa6-134">A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-134">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d4fa6-135">Új triggerek létrehozása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-135">Create new Triggers</span></span>
* <span data-ttu-id="d4fa6-136">A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-136">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d4fa6-137">Triggerek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-137">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4fa6-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4fa6-138">Az.DataFactory</span></span>
* <span data-ttu-id="d4fa6-139">Az ADF .Net SDK a 4.4.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d4fa6-139">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="d4fa6-140">Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-140">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4fa6-141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4fa6-141">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4fa6-142">Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d4fa6-142">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4fa6-143">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4fa6-143">Az.EventHub</span></span>
* <span data-ttu-id="d4fa6-144">A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-144">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4fa6-145">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-145">Az.FrontDoor</span></span>
* <span data-ttu-id="d4fa6-146">Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="d4fa6-146">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="d4fa6-147">A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="d4fa6-147">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="d4fa6-148">Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-148">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="d4fa6-149">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="d4fa6-149">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-150">Az.Network</span></span>
* <span data-ttu-id="d4fa6-151">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-151">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="d4fa6-152">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="d4fa6-152">Az.PrivateDns</span></span>
* <span data-ttu-id="d4fa6-153">A PrivateDns .net sdk frissült az 1.0.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="d4fa6-153">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4fa6-154">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-154">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4fa6-155">Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-155">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="d4fa6-156">Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-156">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="d4fa6-157">SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-157">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d4fa6-158">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d4fa6-158">Az.RedisCache</span></span>
* <span data-ttu-id="d4fa6-159">A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-159">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="d4fa6-160">Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-160">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="d4fa6-161">Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-161">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-162">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-162">Az.Resources</span></span>
- <span data-ttu-id="d4fa6-163">Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-163">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="d4fa6-164">Frissült a létrehozási szabályzat definíciójának súgóbeli példája</span><span class="sxs-lookup"><span data-stu-id="d4fa6-164">Updated create policy definition help example</span></span>
- <span data-ttu-id="d4fa6-165">Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-165">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="d4fa6-166">Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-166">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="d4fa6-167">A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-167">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-168">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-168">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-169">Az adatbázisbeli ReadReplicaCount mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-169">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="d4fa6-170">A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén</span><span class="sxs-lookup"><span data-stu-id="d4fa6-170">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="d4fa6-171">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="d4fa6-171">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="d4fa6-172">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d4fa6-172">General</span></span>
* <span data-ttu-id="d4fa6-173">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d4fa6-173">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4fa6-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-174">Az.Accounts</span></span>
* <span data-ttu-id="d4fa6-175">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-175">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d4fa6-176">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-176">Az.Advisor</span></span>
* <span data-ttu-id="d4fa6-177">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-177">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d4fa6-178">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4fa6-178">Az.Batch</span></span>
* <span data-ttu-id="d4fa6-179">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-179">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="d4fa6-180">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-180">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="d4fa6-181">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-181">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="d4fa6-182">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-182">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="d4fa6-183">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-183">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="d4fa6-184">Ezek az **New-AzBatchTask** `-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-184">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="d4fa6-185">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-185">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="d4fa6-186">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-186">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="d4fa6-187">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-187">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="d4fa6-188">A `PSApplication` **Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-188">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="d4fa6-189">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-189">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="d4fa6-190">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-190">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="d4fa6-191">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-191">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="d4fa6-192">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-192">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="d4fa6-193">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-193">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="d4fa6-194">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-194">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="d4fa6-195">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-195">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="d4fa6-196">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-196">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="d4fa6-197">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-197">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="d4fa6-198">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-198">This operation is no longer supported.</span></span>
* <span data-ttu-id="d4fa6-199">`PSCloudServiceConfiguration` `TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-199">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="d4fa6-200">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-200">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="d4fa6-201">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-201">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="d4fa6-202">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-202">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="d4fa6-203">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-203">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="d4fa6-204">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-204">New non-verified images are also now returned.</span></span> <span data-ttu-id="d4fa6-205">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-205">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="d4fa6-206">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-206">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="d4fa6-207">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-207">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="d4fa6-208">Ez a `PSNetworkSecurityGroupRule` `SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-208">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="d4fa6-209">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-209">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="d4fa6-210">Ezt a `PSTaskContainerSettings` `WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-210">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="d4fa6-211">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-211">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="d4fa6-212">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-212">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="d4fa6-213">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-213">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="d4fa6-214">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-214">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4fa6-215">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4fa6-215">Az.Cdn</span></span>
* <span data-ttu-id="d4fa6-216">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-216">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="d4fa6-217">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-217">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-218">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-219">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="d4fa6-219">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="d4fa6-220">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d4fa6-220">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="d4fa6-221">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="d4fa6-221">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="d4fa6-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d4fa6-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="d4fa6-223">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-223">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d4fa6-224">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-224">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="d4fa6-225">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="d4fa6-225">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="d4fa6-226">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-226">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="d4fa6-227">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="d4fa6-227">Breaking changes</span></span>
    - <span data-ttu-id="d4fa6-228">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="d4fa6-228">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="d4fa6-229">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-229">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4fa6-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4fa6-230">Az.DataFactory</span></span>
* <span data-ttu-id="d4fa6-231">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d4fa6-231">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4fa6-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4fa6-232">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4fa6-233">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="d4fa6-233">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="d4fa6-234">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-234">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="d4fa6-235">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-235">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="d4fa6-236">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-236">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="d4fa6-237">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-237">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="d4fa6-238">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-238">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4fa6-239">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-239">Az.FrontDoor</span></span>
* <span data-ttu-id="d4fa6-240">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-240">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d4fa6-241">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4fa6-241">Az.HDInsight</span></span>
* <span data-ttu-id="d4fa6-242">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-242">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="d4fa6-243">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-243">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="d4fa6-244">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="d4fa6-244">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="d4fa6-245">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-245">Removed five cmdlets:</span></span>
    - <span data-ttu-id="d4fa6-246">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d4fa6-246">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d4fa6-247">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d4fa6-247">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d4fa6-248">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d4fa6-248">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d4fa6-249">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d4fa6-249">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="d4fa6-250">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d4fa6-250">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="d4fa6-251">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-251">Added three cmdlets:</span></span>
    - <span data-ttu-id="d4fa6-252">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-252">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="d4fa6-253">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-253">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="d4fa6-254">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-254">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="d4fa6-255">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-255">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="d4fa6-256">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-256">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="d4fa6-257">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-257">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="d4fa6-258">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-258">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="d4fa6-259">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-259">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="d4fa6-260">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-260">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="d4fa6-261">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-261">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="d4fa6-262">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-262">Added some scenario test cases.</span></span>
* <span data-ttu-id="d4fa6-263">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-263">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4fa6-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4fa6-264">Az.IotHub</span></span>
* <span data-ttu-id="d4fa6-265">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-265">Breaking changes:</span></span>
    - <span data-ttu-id="d4fa6-266">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-266">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d4fa6-267">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-267">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d4fa6-268">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-268">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d4fa6-269">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-269">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d4fa6-270">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-270">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="d4fa6-271">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-271">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="d4fa6-272">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-272">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="d4fa6-273">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-273">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="d4fa6-274">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-274">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d4fa6-275">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-275">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d4fa6-276">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-276">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d4fa6-277">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-277">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4fa6-278">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-278">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4fa6-279">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-279">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="d4fa6-280">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-280">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="d4fa6-281">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-281">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="d4fa6-282">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-282">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="d4fa6-283">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-283">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="d4fa6-284">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-284">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="d4fa6-285">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-285">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="d4fa6-286">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-286">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="d4fa6-287">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="d4fa6-287">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-288">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-289">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="d4fa6-289">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-290">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-290">Az.Network</span></span>
* <span data-ttu-id="d4fa6-291">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-291">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="d4fa6-292">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-292">Updated cmdlet:</span></span>
        - <span data-ttu-id="d4fa6-293">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-293">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4fa6-294">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-294">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4fa6-295">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-295">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4fa6-296">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-296">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4fa6-297">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-297">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d4fa6-298">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-298">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="d4fa6-299">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-299">New cmdlet:</span></span>
        - <span data-ttu-id="d4fa6-300">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d4fa6-300">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="d4fa6-301">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-301">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="d4fa6-302">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-302">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="d4fa6-303">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-303">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="d4fa6-304">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-304">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="d4fa6-305">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="d4fa6-305">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="d4fa6-306">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-306">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="d4fa6-307">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-307">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="d4fa6-308">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-308">New cmdlets added:</span></span>
        - <span data-ttu-id="d4fa6-309">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-309">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="d4fa6-310">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4fa6-310">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d4fa6-311">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4fa6-311">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d4fa6-312">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4fa6-312">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d4fa6-313">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d4fa6-313">Set-AzVirtualHub</span></span>
* <span data-ttu-id="d4fa6-314">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-314">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="d4fa6-315">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-315">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d4fa6-316">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-316">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="d4fa6-317">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-317">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="d4fa6-318">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-318">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="d4fa6-319">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-319">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="d4fa6-320">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-320">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="d4fa6-321">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-321">New cmdlets added:</span></span>
        - <span data-ttu-id="d4fa6-322">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-322">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="d4fa6-323">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-323">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d4fa6-324">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-324">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d4fa6-325">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-325">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d4fa6-326">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-326">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d4fa6-327">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-327">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d4fa6-328">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-328">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="d4fa6-329">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-329">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="d4fa6-330">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-330">New cmdlets added:</span></span>
        - <span data-ttu-id="d4fa6-331">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="d4fa6-331">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="d4fa6-332">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="d4fa6-332">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="d4fa6-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="d4fa6-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="d4fa6-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="d4fa6-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="d4fa6-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="d4fa6-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="d4fa6-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4fa6-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="d4fa6-337">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-337">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d4fa6-338">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-338">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="d4fa6-339">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-339">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="d4fa6-340">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-340">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="d4fa6-341">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-341">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="d4fa6-342">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-342">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d4fa6-343">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-343">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="d4fa6-344">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-344">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="d4fa6-345">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="d4fa6-345">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="d4fa6-346">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-346">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="d4fa6-347">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-347">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="d4fa6-348">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-348">New cmdlets added:</span></span>
        - <span data-ttu-id="d4fa6-349">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d4fa6-349">New-AzIpGroup</span></span>
        - <span data-ttu-id="d4fa6-350">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d4fa6-350">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="d4fa6-351">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d4fa6-351">Get-AzIpGroup</span></span>
        - <span data-ttu-id="d4fa6-352">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d4fa6-352">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4fa6-353">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4fa6-353">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4fa6-354">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-354">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-355">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-355">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-356">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-356">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="d4fa6-357">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-357">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="d4fa6-358">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-358">Removed deprecated aliases:</span></span>
* <span data-ttu-id="d4fa6-359">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="d4fa6-359">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="d4fa6-360">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="d4fa6-360">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="d4fa6-361">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-361">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d4fa6-362">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-362">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="d4fa6-363">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="d4fa6-363">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="d4fa6-364">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-364">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4fa6-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-365">Az.Storage</span></span>
* <span data-ttu-id="d4fa6-366">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="d4fa6-366">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="d4fa6-367">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4fa6-367">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d4fa6-368">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4fa6-368">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d4fa6-369">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="d4fa6-369">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="d4fa6-370">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d4fa6-370">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="d4fa6-371">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d4fa6-371">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="d4fa6-372">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="d4fa6-372">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="d4fa6-373">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d4fa6-373">General</span></span>
* <span data-ttu-id="d4fa6-374">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="d4fa6-374">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4fa6-375">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-375">Az.Accounts</span></span>
* <span data-ttu-id="d4fa6-376">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-376">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d4fa6-377">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4fa6-377">Az.ApiManagement</span></span>
* <span data-ttu-id="d4fa6-378">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d4fa6-378">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="d4fa6-379">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="d4fa6-379">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4fa6-380">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4fa6-380">Az.Automation</span></span>
* <span data-ttu-id="d4fa6-381">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-381">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="d4fa6-382">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4fa6-382">Az.Batch</span></span>
* <span data-ttu-id="d4fa6-383">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-383">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-384">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-384">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-385">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-385">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="d4fa6-386">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-386">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="d4fa6-387">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-387">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="d4fa6-388">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-388">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4fa6-389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4fa6-389">Az.DataFactory</span></span>
* <span data-ttu-id="d4fa6-390">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-390">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="d4fa6-391">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-391">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="d4fa6-392">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d4fa6-392">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4fa6-393">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4fa6-393">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4fa6-394">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="d4fa6-394">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d4fa6-395">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d4fa6-395">Az.HealthcareApis</span></span>
* <span data-ttu-id="d4fa6-396">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d4fa6-396">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="d4fa6-397">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d4fa6-397">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="d4fa6-398">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-398">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="d4fa6-399">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-399">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4fa6-400">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4fa6-400">Az.IotHub</span></span>
* <span data-ttu-id="d4fa6-401">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="d4fa6-401">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="d4fa6-402">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4fa6-402">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="d4fa6-403">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-403">Az.Monitor</span></span>
* <span data-ttu-id="d4fa6-404">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="d4fa6-404">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="d4fa6-405">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-405">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="d4fa6-406">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-406">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="d4fa6-407">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-407">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-408">Az.Network</span></span>
* <span data-ttu-id="d4fa6-409">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-409">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="d4fa6-410">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-410">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="d4fa6-411">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-411">New cmdlets added:</span></span>
        - <span data-ttu-id="d4fa6-412">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="d4fa6-412">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="d4fa6-413">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-413">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d4fa6-414">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-414">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="d4fa6-415">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-415">Updated cmdlets:</span></span>
        - <span data-ttu-id="d4fa6-416">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-416">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d4fa6-417">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-417">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d4fa6-418">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-418">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d4fa6-419">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-419">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="d4fa6-420">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="d4fa6-420">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="d4fa6-421">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-421">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="d4fa6-422">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-422">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d4fa6-423">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d4fa6-423">Az.RedisCache</span></span>
* <span data-ttu-id="d4fa6-424">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-424">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-425">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-426">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-426">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4fa6-427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-427">Az.Storage</span></span>
* <span data-ttu-id="d4fa6-428">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-428">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="d4fa6-429">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="d4fa6-429">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d4fa6-430">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d4fa6-430">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="d4fa6-431">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="d4fa6-431">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d4fa6-432">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4fa6-432">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d4fa6-433">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d4fa6-433">Az.StorageSync</span></span>
* <span data-ttu-id="d4fa6-434">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-434">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4fa6-435">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4fa6-435">Az.Websites</span></span>
* <span data-ttu-id="d4fa6-436">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="d4fa6-436">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="d4fa6-437">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="d4fa6-437">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d4fa6-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4fa6-438">Az.ApiManagement</span></span>
* <span data-ttu-id="d4fa6-439">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="d4fa6-439">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="d4fa6-440">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-440">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="d4fa6-441">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-441">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4fa6-442">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4fa6-442">Az.Automation</span></span>
* <span data-ttu-id="d4fa6-443">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="d4fa6-443">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="d4fa6-444">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-444">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="d4fa6-445">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-445">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-446">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-447">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-447">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="d4fa6-448">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-448">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d4fa6-449">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-449">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="d4fa6-450">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-450">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="d4fa6-451">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-451">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="d4fa6-452">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-452">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="d4fa6-453">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-453">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="d4fa6-454">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-454">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="d4fa6-455">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-455">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4fa6-456">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4fa6-456">Az.DataFactory</span></span>
* <span data-ttu-id="d4fa6-457">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-457">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="d4fa6-458">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d4fa6-458">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d4fa6-459">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4fa6-459">Az.HDInsight</span></span>
* <span data-ttu-id="d4fa6-460">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-460">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4fa6-461">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4fa6-461">Az.IotHub</span></span>
* <span data-ttu-id="d4fa6-462">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-462">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="d4fa6-463">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-463">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="d4fa6-464">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-464">New cmdlets are:</span></span>
    - <span data-ttu-id="d4fa6-465">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d4fa6-465">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d4fa6-466">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d4fa6-466">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d4fa6-467">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d4fa6-467">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d4fa6-468">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d4fa6-468">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4fa6-469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-469">Az.Monitor</span></span>
* <span data-ttu-id="d4fa6-470">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="d4fa6-470">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="d4fa6-471">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-471">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="d4fa6-472">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-472">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="d4fa6-473">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-473">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="d4fa6-474">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-474">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="d4fa6-475">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-475">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="d4fa6-476">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-476">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="d4fa6-477">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-477">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="d4fa6-478">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-478">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d4fa6-479">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-479">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="d4fa6-480">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-480">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d4fa6-481">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-481">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="d4fa6-482">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-482">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="d4fa6-483">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="d4fa6-483">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="d4fa6-484">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="d4fa6-484">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="d4fa6-485">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="d4fa6-485">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="d4fa6-486">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="d4fa6-486">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="d4fa6-487">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-487">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="d4fa6-488">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-488">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="d4fa6-489">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-489">Overall improved help files</span></span>
* <span data-ttu-id="d4fa6-490">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="d4fa6-490">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-491">Az.Network</span></span>
* <span data-ttu-id="d4fa6-492">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="d4fa6-492">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="d4fa6-493">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="d4fa6-493">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="d4fa6-494">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-494">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="d4fa6-495">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-495">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="d4fa6-496">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-496">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="d4fa6-497">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-497">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="d4fa6-498">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-498">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="d4fa6-499">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-499">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="d4fa6-500">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-500">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="d4fa6-501">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="d4fa6-501">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="d4fa6-502">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-502">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="d4fa6-503">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="d4fa6-503">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="d4fa6-504">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-504">New cmdlets</span></span>
        - <span data-ttu-id="d4fa6-505">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="d4fa6-505">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="d4fa6-506">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-506">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="d4fa6-507">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-507">Updated cmdlet:</span></span>
        - <span data-ttu-id="d4fa6-508">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="d4fa6-508">New-VpnSite</span></span>
        - <span data-ttu-id="d4fa6-509">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="d4fa6-509">Update-VpnSite</span></span>
        - <span data-ttu-id="d4fa6-510">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-510">New-VpnConnection</span></span>
        - <span data-ttu-id="d4fa6-511">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-511">Update-VpnConnection</span></span>
* <span data-ttu-id="d4fa6-512">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="d4fa6-512">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4fa6-513">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-513">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4fa6-514">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="d4fa6-514">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="d4fa6-515">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-515">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-516">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-517">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-517">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4fa6-518">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4fa6-518">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4fa6-519">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="d4fa6-519">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="d4fa6-520">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-520">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="d4fa6-521">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d4fa6-521">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d4fa6-522">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d4fa6-522">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d4fa6-523">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d4fa6-523">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d4fa6-524">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d4fa6-524">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="d4fa6-525">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d4fa6-525">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d4fa6-526">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d4fa6-526">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d4fa6-527">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d4fa6-527">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d4fa6-528">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d4fa6-528">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d4fa6-529">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d4fa6-529">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="d4fa6-530">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d4fa6-530">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d4fa6-531">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d4fa6-531">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d4fa6-532">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d4fa6-532">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d4fa6-533">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="d4fa6-533">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="d4fa6-534">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-534">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d4fa6-535">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d4fa6-535">Az.SignalR</span></span>
* <span data-ttu-id="d4fa6-536">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-536">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-537">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-537">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-538">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="d4fa6-538">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="d4fa6-539">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-539">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="d4fa6-540">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-540">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="d4fa6-541">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-541">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="d4fa6-542">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-542">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4fa6-543">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-543">Az.Storage</span></span>
* <span data-ttu-id="d4fa6-544">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="d4fa6-544">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="d4fa6-545">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-545">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="d4fa6-546">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d4fa6-546">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="d4fa6-547">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d4fa6-547">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="d4fa6-548">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-548">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="d4fa6-549">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d4fa6-549">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="d4fa6-550">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-550">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="d4fa6-551">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d4fa6-551">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d4fa6-552">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d4fa6-552">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d4fa6-553">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d4fa6-553">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d4fa6-554">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d4fa6-554">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4fa6-555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4fa6-555">Az.Websites</span></span>
* <span data-ttu-id="d4fa6-556">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-556">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="d4fa6-557">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-557">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="d4fa6-558">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="d4fa6-558">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="d4fa6-559">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="d4fa6-559">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="d4fa6-560">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d4fa6-560">General</span></span>
* <span data-ttu-id="d4fa6-561">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-561">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4fa6-562">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-562">Az.Accounts</span></span>
* <span data-ttu-id="d4fa6-563">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="d4fa6-563">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="d4fa6-564">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d4fa6-564">Az.Aks</span></span>
* <span data-ttu-id="d4fa6-565">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-565">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="d4fa6-566">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="d4fa6-566">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d4fa6-567">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4fa6-567">Az.ApiManagement</span></span>
* <span data-ttu-id="d4fa6-568">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="d4fa6-568">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="d4fa6-569">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="d4fa6-569">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="d4fa6-570">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-570">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="d4fa6-571">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="d4fa6-571">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="d4fa6-572">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="d4fa6-572">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d4fa6-573">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4fa6-573">Az.Batch</span></span>
* <span data-ttu-id="d4fa6-574">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="d4fa6-574">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4fa6-575">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4fa6-575">Az.Cdn</span></span>
* <span data-ttu-id="d4fa6-576">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="d4fa6-576">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-577">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-578">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-578">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="d4fa6-579">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-579">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="d4fa6-580">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-580">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="d4fa6-581">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="d4fa6-581">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="d4fa6-582">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="d4fa6-582">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="d4fa6-583">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-583">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="d4fa6-584">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="d4fa6-584">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="d4fa6-585">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="d4fa6-585">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4fa6-586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4fa6-586">Az.DataFactory</span></span>
* <span data-ttu-id="d4fa6-587">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-587">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="d4fa6-588">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d4fa6-588">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="d4fa6-589">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="d4fa6-589">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="d4fa6-590">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="d4fa6-590">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4fa6-591">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4fa6-591">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4fa6-592">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-592">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4fa6-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4fa6-593">Az.EventHub</span></span>
* <span data-ttu-id="d4fa6-594">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-594">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="d4fa6-595">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="d4fa6-595">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="d4fa6-596">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-596">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="d4fa6-597">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="d4fa6-597">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="d4fa6-598">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d4fa6-598">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d4fa6-599">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="d4fa6-599">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4fa6-600">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-600">Az.Monitor</span></span>
* <span data-ttu-id="d4fa6-601">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-601">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-602">Az.Network</span></span>
* <span data-ttu-id="d4fa6-603">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-603">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="d4fa6-604">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-604">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="d4fa6-605">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-605">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="d4fa6-606">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="d4fa6-606">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="d4fa6-607">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-607">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="d4fa6-608">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-608">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="d4fa6-609">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-609">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4fa6-610">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4fa6-610">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4fa6-611">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d4fa6-611">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="d4fa6-612">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-612">Added example</span></span>
    - <span data-ttu-id="d4fa6-613">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="d4fa6-613">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="d4fa6-614">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-614">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="d4fa6-615">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-615">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4fa6-616">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-616">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4fa6-617">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="d4fa6-617">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-618">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-619">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="d4fa6-619">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="d4fa6-620">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-620">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="d4fa6-621">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="d4fa6-621">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="d4fa6-622">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-622">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4fa6-623">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4fa6-623">Az.ServiceBus</span></span>
* <span data-ttu-id="d4fa6-624">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-624">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="d4fa6-625">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="d4fa6-625">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="d4fa6-626">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="d4fa6-626">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="d4fa6-627">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4fa6-627">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4fa6-628">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-628">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="d4fa6-629">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-629">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="d4fa6-630">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="d4fa6-630">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="d4fa6-631">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-631">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="d4fa6-632">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="d4fa6-632">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="d4fa6-633">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="d4fa6-633">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-634">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-635">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-635">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4fa6-636">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-636">Az.Storage</span></span>
* <span data-ttu-id="d4fa6-637">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="d4fa6-637">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="d4fa6-638">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-638">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="d4fa6-639">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d4fa6-639">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="d4fa6-640">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d4fa6-640">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="d4fa6-641">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-641">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="d4fa6-642">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d4fa6-642">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4fa6-643">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4fa6-643">Az.Websites</span></span>
* <span data-ttu-id="d4fa6-644">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-644">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="d4fa6-645">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="d4fa6-645">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4fa6-646">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-646">Az.Accounts</span></span>
* <span data-ttu-id="d4fa6-647">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-647">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="d4fa6-648">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d4fa6-648">Az.ApplicationInsights</span></span>
* <span data-ttu-id="d4fa6-649">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-649">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="d4fa6-650">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4fa6-650">Az.Automation</span></span>
* <span data-ttu-id="d4fa6-651">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-651">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4fa6-652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-652">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4fa6-653">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-653">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-654">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-655">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-655">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d4fa6-656">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d4fa6-656">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d4fa6-657">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-657">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="d4fa6-658">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="d4fa6-658">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4fa6-659">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4fa6-659">Az.DataFactory</span></span>
* <span data-ttu-id="d4fa6-660">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="d4fa6-660">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="d4fa6-661">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-661">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4fa6-662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4fa6-662">Az.EventHub</span></span>
* <span data-ttu-id="d4fa6-663">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="d4fa6-663">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d4fa6-664">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="d4fa6-664">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4fa6-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4fa6-665">Az.KeyVault</span></span>
* <span data-ttu-id="d4fa6-666">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-666">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d4fa6-667">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d4fa6-667">Az.LogicApp</span></span>
* <span data-ttu-id="d4fa6-668">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="d4fa6-668">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="d4fa6-669">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-669">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="d4fa6-670">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-670">Az.ManagedServices</span></span>
* <span data-ttu-id="d4fa6-671">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-671">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-672">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-672">Az.Network</span></span>
* <span data-ttu-id="d4fa6-673">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-673">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="d4fa6-674">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-674">New cmdlets</span></span>
        - <span data-ttu-id="d4fa6-675">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4fa6-675">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d4fa6-676">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4fa6-676">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d4fa6-677">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-677">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4fa6-678">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-678">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4fa6-679">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-679">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4fa6-680">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-680">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d4fa6-681">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="d4fa6-681">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="d4fa6-682">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4fa6-682">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="d4fa6-683">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-683">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="d4fa6-684">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="d4fa6-684">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="d4fa6-685">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-685">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="d4fa6-686">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-686">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="d4fa6-687">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-687">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="d4fa6-688">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-688">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="d4fa6-689">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-689">Updated cmdlets</span></span>
        - <span data-ttu-id="d4fa6-690">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-690">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d4fa6-691">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-691">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d4fa6-692">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-692">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d4fa6-693">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="d4fa6-693">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d4fa6-694">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-694">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="d4fa6-695">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-695">Updated cmdlet:</span></span>
        - <span data-ttu-id="d4fa6-696">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-696">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d4fa6-697">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-697">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d4fa6-698">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-698">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="d4fa6-699">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-699">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="d4fa6-700">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-700">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="d4fa6-701">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-701">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4fa6-702">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4fa6-702">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4fa6-703">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-703">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="d4fa6-704">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-704">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4fa6-705">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-705">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4fa6-706">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-706">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d4fa6-707">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-707">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="d4fa6-708">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-708">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="d4fa6-709">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-709">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d4fa6-710">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-710">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="d4fa6-711">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-711">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d4fa6-712">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-712">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="d4fa6-713">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-713">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d4fa6-714">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-714">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="d4fa6-715">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-715">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-716">Az.Resources</span></span>
- <span data-ttu-id="d4fa6-717">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-717">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="d4fa6-718">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="d4fa6-718">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4fa6-719">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4fa6-719">Az.ServiceBus</span></span>
* <span data-ttu-id="d4fa6-720">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="d4fa6-720">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d4fa6-721">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="d4fa6-721">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-722">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-722">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-723">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-723">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="d4fa6-724">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-724">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="d4fa6-725">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-725">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4fa6-726">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-726">Az.Storage</span></span>
* <span data-ttu-id="d4fa6-727">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="d4fa6-727">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d4fa6-728">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d4fa6-728">Az.StorageSync</span></span>
* <span data-ttu-id="d4fa6-729">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-729">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="d4fa6-730">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-730">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4fa6-731">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4fa6-731">Az.Websites</span></span>
* <span data-ttu-id="d4fa6-732">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="d4fa6-732">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="d4fa6-733">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-733">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="d4fa6-734">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-734">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="d4fa6-735">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="d4fa6-735">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4fa6-736">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-736">Az.Accounts</span></span>
* <span data-ttu-id="d4fa6-737">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-737">Add support for profile cmdlets</span></span>
* <span data-ttu-id="d4fa6-738">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-738">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="d4fa6-739">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="d4fa6-739">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d4fa6-740">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-740">Az.Advisor</span></span>
* <span data-ttu-id="d4fa6-741">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-741">GA release of Az.Advisor</span></span>
* <span data-ttu-id="d4fa6-742">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="d4fa6-742">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d4fa6-743">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4fa6-743">Az.ApiManagement</span></span>
* <span data-ttu-id="d4fa6-744">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="d4fa6-744">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="d4fa6-745">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d4fa6-745">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="d4fa6-746">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-746">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="d4fa6-747">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-747">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="d4fa6-748">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="d4fa6-748">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="d4fa6-749">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d4fa6-749">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="d4fa6-750">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-750">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4fa6-751">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4fa6-751">Az.Automation</span></span>
* <span data-ttu-id="d4fa6-752">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-752">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-753">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-753">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-754">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-754">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4fa6-755">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4fa6-755">Az.DataFactory</span></span>
* <span data-ttu-id="d4fa6-756">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-756">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d4fa6-757">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d4fa6-757">Az.EventGrid</span></span>
* <span data-ttu-id="d4fa6-758">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="d4fa6-758">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4fa6-759">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4fa6-759">Az.IotHub</span></span>
* <span data-ttu-id="d4fa6-760">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-760">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-761">Az.Network</span></span>
* <span data-ttu-id="d4fa6-762">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-762">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="d4fa6-763">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-763">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4fa6-764">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4fa6-764">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4fa6-765">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-765">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="d4fa6-766">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="d4fa6-766">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4fa6-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4fa6-767">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4fa6-768">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="d4fa6-768">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4fa6-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-769">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4fa6-770">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-770">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-771">Az.Resources</span></span>
    - <span data-ttu-id="d4fa6-772">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-772">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="d4fa6-773">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-773">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="d4fa6-774">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-774">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="d4fa6-775">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-775">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4fa6-776">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4fa6-776">Az.ServiceBus</span></span>
* <span data-ttu-id="d4fa6-777">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-777">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-778">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-778">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-779">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-779">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="d4fa6-780">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-780">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="d4fa6-781">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d4fa6-781">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d4fa6-782">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d4fa6-782">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d4fa6-783">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d4fa6-783">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d4fa6-784">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d4fa6-784">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d4fa6-785">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d4fa6-785">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d4fa6-786">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d4fa6-786">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="d4fa6-787">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="d4fa6-787">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4fa6-788">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-788">Az.Storage</span></span>
* <span data-ttu-id="d4fa6-789">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-789">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="d4fa6-790">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d4fa6-790">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="d4fa6-791">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="d4fa6-791">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="d4fa6-792">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="d4fa6-792">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="d4fa6-793">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="d4fa6-793">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="d4fa6-794">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4fa6-794">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d4fa6-795">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4fa6-795">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d4fa6-796">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-796">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="d4fa6-797">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d4fa6-797">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="d4fa6-798">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d4fa6-798">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d4fa6-799">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d4fa6-799">Az.StorageSync</span></span>
* <span data-ttu-id="d4fa6-800">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="d4fa6-800">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="d4fa6-801">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="d4fa6-801">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4fa6-802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-802">Az.Accounts</span></span>
* <span data-ttu-id="d4fa6-803">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-803">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="d4fa6-804">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="d4fa6-804">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="d4fa6-805">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-805">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="d4fa6-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d4fa6-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="d4fa6-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="d4fa6-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-808">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-808">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-809">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-809">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="d4fa6-810">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="d4fa6-810">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="d4fa6-811">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d4fa6-811">Az.Dns</span></span>
* <span data-ttu-id="d4fa6-812">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-812">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d4fa6-813">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d4fa6-813">Az.EventGrid</span></span>
* <span data-ttu-id="d4fa6-814">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-814">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="d4fa6-815">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-815">New cmdlets:</span></span>
    - <span data-ttu-id="d4fa6-816">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d4fa6-816">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d4fa6-817">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-817">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d4fa6-818">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d4fa6-818">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d4fa6-819">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-819">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="d4fa6-820">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d4fa6-820">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d4fa6-821">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-821">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d4fa6-822">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d4fa6-822">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d4fa6-823">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-823">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d4fa6-824">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d4fa6-824">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d4fa6-825">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-825">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="d4fa6-826">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-826">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d4fa6-827">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-827">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="d4fa6-828">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d4fa6-828">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="d4fa6-829">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="d4fa6-829">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="d4fa6-830">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-830">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d4fa6-831">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-831">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="d4fa6-832">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-832">Updated cmdlets:</span></span>
    - <span data-ttu-id="d4fa6-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="d4fa6-834">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-834">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d4fa6-835">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-835">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d4fa6-836">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-836">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="d4fa6-837">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-837">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="d4fa6-838">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="d4fa6-838">Event subscription expiration date,</span></span>
            - <span data-ttu-id="d4fa6-839">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-839">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="d4fa6-840">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-840">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="d4fa6-841">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-841">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="d4fa6-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="d4fa6-843">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-843">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="d4fa6-844">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d4fa6-844">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="d4fa6-845">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-845">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="d4fa6-846">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-846">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4fa6-847">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-847">Az.FrontDoor</span></span>
* <span data-ttu-id="d4fa6-848">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="d4fa6-848">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="d4fa6-849">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="d4fa6-849">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="d4fa6-850">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="d4fa6-850">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="d4fa6-851">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-851">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-852">Az.Network</span></span>
* <span data-ttu-id="d4fa6-853">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-853">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="d4fa6-854">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-854">New cmdlets</span></span>
        - <span data-ttu-id="d4fa6-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="d4fa6-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="d4fa6-856">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-856">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="d4fa6-857">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-857">New cmdlets</span></span> 
        - <span data-ttu-id="d4fa6-858">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d4fa6-858">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="d4fa6-859">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-859">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="d4fa6-860">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-860">New cmdlets</span></span> 
        - <span data-ttu-id="d4fa6-861">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4fa6-861">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="d4fa6-862">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4fa6-862">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d4fa6-863">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d4fa6-863">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d4fa6-864">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-864">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="d4fa6-865">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-865">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d4fa6-866">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-866">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="d4fa6-867">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-867">New cmdlets</span></span>
        - <span data-ttu-id="d4fa6-868">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4fa6-868">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d4fa6-869">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4fa6-869">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d4fa6-870">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4fa6-870">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d4fa6-871">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-871">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="d4fa6-872">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="d4fa6-872">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="d4fa6-873">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-873">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="d4fa6-874">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-874">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="d4fa6-875">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-875">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="d4fa6-876">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-876">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="d4fa6-877">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="d4fa6-877">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="d4fa6-878">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="d4fa6-878">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="d4fa6-879">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-879">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="d4fa6-880">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-880">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="d4fa6-881">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-881">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="d4fa6-882">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-882">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="d4fa6-883">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-883">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="d4fa6-884">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="d4fa6-884">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="d4fa6-885">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-885">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="d4fa6-886">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-886">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="d4fa6-887">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="d4fa6-887">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="d4fa6-888">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="d4fa6-888">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="d4fa6-889">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="d4fa6-889">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="d4fa6-890">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="d4fa6-890">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="d4fa6-891">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-891">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="d4fa6-892">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-892">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d4fa6-893">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-893">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d4fa6-894">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-894">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4fa6-895">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4fa6-895">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4fa6-896">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-896">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-897">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-898">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-898">Support for additional Template Export options</span></span>
    - <span data-ttu-id="d4fa6-899">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-899">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d4fa6-900">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-900">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d4fa6-901">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-901">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4fa6-902">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4fa6-902">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4fa6-903">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="d4fa6-903">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-904">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-905">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="d4fa6-905">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="d4fa6-906">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="d4fa6-906">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="d4fa6-907">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-907">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="d4fa6-908">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d4fa6-908">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d4fa6-909">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d4fa6-909">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d4fa6-910">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d4fa6-910">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d4fa6-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d4fa6-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="d4fa6-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d4fa6-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4fa6-913">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-913">Az.Storage</span></span>
* <span data-ttu-id="d4fa6-914">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-914">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="d4fa6-915">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4fa6-915">New-AzStorageAccount</span></span>
* <span data-ttu-id="d4fa6-916">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-916">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="d4fa6-917">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d4fa6-917">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4fa6-918">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4fa6-918">Az.Websites</span></span>
* <span data-ttu-id="d4fa6-919">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="d4fa6-919">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="d4fa6-920">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-920">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="d4fa6-921">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="d4fa6-921">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="d4fa6-922">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4fa6-922">Az.Cdn</span></span>
* <span data-ttu-id="d4fa6-923">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="d4fa6-923">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-924">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-925">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-925">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="d4fa6-926">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d4fa6-926">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4fa6-927">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4fa6-927">Az.EventHub</span></span>
* <span data-ttu-id="d4fa6-928">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="d4fa6-928">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="d4fa6-929">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="d4fa6-929">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-930">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-930">Az.Network</span></span>
* <span data-ttu-id="d4fa6-931">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="d4fa6-931">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="d4fa6-932">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-932">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4fa6-933">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4fa6-933">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4fa6-934">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-934">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4fa6-935">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-935">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4fa6-936">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="d4fa6-936">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4fa6-937">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4fa6-937">Az.ServiceBus</span></span>
* <span data-ttu-id="d4fa6-938">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="d4fa6-938">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4fa6-939">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4fa6-939">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4fa6-940">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-940">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="d4fa6-941">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-941">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-942">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-942">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-943">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-943">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="d4fa6-944">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-944">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d4fa6-945">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="d4fa6-945">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="d4fa6-946">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-946">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4fa6-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4fa6-947">Az.Websites</span></span>
* <span data-ttu-id="d4fa6-948">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="d4fa6-948">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="d4fa6-949">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="d4fa6-949">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d4fa6-950">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4fa6-950">Az.ApiManagement</span></span>
* <span data-ttu-id="d4fa6-951">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-951">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="d4fa6-952">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-952">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="d4fa6-953">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-953">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="d4fa6-954">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-954">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="d4fa6-955">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-955">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="d4fa6-956">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-956">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="d4fa6-957">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="d4fa6-957">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="d4fa6-958">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="d4fa6-958">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="d4fa6-959">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-959">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="d4fa6-960">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-960">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="d4fa6-961">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-961">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="d4fa6-962">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-962">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="d4fa6-963">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-963">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="d4fa6-964">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-964">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="d4fa6-965">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-965">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="d4fa6-966">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-966">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="d4fa6-967">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-967">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="d4fa6-968">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-968">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="d4fa6-969">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-969">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="d4fa6-970">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-970">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="d4fa6-971">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-971">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="d4fa6-972">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-972">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="d4fa6-973">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-973">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="d4fa6-974">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-974">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="d4fa6-975">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="d4fa6-975">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="d4fa6-976">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="d4fa6-976">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="d4fa6-977">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-977">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="d4fa6-978">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-978">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="d4fa6-979">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-979">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="d4fa6-980">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-980">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="d4fa6-981">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-981">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="d4fa6-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="d4fa6-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="d4fa6-983">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-983">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="d4fa6-984">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-984">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d4fa6-985">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="d4fa6-985">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="d4fa6-986">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-986">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="d4fa6-987">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-987">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="d4fa6-988">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-988">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="d4fa6-989">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-989">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="d4fa6-990">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-990">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="d4fa6-991">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="d4fa6-991">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d4fa6-992">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-992">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d4fa6-993">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="d4fa6-993">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="d4fa6-994">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="d4fa6-994">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="d4fa6-995">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-995">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d4fa6-996">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="d4fa6-996">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d4fa6-997">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="d4fa6-997">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="d4fa6-998">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="d4fa6-998">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="d4fa6-999">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-999">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="d4fa6-1000">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1000">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="d4fa6-1001">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1001">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="d4fa6-1002">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1002">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="d4fa6-1003">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1003">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="d4fa6-1004">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1004">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="d4fa6-1005">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1005">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="d4fa6-1006">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1006">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="d4fa6-1007">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1007">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d4fa6-1008">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1008">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d4fa6-1009">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1009">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d4fa6-1010">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1010">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d4fa6-1011">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1011">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d4fa6-1012">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1012">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d4fa6-1013">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1013">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d4fa6-1014">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1014">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d4fa6-1015">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1015">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="d4fa6-1016">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1016">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="d4fa6-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="d4fa6-1018">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1018">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="d4fa6-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="d4fa6-1020">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1020">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="d4fa6-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="d4fa6-1022">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1022">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="d4fa6-1023">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1023">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="d4fa6-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="d4fa6-1025">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1025">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="d4fa6-1026">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1026">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="d4fa6-1027">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1027">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4fa6-1028">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1028">Az.Automation</span></span>
* <span data-ttu-id="d4fa6-1029">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1029">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="d4fa6-1030">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1030">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="d4fa6-1031">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1031">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="d4fa6-1032">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1032">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="d4fa6-1033">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1033">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="d4fa6-1034">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1034">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="d4fa6-1035">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1035">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1036">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-1037">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1037">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="d4fa6-1038">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1038">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4fa6-1039">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1039">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4fa6-1040">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1040">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4fa6-1041">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1041">Az.Monitor</span></span>
* <span data-ttu-id="d4fa6-1042">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1042">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-1043">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1043">Az.Network</span></span>
* <span data-ttu-id="d4fa6-1044">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1044">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="d4fa6-1045">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1045">Updated cmdlet:</span></span>
        - <span data-ttu-id="d4fa6-1046">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1046">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="d4fa6-1047">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1047">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1048">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-1049">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1049">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1050">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-1051">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1051">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="d4fa6-1052">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1052">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4fa6-1053">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1053">Az.Accounts</span></span>
* <span data-ttu-id="d4fa6-1054">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1054">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4fa6-1055">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1055">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4fa6-1056">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1056">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="d4fa6-1057">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1057">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-1058">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1058">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-1059">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1059">Proximity placement group feature.</span></span>
    - <span data-ttu-id="d4fa6-1060">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1060">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="d4fa6-1061">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1061">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="d4fa6-1062">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1062">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="d4fa6-1063">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1063">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="d4fa6-1064">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1064">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="d4fa6-1065">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1065">Breaking changes</span></span>
    - <span data-ttu-id="d4fa6-1066">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1066">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="d4fa6-1067">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1067">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d4fa6-1068">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1068">Az.DeploymentManager</span></span>
* <span data-ttu-id="d4fa6-1069">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1069">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="d4fa6-1070">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1070">Az.Dns</span></span>
* <span data-ttu-id="d4fa6-1071">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1071">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="d4fa6-1072">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1072">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="d4fa6-1073">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1073">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d4fa6-1074">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1074">Az.FrontDoor</span></span>
* <span data-ttu-id="d4fa6-1075">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1075">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="d4fa6-1076">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1076">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="d4fa6-1077">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1077">Az.HDInsight</span></span>
* <span data-ttu-id="d4fa6-1078">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1078">Removed two cmdlets:</span></span>
    - <span data-ttu-id="d4fa6-1079">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1079">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="d4fa6-1080">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1080">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d4fa6-1081">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1081">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d4fa6-1082">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1082">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="d4fa6-1083">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1083">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="d4fa6-1084">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1084">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4fa6-1085">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1085">Az.Monitor</span></span>
* <span data-ttu-id="d4fa6-1086">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1086">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="d4fa6-1087">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1087">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="d4fa6-1088">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1088">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="d4fa6-1089">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1089">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="d4fa6-1090">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1090">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="d4fa6-1091">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1091">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="d4fa6-1092">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1092">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="d4fa6-1093">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1093">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d4fa6-1094">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1094">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d4fa6-1095">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1095">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d4fa6-1096">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1096">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d4fa6-1097">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1097">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d4fa6-1098">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1098">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="d4fa6-1099">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1099">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1100">Az.Network</span></span>
* <span data-ttu-id="d4fa6-1101">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1101">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="d4fa6-1102">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1102">New cmdlets</span></span>
        - <span data-ttu-id="d4fa6-1103">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1103">New-AzNatGateway</span></span>
        - <span data-ttu-id="d4fa6-1104">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1104">Get-AzNatGateway</span></span>
        - <span data-ttu-id="d4fa6-1105">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1105">Set-AzNatGateway</span></span>
        - <span data-ttu-id="d4fa6-1106">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1106">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="d4fa6-1107">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1107">Updated cmdlets</span></span>
        - <span data-ttu-id="d4fa6-1108">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1108">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="d4fa6-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="d4fa6-1110">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1110">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="d4fa6-1111">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1111">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="d4fa6-1112">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1112">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4fa6-1113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1113">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4fa6-1114">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1114">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="d4fa6-1115">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1115">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="d4fa6-1116">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1116">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4fa6-1117">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1117">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4fa6-1118">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1118">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="d4fa6-1119">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1119">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="d4fa6-1120">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1120">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="d4fa6-1121">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1121">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="d4fa6-1122">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1122">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="d4fa6-1123">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1123">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="d4fa6-1124">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1124">Az.Relay</span></span>
* <span data-ttu-id="d4fa6-1125">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1125">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4fa6-1126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1126">Az.ServiceBus</span></span>
* <span data-ttu-id="d4fa6-1127">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1127">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4fa6-1128">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1128">Az.Storage</span></span>
* <span data-ttu-id="d4fa6-1129">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1129">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="d4fa6-1130">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1130">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="d4fa6-1131">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1131">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="d4fa6-1132">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1132">New-AzStorageAccount</span></span>
* <span data-ttu-id="d4fa6-1133">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1133">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="d4fa6-1134">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1134">New-AzStorageAccount</span></span>
    - <span data-ttu-id="d4fa6-1135">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1135">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="d4fa6-1136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1136">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4fa6-1137">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1137">Az.Websites</span></span>
* <span data-ttu-id="d4fa6-1138">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1138">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="d4fa6-1139">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1139">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="d4fa6-1140">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1140">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d4fa6-1141">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1141">Highlights since the last major release</span></span>
* <span data-ttu-id="d4fa6-1142">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1142">General availability of `Az` module</span></span>
* <span data-ttu-id="d4fa6-1143">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1143">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d4fa6-1144">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1144">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d4fa6-1145">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1145">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d4fa6-1146">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1146">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d4fa6-1147">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1147">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d4fa6-1148">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1148">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4fa6-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1149">Az.Accounts</span></span>
* <span data-ttu-id="d4fa6-1150">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1150">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d4fa6-1151">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1151">Az.Batch</span></span>
* <span data-ttu-id="d4fa6-1152">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4fa6-1153">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1153">Az.Cdn</span></span>
* <span data-ttu-id="d4fa6-1154">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1154">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4fa6-1155">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1155">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4fa6-1156">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-1157">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1157">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-1158">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1158">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="d4fa6-1159">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4fa6-1160">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1160">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4fa6-1161">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1161">Az.DataFactory</span></span>
* <span data-ttu-id="d4fa6-1162">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1162">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4fa6-1163">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1163">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4fa6-1164">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d4fa6-1165">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1165">Az.EventGrid</span></span>
* <span data-ttu-id="d4fa6-1166">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1166">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4fa6-1167">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1167">Az.EventHub</span></span>
* <span data-ttu-id="d4fa6-1168">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1168">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="d4fa6-1169">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1169">Az.HDInsight</span></span>
* <span data-ttu-id="d4fa6-1170">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1170">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4fa6-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1171">Az.IotHub</span></span>
* <span data-ttu-id="d4fa6-1172">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4fa6-1173">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1173">Az.KeyVault</span></span>
* <span data-ttu-id="d4fa6-1174">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1174">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4fa6-1175">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1175">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d4fa6-1176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1176">Az.MachineLearning</span></span>
* <span data-ttu-id="d4fa6-1177">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="d4fa6-1178">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1178">Az.Media</span></span>
* <span data-ttu-id="d4fa6-1179">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4fa6-1180">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1180">Az.Monitor</span></span>
  * <span data-ttu-id="d4fa6-1181">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1181">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="d4fa6-1182">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1182">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="d4fa6-1183">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1183">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="d4fa6-1184">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1184">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d4fa6-1185">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1185">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d4fa6-1186">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1186">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="d4fa6-1187">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1187">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-1188">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1188">Az.Network</span></span>
* <span data-ttu-id="d4fa6-1189">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1189">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4fa6-1190">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1190">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="d4fa6-1191">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1191">Az.NotificationHubs</span></span>
* <span data-ttu-id="d4fa6-1192">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1192">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4fa6-1193">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1193">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4fa6-1194">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1194">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="d4fa6-1195">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1195">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="d4fa6-1196">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1196">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4fa6-1197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1197">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4fa6-1198">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4fa6-1199">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1199">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="d4fa6-1200">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1200">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="d4fa6-1201">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1201">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d4fa6-1202">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1202">Az.RedisCache</span></span>
* <span data-ttu-id="d4fa6-1203">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-1204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1204">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-1205">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1205">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-1206">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1206">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-1207">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1207">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="d4fa6-1208">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4fa6-1209">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1209">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="d4fa6-1210">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1210">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="d4fa6-1211">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1211">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="d4fa6-1212">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1212">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="d4fa6-1213">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1213">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4fa6-1214">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1214">Az.Websites</span></span>
* <span data-ttu-id="d4fa6-1215">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1215">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="d4fa6-1216">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1216">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d4fa6-1217">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1217">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="d4fa6-1218">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1218">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="d4fa6-1219">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1219">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d4fa6-1220">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1220">Highlights since the last major release</span></span>
* <span data-ttu-id="d4fa6-1221">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1221">General availability of `Az` module</span></span>
* <span data-ttu-id="d4fa6-1222">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1222">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d4fa6-1223">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1223">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d4fa6-1224">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1224">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d4fa6-1225">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1225">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d4fa6-1226">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1226">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d4fa6-1227">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1227">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d4fa6-1228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1228">Az.Accounts</span></span>
* <span data-ttu-id="d4fa6-1229">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1229">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d4fa6-1230">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1230">Az.AnalysisServices</span></span>
* <span data-ttu-id="d4fa6-1231">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1231">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="d4fa6-1232">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1232">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4fa6-1233">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1233">Az.Automation</span></span>
* <span data-ttu-id="d4fa6-1234">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1234">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="d4fa6-1235">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1235">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="d4fa6-1236">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1236">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-1237">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1237">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-1238">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1238">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d4fa6-1239">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1239">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="d4fa6-1240">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1240">Az.ContainerInstance</span></span>
* <span data-ttu-id="d4fa6-1241">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1241">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4fa6-1242">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1242">Az.DataFactory</span></span>
* <span data-ttu-id="d4fa6-1243">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1243">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="d4fa6-1244">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1244">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-1245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1245">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-1246">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1246">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="d4fa6-1247">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1247">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="d4fa6-1248">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1248">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="d4fa6-1249">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1249">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="d4fa6-1250">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1250">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="d4fa6-1251">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1251">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1252">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-1253">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1253">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4fa6-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1254">Az.Storage</span></span>
* <span data-ttu-id="d4fa6-1255">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1255">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="d4fa6-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="d4fa6-1257">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1257">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="d4fa6-1258">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1258">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d4fa6-1259">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1259">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d4fa6-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="d4fa6-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="d4fa6-1262">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1262">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="d4fa6-1263">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1263">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d4fa6-1264">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1264">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d4fa6-1265">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1265">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="d4fa6-1266">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1266">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="d4fa6-1267">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1267">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d4fa6-1268">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1268">Highlights since the last major release</span></span>
* <span data-ttu-id="d4fa6-1269">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1269">General availability of `Az` module</span></span>
* <span data-ttu-id="d4fa6-1270">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1270">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d4fa6-1271">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1271">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d4fa6-1272">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1272">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d4fa6-1273">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1273">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d4fa6-1274">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1274">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d4fa6-1275">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1275">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4fa6-1276">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1276">Az.Automation</span></span>
* <span data-ttu-id="d4fa6-1277">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1277">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="d4fa6-1278">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1278">Dynamic grouping</span></span>
    * <span data-ttu-id="d4fa6-1279">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1279">Pre-Post script</span></span>
    * <span data-ttu-id="d4fa6-1280">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1280">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-1281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1281">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-1282">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1282">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="d4fa6-1283">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1283">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4fa6-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1284">Az.KeyVault</span></span>
* <span data-ttu-id="d4fa6-1285">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1285">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-1286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1286">Az.Network</span></span>
* <span data-ttu-id="d4fa6-1287">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1287">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="d4fa6-1288">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1288">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4fa6-1289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1289">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4fa6-1290">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1290">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="d4fa6-1291">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1291">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1292">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-1293">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1293">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="d4fa6-1294">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1294">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-1295">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1295">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-1296">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1296">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4fa6-1297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1297">Az.Storage</span></span>
* <span data-ttu-id="d4fa6-1298">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1298">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="d4fa6-1299">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1299">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d4fa6-1300">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1300">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d4fa6-1301">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1301">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d4fa6-1302">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1302">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="d4fa6-1303">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1303">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="d4fa6-1304">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1304">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4fa6-1305">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1305">Az.Websites</span></span>
* <span data-ttu-id="d4fa6-1306">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1306">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="d4fa6-1307">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1307">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4fa6-1308">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1308">Az.Accounts</span></span>
* <span data-ttu-id="d4fa6-1309">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1309">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="d4fa6-1310">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1310">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4fa6-1311">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1311">Az.Automation</span></span>
* <span data-ttu-id="d4fa6-1312">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1312">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="d4fa6-1313">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1313">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="d4fa6-1314">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1314">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4fa6-1315">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1315">Az.Cdn</span></span>
* <span data-ttu-id="d4fa6-1316">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1316">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-1317">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1317">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-1318">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1318">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4fa6-1319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1319">Az.DataFactory</span></span>
* <span data-ttu-id="d4fa6-1320">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1320">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d4fa6-1321">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1321">Az.LogicApp</span></span>
* <span data-ttu-id="d4fa6-1322">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1322">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-1323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1323">Az.Network</span></span>
* <span data-ttu-id="d4fa6-1324">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1324">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4fa6-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1325">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4fa6-1326">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1326">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="d4fa6-1327">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1327">SDK Update</span></span>
* <span data-ttu-id="d4fa6-1328">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1328">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="d4fa6-1329">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1329">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1330">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-1331">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1331">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="d4fa6-1332">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1332">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="d4fa6-1333">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1333">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="d4fa6-1334">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1334">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="d4fa6-1335">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1335">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="d4fa6-1336">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1336">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1337">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-1338">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1338">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="d4fa6-1339">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1339">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4fa6-1340">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1340">Az.Storage</span></span>
* <span data-ttu-id="d4fa6-1341">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1341">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="d4fa6-1342">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1342">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="d4fa6-1343">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1343">Az.AnalysisServices</span></span>
* <span data-ttu-id="d4fa6-1344">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1344">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4fa6-1345">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1345">Az.Automation</span></span>
* <span data-ttu-id="d4fa6-1346">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1346">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="d4fa6-1347">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1347">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="d4fa6-1348">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1348">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4fa6-1349">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1349">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4fa6-1350">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1350">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-1351">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1351">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-1352">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1352">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="d4fa6-1353">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1353">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="d4fa6-1354">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1354">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="d4fa6-1355">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1355">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4fa6-1356">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1356">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4fa6-1357">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1357">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d4fa6-1358">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1358">Az.EventHub</span></span>
* <span data-ttu-id="d4fa6-1359">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1359">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="d4fa6-1360">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1360">Az.KeyVault</span></span>
* <span data-ttu-id="d4fa6-1361">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1361">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d4fa6-1362">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1362">Az.LogicApp</span></span>
* <span data-ttu-id="d4fa6-1363">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1363">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="d4fa6-1364">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1364">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="d4fa6-1365">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1365">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="d4fa6-1366">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1366">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d4fa6-1367">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1367">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d4fa6-1368">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1368">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d4fa6-1369">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1369">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="d4fa6-1370">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1370">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="d4fa6-1371">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1371">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d4fa6-1372">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1372">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d4fa6-1373">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1373">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d4fa6-1374">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1374">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="d4fa6-1375">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1375">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d4fa6-1376">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1376">Az.Monitor</span></span>
* <span data-ttu-id="d4fa6-1377">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1377">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-1378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1378">Az.Network</span></span>
* <span data-ttu-id="d4fa6-1379">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1379">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d4fa6-1380">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1380">Az.OperationalInsights</span></span>
* <span data-ttu-id="d4fa6-1381">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1381">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="d4fa6-1382">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1382">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="d4fa6-1383">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1383">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="d4fa6-1384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1384">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-1385">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1385">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d4fa6-1386">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1386">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="d4fa6-1387">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1387">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="d4fa6-1388">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1388">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-1389">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1389">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-1390">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1390">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="d4fa6-1391">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1391">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4fa6-1392">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1392">Az.Websites</span></span>
* <span data-ttu-id="d4fa6-1393">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1393">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="d4fa6-1394">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1394">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4fa6-1395">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1395">Az.Accounts</span></span>
* <span data-ttu-id="d4fa6-1396">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1396">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d4fa6-1397">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1397">Az.AnalysisServices</span></span>
<span data-ttu-id="d4fa6-1398">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1398">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-1399">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1399">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-1400">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1400">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="d4fa6-1401">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1401">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="d4fa6-1402">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1402">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4fa6-1403">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1403">Az.RecoveryServices</span></span>
<span data-ttu-id="d4fa6-1404">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1404">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-1405">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1405">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-1406">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1406">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="d4fa6-1407">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1407">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d4fa6-1408">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1408">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="d4fa6-1409">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1409">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-1410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1410">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-1411">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1411">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="d4fa6-1412">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1412">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="d4fa6-1413">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1413">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="d4fa6-1414">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1414">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4fa6-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1415">Az.Accounts</span></span>
* <span data-ttu-id="d4fa6-1416">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1416">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d4fa6-1417">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1417">Az.AnalysisServices</span></span>
* <span data-ttu-id="d4fa6-1418">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1418">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d4fa6-1419">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1419">Az.RecoveryServices</span></span>
* <span data-ttu-id="d4fa6-1420">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1420">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="d4fa6-1421">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1421">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4fa6-1422">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1422">Az.Accounts</span></span>
* <span data-ttu-id="d4fa6-1423">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1423">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d4fa6-1424">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1424">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d4fa6-1425">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1425">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="d4fa6-1426">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1426">Az.Aks</span></span>
* <span data-ttu-id="d4fa6-1427">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1427">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d4fa6-1428">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1428">Az.Automation</span></span>
* <span data-ttu-id="d4fa6-1429">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1429">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="d4fa6-1430">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1430">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d4fa6-1431">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1431">Az.Cdn</span></span>
* <span data-ttu-id="d4fa6-1432">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1432">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1433">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-1434">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1434">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="d4fa6-1435">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1435">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="d4fa6-1436">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1436">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d4fa6-1437">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1437">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d4fa6-1438">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1438">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d4fa6-1439">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1439">Az.DataFactory</span></span>
* <span data-ttu-id="d4fa6-1440">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1440">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4fa6-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4fa6-1442">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1442">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="d4fa6-1443">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1443">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="d4fa6-1444">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1444">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4fa6-1445">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1445">Az.IotHub</span></span>
* <span data-ttu-id="d4fa6-1446">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1446">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d4fa6-1447">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1447">Az.KeyVault</span></span>
* <span data-ttu-id="d4fa6-1448">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1448">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1449">Az.Network</span></span>
* <span data-ttu-id="d4fa6-1450">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1450">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-1451">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1451">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-1452">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1452">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="d4fa6-1453">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1453">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="d4fa6-1454">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1454">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="d4fa6-1455">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1455">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="d4fa6-1456">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1456">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="d4fa6-1457">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1457">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="d4fa6-1458">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1458">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4fa6-1459">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1459">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4fa6-1460">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1460">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="d4fa6-1461">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1461">Fix some error messages.</span></span>
* <span data-ttu-id="d4fa6-1462">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1462">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="d4fa6-1463">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1463">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d4fa6-1464">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1464">Az.SignalR</span></span>
* <span data-ttu-id="d4fa6-1465">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1465">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-1466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1466">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-1467">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1467">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d4fa6-1468">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1468">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="d4fa6-1469">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1469">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="d4fa6-1470">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1470">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4fa6-1471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1471">Az.Storage</span></span>
* <span data-ttu-id="d4fa6-1472">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1472">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d4fa6-1473">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1473">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="d4fa6-1474">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1474">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="d4fa6-1475">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1475">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="d4fa6-1476">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1476">Az.TrafficManager</span></span>
* <span data-ttu-id="d4fa6-1477">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1477">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4fa6-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1478">Az.Websites</span></span>
* <span data-ttu-id="d4fa6-1479">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1479">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d4fa6-1480">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1480">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="d4fa6-1481">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1481">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="d4fa6-1482">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1482">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d4fa6-1483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1483">Az.Accounts</span></span>
* <span data-ttu-id="d4fa6-1484">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1484">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-1485">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1485">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-1486">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1486">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="d4fa6-1487">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1487">Updated the description of ID in help files</span></span>
* <span data-ttu-id="d4fa6-1488">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1488">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4fa6-1489">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1489">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4fa6-1490">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1490">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="d4fa6-1491">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1491">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d4fa6-1492">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1492">Az.EventGrid</span></span>
* <span data-ttu-id="d4fa6-1493">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1493">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="d4fa6-1494">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1494">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="d4fa6-1495">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1495">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d4fa6-1496">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1496">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d4fa6-1497">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1497">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d4fa6-1498">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1498">Dead letter endpoint.</span></span>
    - <span data-ttu-id="d4fa6-1499">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1499">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d4fa6-1500">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1500">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d4fa6-1501">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1501">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d4fa6-1502">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1502">Dead letter endpoint.</span></span>
* <span data-ttu-id="d4fa6-1503">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1503">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="d4fa6-1504">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1504">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d4fa6-1505">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1505">Az.IotHub</span></span>
* <span data-ttu-id="d4fa6-1506">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1506">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d4fa6-1507">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1507">Az.LogicApp</span></span>
* <span data-ttu-id="d4fa6-1508">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1508">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-1509">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1509">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-1510">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1510">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="d4fa6-1511">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1511">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="d4fa6-1512">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1512">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d4fa6-1513">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1513">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="d4fa6-1514">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1514">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="d4fa6-1515">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1515">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d4fa6-1516">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1516">Az.SignalR</span></span>
* <span data-ttu-id="d4fa6-1517">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1517">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-1518">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1518">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-1519">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1519">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d4fa6-1520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1520">Az.Storage</span></span>
* <span data-ttu-id="d4fa6-1521">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1521">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="d4fa6-1522">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1522">New-AzStorageContext</span></span>
* <span data-ttu-id="d4fa6-1523">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1523">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="d4fa6-1524">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1524">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4fa6-1525">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1525">Az.Websites</span></span>
* <span data-ttu-id="d4fa6-1526">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1526">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="d4fa6-1527">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1527">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="d4fa6-1528">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1528">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="d4fa6-1529">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1529">General</span></span>

- <span data-ttu-id="d4fa6-1530">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1530">General Availability of Az Module</span></span>
- <span data-ttu-id="d4fa6-1531">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1531">Online help for each module</span></span>
- <span data-ttu-id="d4fa6-1532">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1532">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="d4fa6-1533">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1533">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="d4fa6-1534">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1534">Az.Accounts</span></span>
- <span data-ttu-id="d4fa6-1535">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1535">Changed from Az.Profile</span></span>
- <span data-ttu-id="d4fa6-1536">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1536">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d4fa6-1537">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1537">Az.ApiManagement</span></span>
- <span data-ttu-id="d4fa6-1538">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1538">Fixes for #7002</span></span>
- <span data-ttu-id="d4fa6-1539">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="d4fa6-1540">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1540">Az.Batch</span></span>
- <span data-ttu-id="d4fa6-1541">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1541">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="d4fa6-1542">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1542">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="d4fa6-1543">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="d4fa6-1544">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1544">Az.Billing</span></span>
- <span data-ttu-id="d4fa6-1545">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1545">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="d4fa6-1546">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1546">Az.CognitivServices</span></span>
- <span data-ttu-id="d4fa6-1547">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1547">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="d4fa6-1548">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1548">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d4fa6-1549">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1549">Az.ContainerInstance</span></span>
- <span data-ttu-id="d4fa6-1550">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1550">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="d4fa6-1551">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1551">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="d4fa6-1552">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d4fa6-1553">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1553">Az.DataLakeStore</span></span>
- <span data-ttu-id="d4fa6-1554">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="d4fa6-1555">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1555">Az.Monitor</span></span>
- <span data-ttu-id="d4fa6-1556">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1556">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="d4fa6-1557">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1557">Az.KeyVault</span></span>
- <span data-ttu-id="d4fa6-1558">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1558">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="d4fa6-1559">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1559">Az.MachineLearning</span></span>
- <span data-ttu-id="d4fa6-1560">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1560">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="d4fa6-1561">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1561">Az.Media</span></span>
- <span data-ttu-id="d4fa6-1562">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1562">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d4fa6-1563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1563">Az.Network</span></span>
<span data-ttu-id="d4fa6-1564">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1564">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="d4fa6-1565">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1565">New cmdlets added:</span></span>
        - <span data-ttu-id="d4fa6-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d4fa6-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d4fa6-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d4fa6-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d4fa6-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d4fa6-1571">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1571">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="d4fa6-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="d4fa6-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="d4fa6-1574">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1574">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="d4fa6-1575">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1575">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="d4fa6-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d4fa6-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d4fa6-1578">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1578">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="d4fa6-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="d4fa6-1580">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1580">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="d4fa6-1581">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1581">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="d4fa6-1582">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1582">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d4fa6-1583">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1583">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d4fa6-1584">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1584">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="d4fa6-1585">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1585">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="d4fa6-1586">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1586">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="d4fa6-1587">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1587">Az.OperationalInsights</span></span>
- <span data-ttu-id="d4fa6-1588">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="d4fa6-1589">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1589">Az.Profile</span></span>
- <span data-ttu-id="d4fa6-1590">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1590">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d4fa6-1591">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1591">Az.RecoveryServices</span></span>
- <span data-ttu-id="d4fa6-1592">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="d4fa6-1593">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1593">Az.Resources</span></span>
- <span data-ttu-id="d4fa6-1594">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1594">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d4fa6-1595">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1595">Az.ServiceFabric</span></span>
- <span data-ttu-id="d4fa6-1596">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1596">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="d4fa6-1597">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1597">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="d4fa6-1598">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1598">Az.SIgnalR</span></span>
- <span data-ttu-id="d4fa6-1599">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1599">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="d4fa6-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1600">Az.Sql</span></span>
- <span data-ttu-id="d4fa6-1601">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1601">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="d4fa6-1602">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1602">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="d4fa6-1603">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="d4fa6-1604">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1604">Az.Storage</span></span>
- <span data-ttu-id="d4fa6-1605">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d4fa6-1606">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1606">Az.Websites</span></span>
- <span data-ttu-id="d4fa6-1607">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1607">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="d4fa6-1608">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1608">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="d4fa6-1609">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1609">General</span></span>

* <span data-ttu-id="d4fa6-1610">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1610">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="d4fa6-1611">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1611">Az.Compute</span></span>

* <span data-ttu-id="d4fa6-1612">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1612">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d4fa6-1613">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1613">Az.DataLakeStore</span></span>

* <span data-ttu-id="d4fa6-1614">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1614">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="d4fa6-1615">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1615">Az.FrontDoor</span></span>

* <span data-ttu-id="d4fa6-1616">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1616">Fixed some broken links</span></span>
    - <span data-ttu-id="d4fa6-1617">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1617">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="d4fa6-1618">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1618">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d4fa6-1619">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1619">Az.RecoveryServices</span></span>

* <span data-ttu-id="d4fa6-1620">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1620">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="d4fa6-1621">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1621">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="d4fa6-1622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1622">Az.Resources</span></span>

* <span data-ttu-id="d4fa6-1623">https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1623">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="d4fa6-1624">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1624">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="d4fa6-1625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1625">Az.Sql</span></span>

* <span data-ttu-id="d4fa6-1626">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1626">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="d4fa6-1627">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1627">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="d4fa6-1628">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1628">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="d4fa6-1629">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1629">Az.Storage</span></span>

* <span data-ttu-id="d4fa6-1630">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1630">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="d4fa6-1631">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1631">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="d4fa6-1632">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1632">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d4fa6-1633">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1633">Support Static Website configuration</span></span>
    - <span data-ttu-id="d4fa6-1634">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1634">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="d4fa6-1635">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1635">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d4fa6-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1636">Az.Websites</span></span>

* <span data-ttu-id="d4fa6-1637">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1637">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="d4fa6-1638">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1638">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="d4fa6-1639">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1639">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="d4fa6-1640">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1640">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d4fa6-1641">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1641">Az.ApiManagement</span></span>
* <span data-ttu-id="d4fa6-1642">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1642">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="d4fa6-1643">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1643">Az.Automation</span></span>
* <span data-ttu-id="d4fa6-1644">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1644">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="d4fa6-1645">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1645">Added Update Management cmdlets</span></span>
* <span data-ttu-id="d4fa6-1646">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1646">Added Source Control cmdlets</span></span>
* <span data-ttu-id="d4fa6-1647">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1647">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="d4fa6-1648">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1648">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="d4fa6-1649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1649">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-1650">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1650">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="d4fa6-1651">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1651">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d4fa6-1652">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1652">Az.ContainerInstance</span></span>
* <span data-ttu-id="d4fa6-1653">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1653">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="d4fa6-1654">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1654">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d4fa6-1655">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1655">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d4fa6-1656">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1656">Az.Network</span></span>
* <span data-ttu-id="d4fa6-1657">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1657">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="d4fa6-1658">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1658">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="d4fa6-1659">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1659">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="d4fa6-1660">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1660">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="d4fa6-1661">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1661">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d4fa6-1662">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1662">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="d4fa6-1663">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1663">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="d4fa6-1664">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1664">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="d4fa6-1665">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1665">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="d4fa6-1666">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1666">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="d4fa6-1667">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1667">Az.Relay</span></span>
* <span data-ttu-id="d4fa6-1668">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1668">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="d4fa6-1669">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1669">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-1670">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1670">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="d4fa6-1671">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1671">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="d4fa6-1672">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1672">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d4fa6-1673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1673">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4fa6-1674">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1674">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="d4fa6-1675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1675">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-1676">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1676">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="d4fa6-1677">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1677">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d4fa6-1678">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1678">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d4fa6-1679">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1679">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d4fa6-1680">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1680">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d4fa6-1681">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1681">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d4fa6-1682">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1682">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d4fa6-1683">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1683">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d4fa6-1684">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1684">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="d4fa6-1685">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1685">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="d4fa6-1686">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1686">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="d4fa6-1687">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1687">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="d4fa6-1688">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1688">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d4fa6-1689">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1689">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d4fa6-1690">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1690">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="d4fa6-1691">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1691">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="d4fa6-1692">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1692">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="d4fa6-1693">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1693">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d4fa6-1694">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1694">General</span></span>
* <span data-ttu-id="d4fa6-1695">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1695">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="d4fa6-1696">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1696">Az.Profile</span></span>
* <span data-ttu-id="d4fa6-1697">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1697">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="d4fa6-1698">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1698">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="d4fa6-1699">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1699">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="d4fa6-1700">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1700">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="d4fa6-1701">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1701">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="d4fa6-1702">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1702">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="d4fa6-1703">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1703">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="d4fa6-1704">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1704">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4fa6-1705">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1705">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-1706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1706">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-1707">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1707">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="d4fa6-1708">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1708">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="d4fa6-1709">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1709">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4fa6-1710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1710">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4fa6-1711">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1711">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="d4fa6-1712">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1712">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="d4fa6-1713">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1713">Az.Insights</span></span>
* <span data-ttu-id="d4fa6-1714">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1714">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="d4fa6-1715">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1715">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="d4fa6-1716">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1716">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="d4fa6-1717">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1717">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1718">Az.Network</span></span>
* <span data-ttu-id="d4fa6-1719">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1719">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="d4fa6-1720">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1720">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="d4fa6-1721">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1721">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="d4fa6-1722">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1722">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="d4fa6-1723">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1723">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d4fa6-1724">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1724">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d4fa6-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d4fa6-1726">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1726">Az.PolicyInsights</span></span>
* <span data-ttu-id="d4fa6-1727">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1727">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-1728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1728">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-1729">https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1729">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="d4fa6-1730">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1730">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d4fa6-1731">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1731">Az.ServiceBus</span></span>
* <span data-ttu-id="d4fa6-1732">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1732">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d4fa6-1733">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1733">Az.ServiceFabric</span></span>
* <span data-ttu-id="d4fa6-1734">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1734">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="d4fa6-1735">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1735">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="d4fa6-1736">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1736">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="d4fa6-1737">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1737">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="d4fa6-1738">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1738">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="d4fa6-1739">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1739">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="d4fa6-1740">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1740">Az.Profile</span></span>
* <span data-ttu-id="d4fa6-1741">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1741">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="d4fa6-1742">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1742">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-1743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1743">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-1744">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1744">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="d4fa6-1745">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1745">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d4fa6-1746">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1746">Az.DataLakeStore</span></span>
* <span data-ttu-id="d4fa6-1747">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1747">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="d4fa6-1748">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1748">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="d4fa6-1749">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1749">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d4fa6-1750">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1750">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d4fa6-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1752">Az.Network</span></span>
* <span data-ttu-id="d4fa6-1753">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1753">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="d4fa6-1754">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1755">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-1756">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1756">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="d4fa6-1757">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1757">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="d4fa6-1758">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1758">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="d4fa6-1759">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1759">Azure.Storage</span></span>
* <span data-ttu-id="d4fa6-1760">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1760">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="d4fa6-1761">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1761">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="d4fa6-1762">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1762">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d4fa6-1763">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1763">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="d4fa6-1764">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1764">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="d4fa6-1765">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1765">Az.CognitiveServices</span></span>
* <span data-ttu-id="d4fa6-1766">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1766">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d4fa6-1767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1767">Az.Compute</span></span>
* <span data-ttu-id="d4fa6-1768">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1768">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="d4fa6-1769">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1769">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="d4fa6-1770">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1770">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="d4fa6-1771">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1771">Az.DataFactoryV2</span></span>
* <span data-ttu-id="d4fa6-1772">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1772">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d4fa6-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1773">Az.Network</span></span>
* <span data-ttu-id="d4fa6-1774">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1774">Added NetworkProfile functionality.</span></span> <span data-ttu-id="d4fa6-1775">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1775">new cmdlets added</span></span>
    - <span data-ttu-id="d4fa6-1776">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1776">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="d4fa6-1777">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1777">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="d4fa6-1778">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1778">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="d4fa6-1779">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1779">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="d4fa6-1780">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1780">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="d4fa6-1781">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1781">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="d4fa6-1782">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1782">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="d4fa6-1783">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1783">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="d4fa6-1784">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1784">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d4fa6-1785">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1785">Az.RedisCache</span></span>
* <span data-ttu-id="d4fa6-1786">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1786">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="d4fa6-1787">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1787">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="d4fa6-1788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1788">Az.Resources</span></span>
* <span data-ttu-id="d4fa6-1789">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1789">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d4fa6-1790">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1790">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="d4fa6-1791">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1791">Az.Sql</span></span>
* <span data-ttu-id="d4fa6-1792">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1792">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d4fa6-1793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1793">Az.Websites</span></span>
* <span data-ttu-id="d4fa6-1794">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1794">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="d4fa6-1795">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1795">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="d4fa6-1796">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1796">0.2.0 - September 2018</span></span>
 <span data-ttu-id="d4fa6-1797">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="d4fa6-1797">Initial Release</span></span>
