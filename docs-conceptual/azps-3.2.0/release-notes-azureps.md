---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: f77d901169b0d98b2425a2e50d33a1789150b770
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182553"
---
## <a name="320---december-2019"></a><span data-ttu-id="763af-103">3.2.0 – 2019. december</span><span class="sxs-lookup"><span data-stu-id="763af-103">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="763af-104">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="763af-104">General</span></span>
* <span data-ttu-id="763af-105">A .psd1 hivatkozásai frissítve, hogy minden modulhoz a relatív elérési utat használják</span><span class="sxs-lookup"><span data-stu-id="763af-105">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="763af-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-106">Az.Accounts</span></span>
* <span data-ttu-id="763af-107">A megfelelő felhasználói ügynök beállítva az ügyféloldali telemetriához az Az 4.0 előzetes verziójában</span><span class="sxs-lookup"><span data-stu-id="763af-107">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="763af-108">Felhasználóbarát hibaüzenet megjelenítése, ha az Az 4.0 előzetes verziójában a környezet null értékű</span><span class="sxs-lookup"><span data-stu-id="763af-108">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="763af-109">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="763af-109">Az.Batch</span></span>
* <span data-ttu-id="763af-110">Ki lett javítva a [10602-es](https://github.com/Azure/azure-powershell/issues/10602) számú hiba, amely miatt a **New-AzBatchPool** nem megfelelően küldte el a „VirtualMachineConfiguration.ContainerConfiguration” és a „VirtualMachineConfiguration.DataDisks” paramétereket a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="763af-110">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="763af-111">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="763af-111">Az.DataFactory</span></span>
* <span data-ttu-id="763af-112">Az ADF .Net SDK a 4.5.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="763af-112">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="763af-113">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="763af-113">Az.FrontDoor</span></span>
* <span data-ttu-id="763af-114">A WAF felügyeleti szabályok kizárása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="763af-114">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="763af-115">Hozzá lett adva a SocketAddr automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="763af-115">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="763af-116">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="763af-116">Az.HealthcareApis</span></span>
* <span data-ttu-id="763af-117">Kivételkezelés</span><span class="sxs-lookup"><span data-stu-id="763af-117">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="763af-118">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="763af-118">Az.KeyVault</span></span>
* <span data-ttu-id="763af-119">Ki lett javítva az esetleg nem beállított értékek hozzáférésével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="763af-119">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="763af-120">Az elliptikus görbéjű titkosítási tanúsítványok kezelése</span><span class="sxs-lookup"><span data-stu-id="763af-120">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="763af-121">A görbe tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="763af-121">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="763af-122">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="763af-122">Az.Monitor</span></span>
* <span data-ttu-id="763af-123">Opcionális argumentum hozzáadva a Diagnosztikai beállítások hozzáadása parancshoz.</span><span class="sxs-lookup"><span data-stu-id="763af-123">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="763af-124">Ez egy kapcsoló argumentum, amely megléte esetén azt jelzi, hogy a Log Analyticsbe történő exportálást egy rögzített séma (más néven</span><span class="sxs-lookup"><span data-stu-id="763af-124">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="763af-125">dedikált adattípus) szerint kell végrehajtani</span><span class="sxs-lookup"><span data-stu-id="763af-125">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-126">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-126">Az.Network</span></span>
* <span data-ttu-id="763af-127">Támogatás az Ip-csoportok számára az AzureFirewall alkalmazás, valamint a Nat- és a hálózati szabályok esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-127">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-128">Az.Resources</span></span>
* <span data-ttu-id="763af-129">Ki lett javítva az a hiba, amely miatt a sablonalapú üzembe helyezés során a sablonparamétert nem lehet olvasni, ha a sablonparaméter és egy beépített paraméter neve között névütközés áll fenn.</span><span class="sxs-lookup"><span data-stu-id="763af-129">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="763af-130">Frissültek a szabályzat parancsmagjai a 2019. 09. 01. dátumú új API-verzió használatára, amely bevezeti a szabályzatkészlet-definíciókon belüli csoportos támogatást.</span><span class="sxs-lookup"><span data-stu-id="763af-130">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-131">Az.Sql</span></span>
* <span data-ttu-id="763af-132">Frissítve lett a sebezhetőségi felmérés automatikus engedélyezéséhez szükséges tárterület létrehozása a Storagev2-ben</span><span class="sxs-lookup"><span data-stu-id="763af-132">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="763af-133">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-133">Az.Storage</span></span>
* <span data-ttu-id="763af-134">A blob-/tárolóidentitás-alapú SAS-token Oauth-hitelesítésen alapuló Storage-környezettel való létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="763af-134">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="763af-135">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="763af-135">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="763af-136">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="763af-136">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="763af-137">Támogatott lett a tárfiókhoz tartozó felhasználódelegálási kulcsok visszavonása, így minden identitásalapú SAS-token visszavonható</span><span class="sxs-lookup"><span data-stu-id="763af-137">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="763af-138">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="763af-138">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="763af-139">Frissítés a Microsoft.Azure.Management.Storage 14.2.0-s verziójára az új API-verzió (2019. 06. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="763af-139">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="763af-140">A QuotaGiB megosztása több mint 5120 fájlmegosztási parancsmagot támogat a felügyeleti síkon, és a „Kvóta” paraméteraliast hozzáadva a „QuotaGiB” paraméterhez</span><span class="sxs-lookup"><span data-stu-id="763af-140">Support Share QuotaGiB more than 5120 in Management plane File Share cmdlets, and add parameter alias 'Quota' to parameter 'QuotaGiB'</span></span> 
    - <span data-ttu-id="763af-141">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="763af-141">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="763af-142">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="763af-142">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="763af-143">A „QuotaGiB” paraméteralias hozzáadva a „kvóta” paraméterhez</span><span class="sxs-lookup"><span data-stu-id="763af-143">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="763af-144">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="763af-144">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="763af-145">Ki lett javítva az a hiba, amely miatt a Set-AzStorageContainerAcl parancsmag el tudta távolítani a tárolt hozzáférési szabályzatot</span><span class="sxs-lookup"><span data-stu-id="763af-145">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="763af-146">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="763af-146">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="763af-147">3.1.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="763af-147">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="763af-148">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="763af-148">Highlights since the last major release</span></span>
* <span data-ttu-id="763af-149">Az.DataBoxEdge 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="763af-149">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="763af-150">Az.SqlVirtualMachine 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="763af-150">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-151">Az.Compute</span></span>
* <span data-ttu-id="763af-152">A virtuális gépek Reapply funkciója</span><span class="sxs-lookup"><span data-stu-id="763af-152">VM Reapply feature</span></span>
    - <span data-ttu-id="763af-153">A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="763af-153">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="763af-154">A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:</span><span class="sxs-lookup"><span data-stu-id="763af-154">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="763af-155">Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="763af-155">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="763af-156">Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="763af-156">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="763af-157">A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez</span><span class="sxs-lookup"><span data-stu-id="763af-157">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="763af-158">A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-158">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="763af-159">A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező</span><span class="sxs-lookup"><span data-stu-id="763af-159">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="763af-160">A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="763af-160">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="763af-161">A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban</span><span class="sxs-lookup"><span data-stu-id="763af-161">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="763af-162">A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-162">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="763af-163">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="763af-163">Az.DataBoxEdge</span></span>
* <span data-ttu-id="763af-164">A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="763af-164">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="763af-165">Megrendelés lekérése</span><span class="sxs-lookup"><span data-stu-id="763af-165">Get the Order</span></span>
* <span data-ttu-id="763af-166">A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="763af-166">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="763af-167">Új megrendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="763af-167">Create new Order</span></span>
* <span data-ttu-id="763af-168">A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="763af-168">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="763af-169">Megrendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="763af-169">Remove the Order</span></span>
* <span data-ttu-id="763af-170">`New-AzDataBoxEdgeShare` parancsmag módosítása</span><span class="sxs-lookup"><span data-stu-id="763af-170">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="763af-171">Mostantól helyi megosztást hoz létre</span><span class="sxs-lookup"><span data-stu-id="763af-171">Now creates Local Share</span></span>
* <span data-ttu-id="763af-172">A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="763af-172">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="763af-173">Mostantól az IotRole leképezhető a Share-re</span><span class="sxs-lookup"><span data-stu-id="763af-173">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="763af-174">A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="763af-174">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="763af-175">Frissítések keresésének, letöltésének, telepítésének indítása az eszközön</span><span class="sxs-lookup"><span data-stu-id="763af-175">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="763af-176">A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="763af-176">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="763af-177">Triggerek információinak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="763af-177">Gets the information about Triggers</span></span>
* <span data-ttu-id="763af-178">A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="763af-178">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="763af-179">Új triggerek létrehozása</span><span class="sxs-lookup"><span data-stu-id="763af-179">Create new Triggers</span></span>
* <span data-ttu-id="763af-180">A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="763af-180">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="763af-181">Triggerek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="763af-181">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="763af-182">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="763af-182">Az.DataFactory</span></span>
* <span data-ttu-id="763af-183">Az ADF .Net SDK a 4.4.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="763af-183">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="763af-184">Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="763af-184">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="763af-185">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="763af-185">Az.DataLakeStore</span></span>
* <span data-ttu-id="763af-186">Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja</span><span class="sxs-lookup"><span data-stu-id="763af-186">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="763af-187">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="763af-187">Az.EventHub</span></span>
* <span data-ttu-id="763af-188">A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása</span><span class="sxs-lookup"><span data-stu-id="763af-188">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="763af-189">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="763af-189">Az.FrontDoor</span></span>
* <span data-ttu-id="763af-190">Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="763af-190">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="763af-191">A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="763af-191">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="763af-192">Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához</span><span class="sxs-lookup"><span data-stu-id="763af-192">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="763af-193">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="763af-193">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-194">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-194">Az.Network</span></span>
* <span data-ttu-id="763af-195">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.</span><span class="sxs-lookup"><span data-stu-id="763af-195">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="763af-196">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="763af-196">Az.PrivateDns</span></span>
* <span data-ttu-id="763af-197">A PrivateDns .net sdk frissült az 1.0.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="763af-197">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="763af-198">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="763af-198">Az.RecoveryServices</span></span>
* <span data-ttu-id="763af-199">Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="763af-199">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="763af-200">Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.</span><span class="sxs-lookup"><span data-stu-id="763af-200">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="763af-201">SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="763af-201">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="763af-202">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="763af-202">Az.RedisCache</span></span>
* <span data-ttu-id="763af-203">A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="763af-203">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="763af-204">Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="763af-204">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="763af-205">Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="763af-205">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-206">Az.Resources</span></span>
- <span data-ttu-id="763af-207">Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.</span><span class="sxs-lookup"><span data-stu-id="763af-207">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="763af-208">Frissült a létrehozási szabályzat definíciójának súgóbeli példája</span><span class="sxs-lookup"><span data-stu-id="763af-208">Updated create policy definition help example</span></span>
- <span data-ttu-id="763af-209">Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.</span><span class="sxs-lookup"><span data-stu-id="763af-209">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="763af-210">Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.</span><span class="sxs-lookup"><span data-stu-id="763af-210">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="763af-211">A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="763af-211">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-212">Az.Sql</span></span>
* <span data-ttu-id="763af-213">Az adatbázisbeli ReadReplicaCount mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="763af-213">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="763af-214">A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén</span><span class="sxs-lookup"><span data-stu-id="763af-214">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="763af-215">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="763af-215">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="763af-216">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="763af-216">General</span></span>
* <span data-ttu-id="763af-217">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="763af-217">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="763af-218">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-218">Az.Accounts</span></span>
* <span data-ttu-id="763af-219">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="763af-219">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="763af-220">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="763af-220">Az.Advisor</span></span>
* <span data-ttu-id="763af-221">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="763af-221">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="763af-222">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="763af-222">Az.Batch</span></span>
* <span data-ttu-id="763af-223">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="763af-223">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="763af-224">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="763af-224">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="763af-225">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="763af-225">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="763af-226">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="763af-226">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="763af-227">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="763af-227">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="763af-228">Ezek az **New-AzBatchTask** `-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="763af-228">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="763af-229">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="763af-229">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="763af-230">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="763af-230">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="763af-231">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="763af-231">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="763af-232">A `PSApplication` **Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="763af-232">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="763af-233">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="763af-233">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="763af-234">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="763af-234">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="763af-235">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-235">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="763af-236">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="763af-236">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="763af-237">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="763af-237">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="763af-238">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-238">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="763af-239">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-239">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="763af-240">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="763af-240">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="763af-241">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="763af-241">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="763af-242">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="763af-242">This operation is no longer supported.</span></span>
* <span data-ttu-id="763af-243">`PSCloudServiceConfiguration` `TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="763af-243">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="763af-244">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-244">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="763af-245">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="763af-245">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="763af-246">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="763af-246">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="763af-247">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="763af-247">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="763af-248">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="763af-248">New non-verified images are also now returned.</span></span> <span data-ttu-id="763af-249">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="763af-249">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="763af-250">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="763af-250">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="763af-251">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="763af-251">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="763af-252">Ez a `PSNetworkSecurityGroupRule` `SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="763af-252">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="763af-253">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="763af-253">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="763af-254">Ezt a `PSTaskContainerSettings` `WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="763af-254">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="763af-255">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="763af-255">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="763af-256">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="763af-256">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="763af-257">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="763af-257">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="763af-258">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="763af-258">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="763af-259">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="763af-259">Az.Cdn</span></span>
* <span data-ttu-id="763af-260">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="763af-260">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="763af-261">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="763af-261">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-262">Az.Compute</span></span>
* <span data-ttu-id="763af-263">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="763af-263">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="763af-264">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="763af-264">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="763af-265">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="763af-265">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="763af-266">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="763af-266">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="763af-267">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="763af-267">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="763af-268">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-268">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="763af-269">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="763af-269">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="763af-270">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="763af-270">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="763af-271">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="763af-271">Breaking changes</span></span>
    - <span data-ttu-id="763af-272">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="763af-272">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="763af-273">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="763af-273">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="763af-274">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="763af-274">Az.DataFactory</span></span>
* <span data-ttu-id="763af-275">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="763af-275">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="763af-276">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="763af-276">Az.DataLakeStore</span></span>
* <span data-ttu-id="763af-277">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="763af-277">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="763af-278">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="763af-278">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="763af-279">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="763af-279">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="763af-280">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="763af-280">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="763af-281">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="763af-281">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="763af-282">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="763af-282">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="763af-283">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="763af-283">Az.FrontDoor</span></span>
* <span data-ttu-id="763af-284">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="763af-284">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="763af-285">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="763af-285">Az.HDInsight</span></span>
* <span data-ttu-id="763af-286">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-286">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="763af-287">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="763af-287">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="763af-288">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="763af-288">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="763af-289">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="763af-289">Removed five cmdlets:</span></span>
    - <span data-ttu-id="763af-290">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="763af-290">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="763af-291">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="763af-291">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="763af-292">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="763af-292">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="763af-293">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="763af-293">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="763af-294">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="763af-294">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="763af-295">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="763af-295">Added three cmdlets:</span></span>
    - <span data-ttu-id="763af-296">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="763af-296">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="763af-297">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="763af-297">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="763af-298">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="763af-298">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="763af-299">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="763af-299">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="763af-300">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="763af-300">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="763af-301">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="763af-301">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="763af-302">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="763af-302">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="763af-303">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="763af-303">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="763af-304">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="763af-304">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="763af-305">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="763af-305">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="763af-306">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="763af-306">Added some scenario test cases.</span></span>
* <span data-ttu-id="763af-307">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="763af-307">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="763af-308">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="763af-308">Az.IotHub</span></span>
* <span data-ttu-id="763af-309">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="763af-309">Breaking changes:</span></span>
    - <span data-ttu-id="763af-310">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="763af-310">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="763af-311">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="763af-311">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="763af-312">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="763af-312">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="763af-313">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="763af-313">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="763af-314">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="763af-314">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="763af-315">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="763af-315">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="763af-316">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="763af-316">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="763af-317">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="763af-317">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="763af-318">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="763af-318">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="763af-319">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="763af-319">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="763af-320">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="763af-320">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="763af-321">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="763af-321">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="763af-322">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="763af-322">Az.RecoveryServices</span></span>
* <span data-ttu-id="763af-323">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="763af-323">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="763af-324">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="763af-324">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="763af-325">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="763af-325">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="763af-326">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="763af-326">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="763af-327">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="763af-327">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="763af-328">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="763af-328">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="763af-329">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="763af-329">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="763af-330">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="763af-330">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="763af-331">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="763af-331">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-332">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-332">Az.Resources</span></span>
* <span data-ttu-id="763af-333">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="763af-333">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-334">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-334">Az.Network</span></span>
* <span data-ttu-id="763af-335">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="763af-335">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="763af-336">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="763af-336">Updated cmdlet:</span></span>
        - <span data-ttu-id="763af-337">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="763af-337">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="763af-338">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="763af-338">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="763af-339">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="763af-339">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="763af-340">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="763af-340">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="763af-341">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="763af-341">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="763af-342">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="763af-342">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="763af-343">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="763af-343">New cmdlet:</span></span>
        - <span data-ttu-id="763af-344">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="763af-344">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="763af-345">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="763af-345">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="763af-346">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="763af-346">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="763af-347">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="763af-347">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="763af-348">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="763af-348">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="763af-349">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="763af-349">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="763af-350">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="763af-350">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="763af-351">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-351">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="763af-352">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="763af-352">New cmdlets added:</span></span>
        - <span data-ttu-id="763af-353">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="763af-353">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="763af-354">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="763af-354">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="763af-355">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="763af-355">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="763af-356">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="763af-356">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="763af-357">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="763af-357">Set-AzVirtualHub</span></span>
* <span data-ttu-id="763af-358">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="763af-358">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="763af-359">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="763af-359">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="763af-360">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-360">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="763af-361">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-361">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="763af-362">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-362">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="763af-363">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-363">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="763af-364">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="763af-364">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="763af-365">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="763af-365">New cmdlets added:</span></span>
        - <span data-ttu-id="763af-366">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="763af-366">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="763af-367">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="763af-367">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="763af-368">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-368">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="763af-369">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-369">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="763af-370">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-370">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="763af-371">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-371">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="763af-372">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-372">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="763af-373">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-373">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="763af-374">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="763af-374">New cmdlets added:</span></span>
        - <span data-ttu-id="763af-375">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="763af-375">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="763af-376">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="763af-376">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="763af-377">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="763af-377">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="763af-378">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="763af-378">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="763af-379">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="763af-379">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="763af-380">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="763af-380">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="763af-381">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="763af-381">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="763af-382">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-382">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="763af-383">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-383">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="763af-384">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="763af-384">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="763af-385">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-385">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="763af-386">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="763af-386">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="763af-387">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-387">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="763af-388">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-388">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="763af-389">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="763af-389">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="763af-390">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="763af-390">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="763af-391">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-391">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="763af-392">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="763af-392">New cmdlets added:</span></span>
        - <span data-ttu-id="763af-393">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="763af-393">New-AzIpGroup</span></span>
        - <span data-ttu-id="763af-394">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="763af-394">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="763af-395">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="763af-395">Get-AzIpGroup</span></span>
        - <span data-ttu-id="763af-396">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="763af-396">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="763af-397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="763af-397">Az.ServiceFabric</span></span>
* <span data-ttu-id="763af-398">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="763af-398">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-399">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-399">Az.Sql</span></span>
* <span data-ttu-id="763af-400">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="763af-400">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="763af-401">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="763af-401">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="763af-402">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="763af-402">Removed deprecated aliases:</span></span>
* <span data-ttu-id="763af-403">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="763af-403">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="763af-404">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="763af-404">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="763af-405">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="763af-405">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="763af-406">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="763af-406">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="763af-407">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="763af-407">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="763af-408">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="763af-408">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="763af-409">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-409">Az.Storage</span></span>
* <span data-ttu-id="763af-410">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="763af-410">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="763af-411">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="763af-411">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="763af-412">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="763af-412">Set-AzStorageAccount</span></span>
* <span data-ttu-id="763af-413">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="763af-413">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="763af-414">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="763af-414">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="763af-415">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="763af-415">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="763af-416">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="763af-416">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="763af-417">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="763af-417">General</span></span>
* <span data-ttu-id="763af-418">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="763af-418">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="763af-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-419">Az.Accounts</span></span>
* <span data-ttu-id="763af-420">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="763af-420">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="763af-421">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="763af-421">Az.ApiManagement</span></span>
* <span data-ttu-id="763af-422">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="763af-422">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="763af-423">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="763af-423">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="763af-424">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="763af-424">Az.Automation</span></span>
* <span data-ttu-id="763af-425">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="763af-425">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="763af-426">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="763af-426">Az.Batch</span></span>
* <span data-ttu-id="763af-427">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="763af-427">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-428">Az.Compute</span></span>
* <span data-ttu-id="763af-429">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="763af-429">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="763af-430">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="763af-430">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="763af-431">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="763af-431">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="763af-432">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="763af-432">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="763af-433">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="763af-433">Az.DataFactory</span></span>
* <span data-ttu-id="763af-434">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="763af-434">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="763af-435">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="763af-435">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="763af-436">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="763af-436">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="763af-437">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="763af-437">Az.DataLakeStore</span></span>
* <span data-ttu-id="763af-438">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="763af-438">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="763af-439">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="763af-439">Az.HealthcareApis</span></span>
* <span data-ttu-id="763af-440">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="763af-440">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="763af-441">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="763af-441">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="763af-442">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="763af-442">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="763af-443">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="763af-443">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="763af-444">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="763af-444">Az.IotHub</span></span>
* <span data-ttu-id="763af-445">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="763af-445">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="763af-446">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="763af-446">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="763af-447">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="763af-447">Az.Monitor</span></span>
* <span data-ttu-id="763af-448">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="763af-448">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="763af-449">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="763af-449">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="763af-450">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="763af-450">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="763af-451">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="763af-451">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-452">Az.Network</span></span>
* <span data-ttu-id="763af-453">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="763af-453">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="763af-454">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="763af-454">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="763af-455">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="763af-455">New cmdlets added:</span></span>
        - <span data-ttu-id="763af-456">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="763af-456">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="763af-457">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="763af-457">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="763af-458">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="763af-458">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="763af-459">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="763af-459">Updated cmdlets:</span></span>
        - <span data-ttu-id="763af-460">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="763af-460">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="763af-461">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="763af-461">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="763af-462">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="763af-462">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="763af-463">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="763af-463">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="763af-464">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="763af-464">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="763af-465">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="763af-465">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="763af-466">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="763af-466">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="763af-467">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="763af-467">Az.RedisCache</span></span>
* <span data-ttu-id="763af-468">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="763af-468">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-469">Az.Sql</span></span>
* <span data-ttu-id="763af-470">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="763af-470">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="763af-471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-471">Az.Storage</span></span>
* <span data-ttu-id="763af-472">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="763af-472">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="763af-473">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="763af-473">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="763af-474">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="763af-474">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="763af-475">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="763af-475">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="763af-476">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="763af-476">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="763af-477">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="763af-477">Az.StorageSync</span></span>
* <span data-ttu-id="763af-478">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="763af-478">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="763af-479">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="763af-479">Az.Websites</span></span>
* <span data-ttu-id="763af-480">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="763af-480">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="763af-481">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="763af-481">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="763af-482">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="763af-482">Az.ApiManagement</span></span>
* <span data-ttu-id="763af-483">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="763af-483">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="763af-484">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="763af-484">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="763af-485">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="763af-485">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="763af-486">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="763af-486">Az.Automation</span></span>
* <span data-ttu-id="763af-487">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="763af-487">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="763af-488">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-488">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="763af-489">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="763af-489">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-490">Az.Compute</span></span>
* <span data-ttu-id="763af-491">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-491">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="763af-492">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-492">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="763af-493">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="763af-493">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="763af-494">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="763af-494">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="763af-495">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="763af-495">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="763af-496">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="763af-496">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="763af-497">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="763af-497">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="763af-498">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-498">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="763af-499">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-499">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="763af-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="763af-500">Az.DataFactory</span></span>
* <span data-ttu-id="763af-501">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="763af-501">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="763af-502">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="763af-502">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="763af-503">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="763af-503">Az.HDInsight</span></span>
* <span data-ttu-id="763af-504">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="763af-504">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="763af-505">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="763af-505">Az.IotHub</span></span>
* <span data-ttu-id="763af-506">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="763af-506">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="763af-507">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="763af-507">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="763af-508">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="763af-508">New cmdlets are:</span></span>
    - <span data-ttu-id="763af-509">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="763af-509">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="763af-510">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="763af-510">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="763af-511">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="763af-511">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="763af-512">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="763af-512">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="763af-513">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="763af-513">Az.Monitor</span></span>
* <span data-ttu-id="763af-514">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="763af-514">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="763af-515">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="763af-515">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="763af-516">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="763af-516">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="763af-517">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="763af-517">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="763af-518">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="763af-518">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="763af-519">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="763af-519">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="763af-520">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="763af-520">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="763af-521">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="763af-521">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="763af-522">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="763af-522">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="763af-523">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="763af-523">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="763af-524">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="763af-524">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="763af-525">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="763af-525">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="763af-526">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="763af-526">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="763af-527">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="763af-527">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="763af-528">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="763af-528">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="763af-529">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="763af-529">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="763af-530">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="763af-530">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="763af-531">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="763af-531">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="763af-532">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="763af-532">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="763af-533">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="763af-533">Overall improved help files</span></span>
* <span data-ttu-id="763af-534">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="763af-534">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-535">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-535">Az.Network</span></span>
* <span data-ttu-id="763af-536">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="763af-536">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="763af-537">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="763af-537">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="763af-538">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="763af-538">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="763af-539">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="763af-539">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="763af-540">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="763af-540">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="763af-541">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="763af-541">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="763af-542">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="763af-542">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="763af-543">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="763af-543">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="763af-544">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="763af-544">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="763af-545">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="763af-545">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="763af-546">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="763af-546">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="763af-547">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="763af-547">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="763af-548">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="763af-548">New cmdlets</span></span>
        - <span data-ttu-id="763af-549">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="763af-549">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="763af-550">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="763af-550">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="763af-551">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="763af-551">Updated cmdlet:</span></span>
        - <span data-ttu-id="763af-552">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="763af-552">New-VpnSite</span></span>
        - <span data-ttu-id="763af-553">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="763af-553">Update-VpnSite</span></span>
        - <span data-ttu-id="763af-554">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="763af-554">New-VpnConnection</span></span>
        - <span data-ttu-id="763af-555">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="763af-555">Update-VpnConnection</span></span>
* <span data-ttu-id="763af-556">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="763af-556">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="763af-557">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="763af-557">Az.RecoveryServices</span></span>
* <span data-ttu-id="763af-558">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="763af-558">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="763af-559">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="763af-559">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-560">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-560">Az.Resources</span></span>
* <span data-ttu-id="763af-561">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="763af-561">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="763af-562">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="763af-562">Az.ServiceFabric</span></span>
* <span data-ttu-id="763af-563">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="763af-563">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="763af-564">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="763af-564">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="763af-565">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="763af-565">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="763af-566">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="763af-566">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="763af-567">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="763af-567">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="763af-568">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="763af-568">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="763af-569">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="763af-569">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="763af-570">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="763af-570">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="763af-571">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="763af-571">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="763af-572">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="763af-572">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="763af-573">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="763af-573">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="763af-574">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="763af-574">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="763af-575">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="763af-575">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="763af-576">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="763af-576">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="763af-577">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="763af-577">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="763af-578">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="763af-578">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="763af-579">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="763af-579">Az.SignalR</span></span>
* <span data-ttu-id="763af-580">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="763af-580">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-581">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-581">Az.Sql</span></span>
* <span data-ttu-id="763af-582">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="763af-582">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="763af-583">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="763af-583">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="763af-584">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="763af-584">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="763af-585">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="763af-585">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="763af-586">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="763af-586">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="763af-587">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-587">Az.Storage</span></span>
* <span data-ttu-id="763af-588">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="763af-588">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="763af-589">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="763af-589">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="763af-590">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="763af-590">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="763af-591">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="763af-591">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="763af-592">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-592">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="763af-593">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="763af-593">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="763af-594">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="763af-594">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="763af-595">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="763af-595">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="763af-596">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="763af-596">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="763af-597">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="763af-597">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="763af-598">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="763af-598">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="763af-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="763af-599">Az.Websites</span></span>
* <span data-ttu-id="763af-600">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="763af-600">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="763af-601">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="763af-601">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="763af-602">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="763af-602">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="763af-603">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="763af-603">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="763af-604">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="763af-604">General</span></span>
* <span data-ttu-id="763af-605">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="763af-605">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="763af-606">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-606">Az.Accounts</span></span>
* <span data-ttu-id="763af-607">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="763af-607">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="763af-608">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="763af-608">Az.Aks</span></span>
* <span data-ttu-id="763af-609">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="763af-609">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="763af-610">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="763af-610">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="763af-611">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="763af-611">Az.ApiManagement</span></span>
* <span data-ttu-id="763af-612">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="763af-612">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="763af-613">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="763af-613">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="763af-614">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="763af-614">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="763af-615">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="763af-615">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="763af-616">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="763af-616">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="763af-617">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="763af-617">Az.Batch</span></span>
* <span data-ttu-id="763af-618">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="763af-618">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="763af-619">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="763af-619">Az.Cdn</span></span>
* <span data-ttu-id="763af-620">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="763af-620">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-621">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-621">Az.Compute</span></span>
* <span data-ttu-id="763af-622">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-622">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="763af-623">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-623">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="763af-624">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="763af-624">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="763af-625">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="763af-625">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="763af-626">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="763af-626">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="763af-627">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-627">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="763af-628">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="763af-628">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="763af-629">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="763af-629">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="763af-630">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="763af-630">Az.DataFactory</span></span>
* <span data-ttu-id="763af-631">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="763af-631">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="763af-632">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="763af-632">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="763af-633">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="763af-633">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="763af-634">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="763af-634">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="763af-635">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="763af-635">Az.DataLakeStore</span></span>
* <span data-ttu-id="763af-636">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="763af-636">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="763af-637">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="763af-637">Az.EventHub</span></span>
* <span data-ttu-id="763af-638">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="763af-638">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="763af-639">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="763af-639">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="763af-640">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-640">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="763af-641">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="763af-641">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="763af-642">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="763af-642">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="763af-643">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="763af-643">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="763af-644">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="763af-644">Az.Monitor</span></span>
* <span data-ttu-id="763af-645">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="763af-645">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-646">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-646">Az.Network</span></span>
* <span data-ttu-id="763af-647">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="763af-647">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="763af-648">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="763af-648">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="763af-649">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="763af-649">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="763af-650">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="763af-650">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="763af-651">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="763af-651">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="763af-652">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="763af-652">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="763af-653">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="763af-653">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="763af-654">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="763af-654">Az.OperationalInsights</span></span>
* <span data-ttu-id="763af-655">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="763af-655">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="763af-656">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-656">Added example</span></span>
    - <span data-ttu-id="763af-657">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="763af-657">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="763af-658">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-658">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="763af-659">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="763af-659">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="763af-660">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="763af-660">Az.RecoveryServices</span></span>
* <span data-ttu-id="763af-661">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="763af-661">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-662">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-662">Az.Resources</span></span>
* <span data-ttu-id="763af-663">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="763af-663">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="763af-664">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="763af-664">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="763af-665">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="763af-665">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="763af-666">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="763af-666">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="763af-667">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="763af-667">Az.ServiceBus</span></span>
* <span data-ttu-id="763af-668">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="763af-668">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="763af-669">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="763af-669">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="763af-670">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="763af-670">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="763af-671">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="763af-671">Az.ServiceFabric</span></span>
* <span data-ttu-id="763af-672">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="763af-672">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="763af-673">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="763af-673">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="763af-674">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="763af-674">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="763af-675">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="763af-675">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="763af-676">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="763af-676">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="763af-677">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="763af-677">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-678">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-678">Az.Sql</span></span>
* <span data-ttu-id="763af-679">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="763af-679">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="763af-680">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-680">Az.Storage</span></span>
* <span data-ttu-id="763af-681">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="763af-681">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="763af-682">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="763af-682">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="763af-683">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="763af-683">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="763af-684">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="763af-684">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="763af-685">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="763af-685">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="763af-686">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="763af-686">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="763af-687">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="763af-687">Az.Websites</span></span>
* <span data-ttu-id="763af-688">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="763af-688">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="763af-689">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="763af-689">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="763af-690">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-690">Az.Accounts</span></span>
* <span data-ttu-id="763af-691">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="763af-691">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="763af-692">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="763af-692">Az.ApplicationInsights</span></span>
* <span data-ttu-id="763af-693">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="763af-693">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="763af-694">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="763af-694">Az.Automation</span></span>
* <span data-ttu-id="763af-695">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="763af-695">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="763af-696">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="763af-696">Az.CognitiveServices</span></span>
* <span data-ttu-id="763af-697">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="763af-697">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-698">Az.Compute</span></span>
* <span data-ttu-id="763af-699">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="763af-699">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="763af-700">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="763af-700">Az.ContainerRegistry</span></span>
* <span data-ttu-id="763af-701">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="763af-701">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="763af-702">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="763af-702">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="763af-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="763af-703">Az.DataFactory</span></span>
* <span data-ttu-id="763af-704">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="763af-704">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="763af-705">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="763af-705">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="763af-706">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="763af-706">Az.EventHub</span></span>
* <span data-ttu-id="763af-707">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="763af-707">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="763af-708">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="763af-708">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="763af-709">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="763af-709">Az.KeyVault</span></span>
* <span data-ttu-id="763af-710">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="763af-710">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="763af-711">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="763af-711">Az.LogicApp</span></span>
* <span data-ttu-id="763af-712">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="763af-712">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="763af-713">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="763af-713">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="763af-714">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="763af-714">Az.ManagedServices</span></span>
* <span data-ttu-id="763af-715">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-715">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-716">Az.Network</span></span>
* <span data-ttu-id="763af-717">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-717">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="763af-718">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="763af-718">New cmdlets</span></span>
        - <span data-ttu-id="763af-719">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="763af-719">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="763af-720">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="763af-720">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="763af-721">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="763af-721">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="763af-722">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="763af-722">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="763af-723">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="763af-723">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="763af-724">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="763af-724">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="763af-725">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="763af-725">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="763af-726">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="763af-726">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="763af-727">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="763af-727">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="763af-728">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="763af-728">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="763af-729">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-729">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="763af-730">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-730">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="763af-731">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="763af-731">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="763af-732">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="763af-732">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="763af-733">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="763af-733">Updated cmdlets</span></span>
        - <span data-ttu-id="763af-734">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="763af-734">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="763af-735">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="763af-735">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="763af-736">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="763af-736">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="763af-737">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="763af-737">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="763af-738">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="763af-738">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="763af-739">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="763af-739">Updated cmdlet:</span></span>
        - <span data-ttu-id="763af-740">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="763af-740">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="763af-741">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="763af-741">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="763af-742">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="763af-742">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="763af-743">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="763af-743">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="763af-744">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="763af-744">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="763af-745">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="763af-745">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="763af-746">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="763af-746">Az.OperationalInsights</span></span>
* <span data-ttu-id="763af-747">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="763af-747">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="763af-748">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="763af-748">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="763af-749">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="763af-749">Az.RecoveryServices</span></span>
* <span data-ttu-id="763af-750">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-750">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="763af-751">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-751">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="763af-752">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-752">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="763af-753">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-753">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="763af-754">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-754">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="763af-755">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-755">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="763af-756">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-756">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="763af-757">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-757">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="763af-758">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-758">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="763af-759">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-759">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-760">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-760">Az.Resources</span></span>
- <span data-ttu-id="763af-761">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="763af-761">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="763af-762">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="763af-762">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="763af-763">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="763af-763">Az.ServiceBus</span></span>
* <span data-ttu-id="763af-764">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="763af-764">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="763af-765">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="763af-765">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-766">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-766">Az.Sql</span></span>
* <span data-ttu-id="763af-767">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="763af-767">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="763af-768">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="763af-768">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="763af-769">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="763af-769">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="763af-770">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-770">Az.Storage</span></span>
* <span data-ttu-id="763af-771">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="763af-771">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="763af-772">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="763af-772">Az.StorageSync</span></span>
* <span data-ttu-id="763af-773">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="763af-773">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="763af-774">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="763af-774">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="763af-775">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="763af-775">Az.Websites</span></span>
* <span data-ttu-id="763af-776">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="763af-776">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="763af-777">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-777">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="763af-778">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="763af-778">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="763af-779">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="763af-779">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="763af-780">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-780">Az.Accounts</span></span>
* <span data-ttu-id="763af-781">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="763af-781">Add support for profile cmdlets</span></span>
* <span data-ttu-id="763af-782">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="763af-782">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="763af-783">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="763af-783">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="763af-784">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="763af-784">Az.Advisor</span></span>
* <span data-ttu-id="763af-785">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="763af-785">GA release of Az.Advisor</span></span>
* <span data-ttu-id="763af-786">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="763af-786">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="763af-787">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="763af-787">Az.ApiManagement</span></span>
* <span data-ttu-id="763af-788">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="763af-788">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="763af-789">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="763af-789">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="763af-790">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-790">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="763af-791">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-791">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="763af-792">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="763af-792">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="763af-793">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="763af-793">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="763af-794">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="763af-794">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="763af-795">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="763af-795">Az.Automation</span></span>
* <span data-ttu-id="763af-796">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="763af-796">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-797">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-797">Az.Compute</span></span>
* <span data-ttu-id="763af-798">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-798">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="763af-799">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="763af-799">Az.DataFactory</span></span>
* <span data-ttu-id="763af-800">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="763af-800">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="763af-801">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="763af-801">Az.EventGrid</span></span>
* <span data-ttu-id="763af-802">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="763af-802">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="763af-803">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="763af-803">Az.IotHub</span></span>
* <span data-ttu-id="763af-804">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="763af-804">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-805">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-805">Az.Network</span></span>
* <span data-ttu-id="763af-806">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="763af-806">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="763af-807">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="763af-807">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="763af-808">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="763af-808">Az.PolicyInsights</span></span>
* <span data-ttu-id="763af-809">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="763af-809">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="763af-810">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="763af-810">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="763af-811">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="763af-811">Az.OperationalInsights</span></span>
* <span data-ttu-id="763af-812">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="763af-812">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="763af-813">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="763af-813">Az.RecoveryServices</span></span>
* <span data-ttu-id="763af-814">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="763af-814">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-815">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-815">Az.Resources</span></span>
    - <span data-ttu-id="763af-816">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="763af-816">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="763af-817">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-817">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="763af-818">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-818">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="763af-819">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-819">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="763af-820">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="763af-820">Az.ServiceBus</span></span>
* <span data-ttu-id="763af-821">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="763af-821">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-822">Az.Sql</span></span>
* <span data-ttu-id="763af-823">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="763af-823">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="763af-824">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="763af-824">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="763af-825">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="763af-825">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="763af-826">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="763af-826">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="763af-827">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="763af-827">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="763af-828">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="763af-828">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="763af-829">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="763af-829">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="763af-830">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="763af-830">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="763af-831">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="763af-831">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="763af-832">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-832">Az.Storage</span></span>
* <span data-ttu-id="763af-833">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="763af-833">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="763af-834">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="763af-834">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="763af-835">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="763af-835">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="763af-836">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="763af-836">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="763af-837">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="763af-837">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="763af-838">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="763af-838">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="763af-839">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="763af-839">Set-AzStorageAccount</span></span>
* <span data-ttu-id="763af-840">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="763af-840">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="763af-841">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="763af-841">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="763af-842">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="763af-842">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="763af-843">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="763af-843">Az.StorageSync</span></span>
* <span data-ttu-id="763af-844">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="763af-844">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="763af-845">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="763af-845">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="763af-846">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-846">Az.Accounts</span></span>
* <span data-ttu-id="763af-847">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="763af-847">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="763af-848">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="763af-848">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="763af-849">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="763af-849">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="763af-850">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="763af-850">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="763af-851">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="763af-851">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-852">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-852">Az.Compute</span></span>
* <span data-ttu-id="763af-853">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="763af-853">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="763af-854">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="763af-854">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="763af-855">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="763af-855">Az.Dns</span></span>
* <span data-ttu-id="763af-856">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="763af-856">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="763af-857">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="763af-857">Az.EventGrid</span></span>
* <span data-ttu-id="763af-858">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="763af-858">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="763af-859">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="763af-859">New cmdlets:</span></span>
    - <span data-ttu-id="763af-860">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="763af-860">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="763af-861">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="763af-861">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="763af-862">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="763af-862">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="763af-863">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="763af-863">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="763af-864">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="763af-864">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="763af-865">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="763af-865">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="763af-866">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="763af-866">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="763af-867">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="763af-867">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="763af-868">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="763af-868">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="763af-869">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="763af-869">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="763af-870">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="763af-870">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="763af-871">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="763af-871">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="763af-872">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="763af-872">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="763af-873">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="763af-873">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="763af-874">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="763af-874">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="763af-875">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="763af-875">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="763af-876">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="763af-876">Updated cmdlets:</span></span>
    - <span data-ttu-id="763af-877">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="763af-877">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="763af-878">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="763af-878">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="763af-879">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="763af-879">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="763af-880">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="763af-880">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="763af-881">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="763af-881">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="763af-882">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="763af-882">Event subscription expiration date,</span></span>
            - <span data-ttu-id="763af-883">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="763af-883">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="763af-884">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="763af-884">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="763af-885">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="763af-885">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="763af-886">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="763af-886">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="763af-887">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="763af-887">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="763af-888">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="763af-888">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="763af-889">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="763af-889">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="763af-890">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="763af-890">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="763af-891">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="763af-891">Az.FrontDoor</span></span>
* <span data-ttu-id="763af-892">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="763af-892">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="763af-893">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="763af-893">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="763af-894">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="763af-894">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="763af-895">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="763af-895">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-896">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-896">Az.Network</span></span>
* <span data-ttu-id="763af-897">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-897">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="763af-898">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="763af-898">New cmdlets</span></span>
        - <span data-ttu-id="763af-899">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="763af-899">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="763af-900">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-900">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="763af-901">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="763af-901">New cmdlets</span></span> 
        - <span data-ttu-id="763af-902">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="763af-902">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="763af-903">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-903">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="763af-904">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="763af-904">New cmdlets</span></span> 
        - <span data-ttu-id="763af-905">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="763af-905">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="763af-906">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="763af-906">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="763af-907">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="763af-907">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="763af-908">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="763af-908">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="763af-909">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="763af-909">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="763af-910">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-910">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="763af-911">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="763af-911">New cmdlets</span></span>
        - <span data-ttu-id="763af-912">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="763af-912">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="763af-913">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="763af-913">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="763af-914">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="763af-914">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="763af-915">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="763af-915">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="763af-916">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="763af-916">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="763af-917">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="763af-917">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="763af-918">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="763af-918">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="763af-919">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-919">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="763af-920">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-920">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="763af-921">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="763af-921">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="763af-922">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="763af-922">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="763af-923">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="763af-923">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="763af-924">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="763af-924">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="763af-925">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="763af-925">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="763af-926">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="763af-926">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="763af-927">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="763af-927">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="763af-928">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="763af-928">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="763af-929">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="763af-929">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="763af-930">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="763af-930">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="763af-931">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="763af-931">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="763af-932">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="763af-932">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="763af-933">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="763af-933">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="763af-934">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="763af-934">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="763af-935">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="763af-935">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="763af-936">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-936">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="763af-937">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-937">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="763af-938">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-938">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="763af-939">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="763af-939">Az.OperationalInsights</span></span>
* <span data-ttu-id="763af-940">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="763af-940">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-941">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-941">Az.Resources</span></span>
* <span data-ttu-id="763af-942">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="763af-942">Support for additional Template Export options</span></span>
    - <span data-ttu-id="763af-943">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="763af-943">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="763af-944">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="763af-944">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="763af-945">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="763af-945">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="763af-946">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="763af-946">Az.ServiceFabric</span></span>
* <span data-ttu-id="763af-947">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="763af-947">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-948">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-948">Az.Sql</span></span>
* <span data-ttu-id="763af-949">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="763af-949">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="763af-950">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="763af-950">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="763af-951">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="763af-951">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="763af-952">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="763af-952">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="763af-953">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="763af-953">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="763af-954">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="763af-954">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="763af-955">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="763af-955">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="763af-956">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="763af-956">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="763af-957">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-957">Az.Storage</span></span>
* <span data-ttu-id="763af-958">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="763af-958">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="763af-959">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="763af-959">New-AzStorageAccount</span></span>
* <span data-ttu-id="763af-960">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="763af-960">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="763af-961">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="763af-961">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="763af-962">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="763af-962">Az.Websites</span></span>
* <span data-ttu-id="763af-963">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="763af-963">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="763af-964">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-964">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="763af-965">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="763af-965">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="763af-966">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="763af-966">Az.Cdn</span></span>
* <span data-ttu-id="763af-967">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="763af-967">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-968">Az.Compute</span></span>
* <span data-ttu-id="763af-969">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="763af-969">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="763af-970">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="763af-970">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="763af-971">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="763af-971">Az.EventHub</span></span>
* <span data-ttu-id="763af-972">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="763af-972">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="763af-973">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="763af-973">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-974">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-974">Az.Network</span></span>
* <span data-ttu-id="763af-975">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="763af-975">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="763af-976">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="763af-976">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="763af-977">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="763af-977">Az.PolicyInsights</span></span>
* <span data-ttu-id="763af-978">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="763af-978">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="763af-979">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="763af-979">Az.RecoveryServices</span></span>
* <span data-ttu-id="763af-980">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="763af-980">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="763af-981">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="763af-981">Az.ServiceBus</span></span>
* <span data-ttu-id="763af-982">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="763af-982">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="763af-983">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="763af-983">Az.ServiceFabric</span></span>
* <span data-ttu-id="763af-984">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="763af-984">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="763af-985">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="763af-985">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-986">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-986">Az.Sql</span></span>
* <span data-ttu-id="763af-987">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="763af-987">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="763af-988">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="763af-988">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="763af-989">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="763af-989">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="763af-990">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="763af-990">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="763af-991">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="763af-991">Az.Websites</span></span>
* <span data-ttu-id="763af-992">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="763af-992">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="763af-993">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="763af-993">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="763af-994">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="763af-994">Az.ApiManagement</span></span>
* <span data-ttu-id="763af-995">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="763af-995">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="763af-996">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="763af-996">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="763af-997">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="763af-997">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="763af-998">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="763af-998">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="763af-999">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="763af-999">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="763af-1000">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1000">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="763af-1001">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="763af-1001">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="763af-1002">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="763af-1002">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="763af-1003">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="763af-1003">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="763af-1004">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="763af-1004">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="763af-1005">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="763af-1005">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="763af-1006">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="763af-1006">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="763af-1007">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-1007">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="763af-1008">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="763af-1008">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="763af-1009">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="763af-1009">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="763af-1010">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="763af-1010">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="763af-1011">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="763af-1011">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="763af-1012">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-1012">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="763af-1013">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="763af-1013">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="763af-1014">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="763af-1014">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="763af-1015">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="763af-1015">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="763af-1016">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="763af-1016">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="763af-1017">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="763af-1017">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="763af-1018">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="763af-1018">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="763af-1019">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="763af-1019">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="763af-1020">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="763af-1020">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="763af-1021">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="763af-1021">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="763af-1022">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="763af-1022">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="763af-1023">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="763af-1023">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="763af-1024">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="763af-1024">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="763af-1025">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="763af-1025">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="763af-1026">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="763af-1026">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="763af-1027">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="763af-1027">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="763af-1028">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-1028">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="763af-1029">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="763af-1029">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="763af-1030">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="763af-1030">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="763af-1031">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="763af-1031">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="763af-1032">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="763af-1032">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="763af-1033">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="763af-1033">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="763af-1034">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-1034">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="763af-1035">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="763af-1035">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="763af-1036">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="763af-1036">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="763af-1037">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="763af-1037">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="763af-1038">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="763af-1038">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="763af-1039">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-1039">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="763af-1040">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="763af-1040">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="763af-1041">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="763af-1041">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="763af-1042">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="763af-1042">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="763af-1043">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-1043">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="763af-1044">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="763af-1044">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="763af-1045">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="763af-1045">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="763af-1046">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="763af-1046">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="763af-1047">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="763af-1047">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="763af-1048">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-1048">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="763af-1049">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="763af-1049">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="763af-1050">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="763af-1050">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="763af-1051">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-1051">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="763af-1052">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="763af-1052">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="763af-1053">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="763af-1053">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="763af-1054">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="763af-1054">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="763af-1055">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-1055">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="763af-1056">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="763af-1056">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="763af-1057">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="763af-1057">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="763af-1058">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="763af-1058">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="763af-1059">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="763af-1059">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="763af-1060">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="763af-1060">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="763af-1061">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="763af-1061">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="763af-1062">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="763af-1062">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="763af-1063">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="763af-1063">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="763af-1064">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="763af-1064">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="763af-1065">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="763af-1065">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="763af-1066">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="763af-1066">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="763af-1067">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="763af-1067">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="763af-1068">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="763af-1068">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="763af-1069">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="763af-1069">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="763af-1070">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="763af-1070">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="763af-1071">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="763af-1071">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="763af-1072">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="763af-1072">Az.Automation</span></span>
* <span data-ttu-id="763af-1073">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="763af-1073">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="763af-1074">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="763af-1074">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="763af-1075">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="763af-1075">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="763af-1076">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="763af-1076">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="763af-1077">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="763af-1077">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="763af-1078">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="763af-1078">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="763af-1079">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="763af-1079">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-1080">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-1080">Az.Compute</span></span>
* <span data-ttu-id="763af-1081">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-1081">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="763af-1082">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="763af-1082">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="763af-1083">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="763af-1083">Az.DataLakeStore</span></span>
* <span data-ttu-id="763af-1084">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="763af-1084">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="763af-1085">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="763af-1085">Az.Monitor</span></span>
* <span data-ttu-id="763af-1086">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="763af-1086">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-1087">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-1087">Az.Network</span></span>
* <span data-ttu-id="763af-1088">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="763af-1088">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="763af-1089">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="763af-1089">Updated cmdlet:</span></span>
        - <span data-ttu-id="763af-1090">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="763af-1090">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="763af-1091">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="763af-1091">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-1092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-1092">Az.Resources</span></span>
* <span data-ttu-id="763af-1093">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="763af-1093">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-1094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-1094">Az.Sql</span></span>
* <span data-ttu-id="763af-1095">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="763af-1095">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="763af-1096">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="763af-1096">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="763af-1097">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-1097">Az.Accounts</span></span>
* <span data-ttu-id="763af-1098">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="763af-1098">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="763af-1099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="763af-1099">Az.CognitiveServices</span></span>
* <span data-ttu-id="763af-1100">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="763af-1100">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="763af-1101">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="763af-1101">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-1102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-1102">Az.Compute</span></span>
* <span data-ttu-id="763af-1103">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="763af-1103">Proximity placement group feature.</span></span>
    - <span data-ttu-id="763af-1104">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="763af-1104">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="763af-1105">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="763af-1105">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="763af-1106">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="763af-1106">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="763af-1107">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="763af-1107">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="763af-1108">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1108">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="763af-1109">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="763af-1109">Breaking changes</span></span>
    - <span data-ttu-id="763af-1110">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="763af-1110">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="763af-1111">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="763af-1111">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="763af-1112">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="763af-1112">Az.DeploymentManager</span></span>
* <span data-ttu-id="763af-1113">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="763af-1113">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="763af-1114">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="763af-1114">Az.Dns</span></span>
* <span data-ttu-id="763af-1115">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="763af-1115">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="763af-1116">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1116">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="763af-1117">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="763af-1117">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="763af-1118">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="763af-1118">Az.FrontDoor</span></span>
* <span data-ttu-id="763af-1119">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="763af-1119">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="763af-1120">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="763af-1120">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="763af-1121">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="763af-1121">Az.HDInsight</span></span>
* <span data-ttu-id="763af-1122">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="763af-1122">Removed two cmdlets:</span></span>
    - <span data-ttu-id="763af-1123">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="763af-1123">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="763af-1124">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="763af-1124">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="763af-1125">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="763af-1125">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="763af-1126">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="763af-1126">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="763af-1127">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="763af-1127">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="763af-1128">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="763af-1128">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="763af-1129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="763af-1129">Az.Monitor</span></span>
* <span data-ttu-id="763af-1130">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="763af-1130">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="763af-1131">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="763af-1131">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="763af-1132">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="763af-1132">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="763af-1133">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="763af-1133">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="763af-1134">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="763af-1134">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="763af-1135">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="763af-1135">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="763af-1136">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="763af-1136">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="763af-1137">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="763af-1137">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="763af-1138">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="763af-1138">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="763af-1139">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="763af-1139">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="763af-1140">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="763af-1140">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="763af-1141">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="763af-1141">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="763af-1142">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="763af-1142">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="763af-1143">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="763af-1143">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-1144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-1144">Az.Network</span></span>
* <span data-ttu-id="763af-1145">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-1145">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="763af-1146">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="763af-1146">New cmdlets</span></span>
        - <span data-ttu-id="763af-1147">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="763af-1147">New-AzNatGateway</span></span>
        - <span data-ttu-id="763af-1148">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="763af-1148">Get-AzNatGateway</span></span>
        - <span data-ttu-id="763af-1149">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="763af-1149">Set-AzNatGateway</span></span>
        - <span data-ttu-id="763af-1150">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="763af-1150">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="763af-1151">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="763af-1151">Updated cmdlets</span></span>
        - <span data-ttu-id="763af-1152">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="763af-1152">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="763af-1153">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="763af-1153">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="763af-1154">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="763af-1154">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="763af-1155">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="763af-1155">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="763af-1156">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="763af-1156">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="763af-1157">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="763af-1157">Az.PolicyInsights</span></span>
* <span data-ttu-id="763af-1158">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="763af-1158">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="763af-1159">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="763af-1159">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="763af-1160">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="763af-1160">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="763af-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="763af-1161">Az.RecoveryServices</span></span>
* <span data-ttu-id="763af-1162">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="763af-1162">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="763af-1163">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="763af-1163">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="763af-1164">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="763af-1164">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="763af-1165">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="763af-1165">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="763af-1166">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="763af-1166">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="763af-1167">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="763af-1167">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="763af-1168">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="763af-1168">Az.Relay</span></span>
* <span data-ttu-id="763af-1169">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="763af-1169">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="763af-1170">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="763af-1170">Az.ServiceBus</span></span>
* <span data-ttu-id="763af-1171">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="763af-1171">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="763af-1172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-1172">Az.Storage</span></span>
* <span data-ttu-id="763af-1173">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage.\* névtérről a Microsoft.Azure.Storage.\* névtérre)</span><span class="sxs-lookup"><span data-stu-id="763af-1173">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="763af-1174">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="763af-1174">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="763af-1175">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="763af-1175">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="763af-1176">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="763af-1176">New-AzStorageAccount</span></span>
* <span data-ttu-id="763af-1177">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="763af-1177">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="763af-1178">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="763af-1178">New-AzStorageAccount</span></span>
    - <span data-ttu-id="763af-1179">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="763af-1179">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="763af-1180">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="763af-1180">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="763af-1181">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="763af-1181">Az.Websites</span></span>
* <span data-ttu-id="763af-1182">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1182">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="763af-1183">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="763af-1183">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="763af-1184">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="763af-1184">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="763af-1185">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="763af-1185">Highlights since the last major release</span></span>
* <span data-ttu-id="763af-1186">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="763af-1186">General availability of `Az` module</span></span>
* <span data-ttu-id="763af-1187">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="763af-1187">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="763af-1188">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="763af-1188">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="763af-1189">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1189">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="763af-1190">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1190">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="763af-1191">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1191">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="763af-1192">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1192">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="763af-1193">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-1193">Az.Accounts</span></span>
* <span data-ttu-id="763af-1194">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-1194">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="763af-1195">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="763af-1195">Az.Batch</span></span>
* <span data-ttu-id="763af-1196">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1196">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="763af-1197">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="763af-1197">Az.Cdn</span></span>
* <span data-ttu-id="763af-1198">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="763af-1199">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="763af-1199">Az.CognitiveServices</span></span>
* <span data-ttu-id="763af-1200">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1200">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-1201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-1201">Az.Compute</span></span>
* <span data-ttu-id="763af-1202">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="763af-1202">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="763af-1203">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="763af-1204">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="763af-1204">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="763af-1205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="763af-1205">Az.DataFactory</span></span>
* <span data-ttu-id="763af-1206">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="763af-1206">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="763af-1207">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="763af-1207">Az.DataLakeStore</span></span>
* <span data-ttu-id="763af-1208">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="763af-1209">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="763af-1209">Az.EventGrid</span></span>
* <span data-ttu-id="763af-1210">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="763af-1210">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="763af-1211">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="763af-1211">Az.EventHub</span></span>
* <span data-ttu-id="763af-1212">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="763af-1212">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="763af-1213">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="763af-1213">Az.HDInsight</span></span>
* <span data-ttu-id="763af-1214">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1214">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="763af-1215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="763af-1215">Az.IotHub</span></span>
* <span data-ttu-id="763af-1216">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1216">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="763af-1217">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="763af-1217">Az.KeyVault</span></span>
* <span data-ttu-id="763af-1218">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1218">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="763af-1219">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="763af-1219">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="763af-1220">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="763af-1220">Az.MachineLearning</span></span>
* <span data-ttu-id="763af-1221">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1221">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="763af-1222">Az.Media</span><span class="sxs-lookup"><span data-stu-id="763af-1222">Az.Media</span></span>
* <span data-ttu-id="763af-1223">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1223">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="763af-1224">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="763af-1224">Az.Monitor</span></span>
  * <span data-ttu-id="763af-1225">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="763af-1225">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="763af-1226">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="763af-1226">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="763af-1227">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="763af-1227">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="763af-1228">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="763af-1228">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="763af-1229">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="763af-1229">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="763af-1230">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="763af-1230">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="763af-1231">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="763af-1231">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-1232">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-1232">Az.Network</span></span>
* <span data-ttu-id="763af-1233">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1233">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="763af-1234">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="763af-1234">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="763af-1235">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="763af-1235">Az.NotificationHubs</span></span>
* <span data-ttu-id="763af-1236">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1236">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="763af-1237">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="763af-1237">Az.OperationalInsights</span></span>
* <span data-ttu-id="763af-1238">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="763af-1239">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="763af-1239">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="763af-1240">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="763af-1241">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="763af-1241">Az.RecoveryServices</span></span>
* <span data-ttu-id="763af-1242">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1242">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="763af-1243">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="763af-1243">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="763af-1244">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="763af-1244">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="763af-1245">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="763af-1245">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="763af-1246">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="763af-1246">Az.RedisCache</span></span>
* <span data-ttu-id="763af-1247">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1247">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-1248">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-1248">Az.Resources</span></span>
* <span data-ttu-id="763af-1249">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="763af-1249">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-1250">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-1250">Az.Sql</span></span>
* <span data-ttu-id="763af-1251">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="763af-1251">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="763af-1252">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="763af-1253">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="763af-1253">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="763af-1254">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="763af-1254">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="763af-1255">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="763af-1255">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="763af-1256">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="763af-1256">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="763af-1257">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="763af-1257">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="763af-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="763af-1258">Az.Websites</span></span>
* <span data-ttu-id="763af-1259">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="763af-1259">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="763af-1260">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="763af-1260">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="763af-1261">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="763af-1261">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="763af-1262">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="763af-1262">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="763af-1263">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="763af-1263">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="763af-1264">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="763af-1264">Highlights since the last major release</span></span>
* <span data-ttu-id="763af-1265">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="763af-1265">General availability of `Az` module</span></span>
* <span data-ttu-id="763af-1266">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="763af-1266">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="763af-1267">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="763af-1267">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="763af-1268">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1268">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="763af-1269">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1269">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="763af-1270">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1270">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="763af-1271">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1271">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="763af-1272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-1272">Az.Accounts</span></span>
* <span data-ttu-id="763af-1273">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="763af-1273">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="763af-1274">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="763af-1274">Az.AnalysisServices</span></span>
* <span data-ttu-id="763af-1275">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="763af-1275">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="763af-1276">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="763af-1276">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="763af-1277">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="763af-1277">Az.Automation</span></span>
* <span data-ttu-id="763af-1278">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="763af-1278">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="763af-1279">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="763af-1279">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="763af-1280">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1280">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-1281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-1281">Az.Compute</span></span>
* <span data-ttu-id="763af-1282">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1282">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="763af-1283">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="763af-1283">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="763af-1284">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="763af-1284">Az.ContainerInstance</span></span>
* <span data-ttu-id="763af-1285">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="763af-1285">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="763af-1286">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="763af-1286">Az.DataFactory</span></span>
* <span data-ttu-id="763af-1287">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="763af-1287">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="763af-1288">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="763af-1288">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-1289">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-1289">Az.Resources</span></span>
* <span data-ttu-id="763af-1290">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="763af-1290">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="763af-1291">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1291">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="763af-1292">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="763af-1292">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="763af-1293">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="763af-1293">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="763af-1294">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="763af-1294">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="763af-1295">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="763af-1295">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-1296">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-1296">Az.Sql</span></span>
* <span data-ttu-id="763af-1297">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="763af-1297">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="763af-1298">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-1298">Az.Storage</span></span>
* <span data-ttu-id="763af-1299">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="763af-1299">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="763af-1300">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="763af-1300">New-AzStorageContext</span></span>
* <span data-ttu-id="763af-1301">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="763af-1301">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="763af-1302">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="763af-1302">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="763af-1303">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="763af-1303">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="763af-1304">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="763af-1304">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="763af-1305">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="763af-1305">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="763af-1306">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="763af-1306">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="763af-1307">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="763af-1307">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="763af-1308">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="763af-1308">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="763af-1309">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="763af-1309">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="763af-1310">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="763af-1310">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="763af-1311">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="763af-1311">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="763af-1312">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="763af-1312">Highlights since the last major release</span></span>
* <span data-ttu-id="763af-1313">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="763af-1313">General availability of `Az` module</span></span>
* <span data-ttu-id="763af-1314">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="763af-1314">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="763af-1315">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="763af-1315">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="763af-1316">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1316">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="763af-1317">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1317">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="763af-1318">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1318">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="763af-1319">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1319">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="763af-1320">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="763af-1320">Az.Automation</span></span>
* <span data-ttu-id="763af-1321">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="763af-1321">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="763af-1322">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="763af-1322">Dynamic grouping</span></span>
    * <span data-ttu-id="763af-1323">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="763af-1323">Pre-Post script</span></span>
    * <span data-ttu-id="763af-1324">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="763af-1324">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-1325">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-1325">Az.Compute</span></span>
* <span data-ttu-id="763af-1326">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1326">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="763af-1327">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="763af-1327">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="763af-1328">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="763af-1328">Az.KeyVault</span></span>
* <span data-ttu-id="763af-1329">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1329">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-1330">Az.Network</span></span>
* <span data-ttu-id="763af-1331">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1331">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="763af-1332">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-1332">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="763af-1333">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="763af-1333">Az.RecoveryServices</span></span>
* <span data-ttu-id="763af-1334">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="763af-1334">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="763af-1335">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1335">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-1336">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-1336">Az.Resources</span></span>
* <span data-ttu-id="763af-1337">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1337">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="763af-1338">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-1338">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-1339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-1339">Az.Sql</span></span>
* <span data-ttu-id="763af-1340">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="763af-1340">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="763af-1341">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-1341">Az.Storage</span></span>
* <span data-ttu-id="763af-1342">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="763af-1342">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="763af-1343">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="763af-1343">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="763af-1344">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="763af-1344">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="763af-1345">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="763af-1345">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="763af-1346">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="763af-1346">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="763af-1347">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="763af-1347">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="763af-1348">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="763af-1348">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="763af-1349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="763af-1349">Az.Websites</span></span>
* <span data-ttu-id="763af-1350">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="763af-1350">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="763af-1351">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="763af-1351">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="763af-1352">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-1352">Az.Accounts</span></span>
* <span data-ttu-id="763af-1353">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="763af-1353">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="763af-1354">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-1354">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="763af-1355">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="763af-1355">Az.Automation</span></span>
* <span data-ttu-id="763af-1356">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1356">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="763af-1357">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="763af-1357">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="763af-1358">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="763af-1358">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="763af-1359">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="763af-1359">Az.Cdn</span></span>
* <span data-ttu-id="763af-1360">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="763af-1360">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-1361">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-1361">Az.Compute</span></span>
* <span data-ttu-id="763af-1362">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1362">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="763af-1363">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="763af-1363">Az.DataFactory</span></span>
* <span data-ttu-id="763af-1364">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="763af-1364">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="763af-1365">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="763af-1365">Az.LogicApp</span></span>
* <span data-ttu-id="763af-1366">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="763af-1366">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-1367">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-1367">Az.Network</span></span>
* <span data-ttu-id="763af-1368">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1368">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="763af-1369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="763af-1369">Az.RecoveryServices</span></span>
* <span data-ttu-id="763af-1370">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="763af-1370">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="763af-1371">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="763af-1371">SDK Update</span></span>
* <span data-ttu-id="763af-1372">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="763af-1372">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="763af-1373">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-1373">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-1374">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-1374">Az.Resources</span></span>
* <span data-ttu-id="763af-1375">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1375">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="763af-1376">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="763af-1376">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="763af-1377">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="763af-1377">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="763af-1378">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="763af-1378">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="763af-1379">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="763af-1379">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="763af-1380">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="763af-1380">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-1381">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-1381">Az.Sql</span></span>
* <span data-ttu-id="763af-1382">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="763af-1382">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="763af-1383">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="763af-1383">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="763af-1384">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-1384">Az.Storage</span></span>
* <span data-ttu-id="763af-1385">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="763af-1385">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="763af-1386">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="763af-1386">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="763af-1387">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="763af-1387">Az.AnalysisServices</span></span>
* <span data-ttu-id="763af-1388">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="763af-1388">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="763af-1389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="763af-1389">Az.Automation</span></span>
* <span data-ttu-id="763af-1390">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-1390">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="763af-1391">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-1391">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="763af-1392">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1392">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="763af-1393">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="763af-1393">Az.CognitiveServices</span></span>
* <span data-ttu-id="763af-1394">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="763af-1394">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-1395">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-1395">Az.Compute</span></span>
* <span data-ttu-id="763af-1396">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="763af-1396">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="763af-1397">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="763af-1397">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="763af-1398">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-1398">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="763af-1399">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="763af-1399">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="763af-1400">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="763af-1400">Az.DataLakeStore</span></span>
* <span data-ttu-id="763af-1401">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="763af-1401">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="763af-1402">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="763af-1402">Az.EventHub</span></span>
* <span data-ttu-id="763af-1403">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="763af-1403">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="763af-1404">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="763af-1404">Az.KeyVault</span></span>
* <span data-ttu-id="763af-1405">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="763af-1405">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="763af-1406">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="763af-1406">Az.LogicApp</span></span>
* <span data-ttu-id="763af-1407">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="763af-1407">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="763af-1408">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="763af-1408">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="763af-1409">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="763af-1409">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="763af-1410">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="763af-1410">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="763af-1411">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="763af-1411">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="763af-1412">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="763af-1412">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="763af-1413">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="763af-1413">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="763af-1414">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="763af-1414">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="763af-1415">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="763af-1415">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="763af-1416">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="763af-1416">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="763af-1417">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="763af-1417">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="763af-1418">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="763af-1418">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="763af-1419">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="763af-1419">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="763af-1420">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="763af-1420">Az.Monitor</span></span>
* <span data-ttu-id="763af-1421">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-1421">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-1422">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-1422">Az.Network</span></span>
* <span data-ttu-id="763af-1423">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="763af-1423">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="763af-1424">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="763af-1424">Az.OperationalInsights</span></span>
* <span data-ttu-id="763af-1425">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="763af-1425">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="763af-1426">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="763af-1426">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="763af-1427">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="763af-1427">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="763af-1428">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-1428">Az.Resources</span></span>
* <span data-ttu-id="763af-1429">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="763af-1429">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="763af-1430">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="763af-1430">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="763af-1431">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="763af-1431">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="763af-1432">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="763af-1432">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-1433">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-1433">Az.Sql</span></span>
* <span data-ttu-id="763af-1434">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-1434">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="763af-1435">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="763af-1435">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="763af-1436">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="763af-1436">Az.Websites</span></span>
* <span data-ttu-id="763af-1437">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="763af-1437">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="763af-1438">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="763af-1438">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="763af-1439">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-1439">Az.Accounts</span></span>
* <span data-ttu-id="763af-1440">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="763af-1440">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="763af-1441">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="763af-1441">Az.AnalysisServices</span></span>
<span data-ttu-id="763af-1442">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="763af-1442">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-1443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-1443">Az.Compute</span></span>
* <span data-ttu-id="763af-1444">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="763af-1444">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="763af-1445">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="763af-1445">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="763af-1446">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="763af-1446">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="763af-1447">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="763af-1447">Az.RecoveryServices</span></span>
<span data-ttu-id="763af-1448">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="763af-1448">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-1449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-1449">Az.Resources</span></span>
* <span data-ttu-id="763af-1450">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="763af-1450">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="763af-1451">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="763af-1451">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="763af-1452">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="763af-1452">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="763af-1453">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="763af-1453">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-1454">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-1454">Az.Sql</span></span>
* <span data-ttu-id="763af-1455">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-1455">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="763af-1456">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="763af-1456">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="763af-1457">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="763af-1457">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="763af-1458">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="763af-1458">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="763af-1459">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-1459">Az.Accounts</span></span>
* <span data-ttu-id="763af-1460">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="763af-1460">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="763af-1461">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="763af-1461">Az.AnalysisServices</span></span>
* <span data-ttu-id="763af-1462">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="763af-1462">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="763af-1463">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="763af-1463">Az.RecoveryServices</span></span>
* <span data-ttu-id="763af-1464">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="763af-1464">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="763af-1465">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="763af-1465">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="763af-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-1466">Az.Accounts</span></span>
* <span data-ttu-id="763af-1467">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1467">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="763af-1468">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="763af-1468">Update incorrect online help URLs</span></span>
* <span data-ttu-id="763af-1469">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="763af-1469">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="763af-1470">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="763af-1470">Az.Aks</span></span>
* <span data-ttu-id="763af-1471">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="763af-1471">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="763af-1472">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="763af-1472">Az.Automation</span></span>
* <span data-ttu-id="763af-1473">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="763af-1473">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="763af-1474">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="763af-1474">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="763af-1475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="763af-1475">Az.Cdn</span></span>
* <span data-ttu-id="763af-1476">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="763af-1476">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-1477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-1477">Az.Compute</span></span>
* <span data-ttu-id="763af-1478">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="763af-1478">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="763af-1479">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="763af-1479">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="763af-1480">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="763af-1480">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="763af-1481">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="763af-1481">Az.ContainerRegistry</span></span>
* <span data-ttu-id="763af-1482">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="763af-1482">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="763af-1483">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="763af-1483">Az.DataFactory</span></span>
* <span data-ttu-id="763af-1484">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="763af-1484">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="763af-1485">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="763af-1485">Az.DataLakeStore</span></span>
* <span data-ttu-id="763af-1486">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="763af-1486">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="763af-1487">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="763af-1487">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="763af-1488">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="763af-1488">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="763af-1489">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="763af-1489">Az.IotHub</span></span>
* <span data-ttu-id="763af-1490">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="763af-1490">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="763af-1491">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="763af-1491">Az.KeyVault</span></span>
* <span data-ttu-id="763af-1492">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="763af-1492">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-1493">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-1493">Az.Network</span></span>
* <span data-ttu-id="763af-1494">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="763af-1494">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-1495">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-1495">Az.Resources</span></span>
* <span data-ttu-id="763af-1496">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="763af-1496">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="763af-1497">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="763af-1497">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="763af-1498">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="763af-1498">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="763af-1499">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="763af-1499">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="763af-1500">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="763af-1500">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="763af-1501">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="763af-1501">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="763af-1502">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="763af-1502">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="763af-1503">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="763af-1503">Az.ServiceFabric</span></span>
* <span data-ttu-id="763af-1504">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="763af-1504">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="763af-1505">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="763af-1505">Fix some error messages.</span></span>
* <span data-ttu-id="763af-1506">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="763af-1506">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="763af-1507">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="763af-1507">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="763af-1508">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="763af-1508">Az.SignalR</span></span>
* <span data-ttu-id="763af-1509">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="763af-1509">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-1510">Az.Sql</span></span>
* <span data-ttu-id="763af-1511">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="763af-1511">Update incorrect online help URLs</span></span>
* <span data-ttu-id="763af-1512">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="763af-1512">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="763af-1513">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="763af-1513">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="763af-1514">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="763af-1514">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="763af-1515">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-1515">Az.Storage</span></span>
* <span data-ttu-id="763af-1516">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="763af-1516">Update incorrect online help URLs</span></span>
* <span data-ttu-id="763af-1517">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="763af-1517">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="763af-1518">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="763af-1518">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="763af-1519">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="763af-1519">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="763af-1520">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="763af-1520">Az.TrafficManager</span></span>
* <span data-ttu-id="763af-1521">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="763af-1521">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="763af-1522">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="763af-1522">Az.Websites</span></span>
* <span data-ttu-id="763af-1523">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="763af-1523">Update incorrect online help URLs</span></span>
* <span data-ttu-id="763af-1524">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="763af-1524">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="763af-1525">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="763af-1525">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="763af-1526">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="763af-1526">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="763af-1527">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-1527">Az.Accounts</span></span>
* <span data-ttu-id="763af-1528">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="763af-1528">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-1529">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-1529">Az.Compute</span></span>
* <span data-ttu-id="763af-1530">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="763af-1530">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="763af-1531">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="763af-1531">Updated the description of ID in help files</span></span>
* <span data-ttu-id="763af-1532">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="763af-1532">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="763af-1533">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="763af-1533">Az.DataLakeStore</span></span>
* <span data-ttu-id="763af-1534">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="763af-1534">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="763af-1535">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="763af-1535">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="763af-1536">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="763af-1536">Az.EventGrid</span></span>
* <span data-ttu-id="763af-1537">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="763af-1537">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="763af-1538">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="763af-1538">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="763af-1539">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="763af-1539">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="763af-1540">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="763af-1540">Event Time-To-Live,</span></span>
        - <span data-ttu-id="763af-1541">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="763af-1541">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="763af-1542">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="763af-1542">Dead letter endpoint.</span></span>
    - <span data-ttu-id="763af-1543">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="763af-1543">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="763af-1544">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="763af-1544">Event Time-To-Live,</span></span>
        - <span data-ttu-id="763af-1545">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="763af-1545">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="763af-1546">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="763af-1546">Dead letter endpoint.</span></span>
* <span data-ttu-id="763af-1547">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="763af-1547">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="763af-1548">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="763af-1548">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="763af-1549">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="763af-1549">Az.IotHub</span></span>
* <span data-ttu-id="763af-1550">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="763af-1550">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="763af-1551">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="763af-1551">Az.LogicApp</span></span>
* <span data-ttu-id="763af-1552">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="763af-1552">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-1553">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-1553">Az.Resources</span></span>
* <span data-ttu-id="763af-1554">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="763af-1554">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="763af-1555">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="763af-1555">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="763af-1556">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="763af-1556">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="763af-1557">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="763af-1557">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="763af-1558">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="763af-1558">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="763af-1559">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="763af-1559">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="763af-1560">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="763af-1560">Az.SignalR</span></span>
* <span data-ttu-id="763af-1561">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="763af-1561">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-1562">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-1562">Az.Sql</span></span>
* <span data-ttu-id="763af-1563">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="763af-1563">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="763af-1564">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-1564">Az.Storage</span></span>
* <span data-ttu-id="763af-1565">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="763af-1565">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="763af-1566">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="763af-1566">New-AzStorageContext</span></span>
* <span data-ttu-id="763af-1567">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="763af-1567">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="763af-1568">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="763af-1568">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="763af-1569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="763af-1569">Az.Websites</span></span>
* <span data-ttu-id="763af-1570">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="763af-1570">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="763af-1571">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="763af-1571">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="763af-1572">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="763af-1572">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="763af-1573">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="763af-1573">General</span></span>

- <span data-ttu-id="763af-1574">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="763af-1574">General Availability of Az Module</span></span>
- <span data-ttu-id="763af-1575">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1575">Online help for each module</span></span>
- <span data-ttu-id="763af-1576">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="763af-1576">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="763af-1577">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="763af-1577">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="763af-1578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-1578">Az.Accounts</span></span>
- <span data-ttu-id="763af-1579">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="763af-1579">Changed from Az.Profile</span></span>
- <span data-ttu-id="763af-1580">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1580">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="763af-1581">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="763af-1581">Az.ApiManagement</span></span>
- <span data-ttu-id="763af-1582">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="763af-1582">Fixes for #7002</span></span>
- <span data-ttu-id="763af-1583">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="763af-1583">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="763af-1584">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="763af-1584">Az.Batch</span></span>
- <span data-ttu-id="763af-1585">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="763af-1585">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="763af-1586">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="763af-1586">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="763af-1587">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="763af-1587">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="763af-1588">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="763af-1588">Az.Billing</span></span>
- <span data-ttu-id="763af-1589">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="763af-1589">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="763af-1590">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="763af-1590">Az.CognitivServices</span></span>
- <span data-ttu-id="763af-1591">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="763af-1591">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="763af-1592">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="763af-1592">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="763af-1593">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="763af-1593">Az.ContainerInstance</span></span>
- <span data-ttu-id="763af-1594">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="763af-1594">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="763af-1595">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="763af-1595">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="763af-1596">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="763af-1596">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="763af-1597">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="763af-1597">Az.DataLakeStore</span></span>
- <span data-ttu-id="763af-1598">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="763af-1598">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="763af-1599">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="763af-1599">Az.Monitor</span></span>
- <span data-ttu-id="763af-1600">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="763af-1600">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="763af-1601">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="763af-1601">Az.KeyVault</span></span>
- <span data-ttu-id="763af-1602">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="763af-1602">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="763af-1603">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="763af-1603">Az.MachineLearning</span></span>
- <span data-ttu-id="763af-1604">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="763af-1604">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="763af-1605">Az.Media</span><span class="sxs-lookup"><span data-stu-id="763af-1605">Az.Media</span></span>
- <span data-ttu-id="763af-1606">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="763af-1606">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="763af-1607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-1607">Az.Network</span></span>
<span data-ttu-id="763af-1608">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="763af-1608">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="763af-1609">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="763af-1609">New cmdlets added:</span></span>
        - <span data-ttu-id="763af-1610">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="763af-1610">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="763af-1611">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="763af-1611">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="763af-1612">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="763af-1612">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="763af-1613">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="763af-1613">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="763af-1614">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="763af-1614">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="763af-1615">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="763af-1615">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="763af-1616">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="763af-1616">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="763af-1617">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="763af-1617">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="763af-1618">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="763af-1618">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="763af-1619">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="763af-1619">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="763af-1620">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="763af-1620">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="763af-1621">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="763af-1621">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="763af-1622">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="763af-1622">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="763af-1623">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="763af-1623">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="763af-1624">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="763af-1624">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="763af-1625">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="763af-1625">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="763af-1626">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="763af-1626">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="763af-1627">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="763af-1627">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="763af-1628">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="763af-1628">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="763af-1629">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="763af-1629">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="763af-1630">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="763af-1630">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="763af-1631">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="763af-1631">Az.OperationalInsights</span></span>
- <span data-ttu-id="763af-1632">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="763af-1632">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="763af-1633">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="763af-1633">Az.Profile</span></span>
- <span data-ttu-id="763af-1634">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="763af-1634">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="763af-1635">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="763af-1635">Az.RecoveryServices</span></span>
- <span data-ttu-id="763af-1636">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="763af-1636">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="763af-1637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-1637">Az.Resources</span></span>
- <span data-ttu-id="763af-1638">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="763af-1638">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="763af-1639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="763af-1639">Az.ServiceFabric</span></span>
- <span data-ttu-id="763af-1640">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="763af-1640">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="763af-1641">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="763af-1641">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="763af-1642">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="763af-1642">Az.SIgnalR</span></span>
- <span data-ttu-id="763af-1643">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="763af-1643">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="763af-1644">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-1644">Az.Sql</span></span>
- <span data-ttu-id="763af-1645">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="763af-1645">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="763af-1646">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="763af-1646">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="763af-1647">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="763af-1647">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="763af-1648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-1648">Az.Storage</span></span>
- <span data-ttu-id="763af-1649">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="763af-1649">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="763af-1650">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="763af-1650">Az.Websites</span></span>
- <span data-ttu-id="763af-1651">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="763af-1651">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="763af-1652">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="763af-1652">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="763af-1653">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="763af-1653">General</span></span>

* <span data-ttu-id="763af-1654">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="763af-1654">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="763af-1655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-1655">Az.Compute</span></span>

* <span data-ttu-id="763af-1656">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="763af-1656">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="763af-1657">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="763af-1657">Az.DataLakeStore</span></span>

* <span data-ttu-id="763af-1658">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="763af-1658">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="763af-1659">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="763af-1659">Az.FrontDoor</span></span>

* <span data-ttu-id="763af-1660">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="763af-1660">Fixed some broken links</span></span>
    - <span data-ttu-id="763af-1661">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="763af-1661">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="763af-1662">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="763af-1662">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="763af-1663">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="763af-1663">Az.RecoveryServices</span></span>

* <span data-ttu-id="763af-1664">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="763af-1664">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="763af-1665">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="763af-1665">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="763af-1666">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-1666">Az.Resources</span></span>

* <span data-ttu-id="763af-1667">https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="763af-1667">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="763af-1668">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="763af-1668">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="763af-1669">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-1669">Az.Sql</span></span>

* <span data-ttu-id="763af-1670">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="763af-1670">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="763af-1671">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="763af-1671">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="763af-1672">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="763af-1672">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="763af-1673">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-1673">Az.Storage</span></span>

* <span data-ttu-id="763af-1674">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-1674">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="763af-1675">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="763af-1675">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="763af-1676">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="763af-1676">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="763af-1677">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="763af-1677">Support Static Website configuration</span></span>
    - <span data-ttu-id="763af-1678">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="763af-1678">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="763af-1679">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="763af-1679">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="763af-1680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="763af-1680">Az.Websites</span></span>

* <span data-ttu-id="763af-1681">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="763af-1681">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="763af-1682">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="763af-1682">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="763af-1683">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="763af-1683">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="763af-1684">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="763af-1684">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="763af-1685">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="763af-1685">Az.ApiManagement</span></span>
* <span data-ttu-id="763af-1686">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="763af-1686">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="763af-1687">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="763af-1687">Az.Automation</span></span>
* <span data-ttu-id="763af-1688">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="763af-1688">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="763af-1689">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="763af-1689">Added Update Management cmdlets</span></span>
* <span data-ttu-id="763af-1690">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="763af-1690">Added Source Control cmdlets</span></span>
* <span data-ttu-id="763af-1691">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="763af-1691">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="763af-1692">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="763af-1692">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="763af-1693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-1693">Az.Compute</span></span>
* <span data-ttu-id="763af-1694">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="763af-1694">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="763af-1695">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="763af-1695">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="763af-1696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="763af-1696">Az.ContainerInstance</span></span>
* <span data-ttu-id="763af-1697">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="763af-1697">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="763af-1698">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="763af-1698">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="763af-1699">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="763af-1699">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="763af-1700">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-1700">Az.Network</span></span>
* <span data-ttu-id="763af-1701">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="763af-1701">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="763af-1702">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="763af-1702">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="763af-1703">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="763af-1703">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="763af-1704">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="763af-1704">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="763af-1705">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="763af-1705">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="763af-1706">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="763af-1706">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="763af-1707">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="763af-1707">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="763af-1708">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="763af-1708">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="763af-1709">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="763af-1709">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="763af-1710">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="763af-1710">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="763af-1711">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="763af-1711">Az.Relay</span></span>
* <span data-ttu-id="763af-1712">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="763af-1712">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="763af-1713">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-1713">Az.Resources</span></span>
* <span data-ttu-id="763af-1714">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="763af-1714">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="763af-1715">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="763af-1715">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="763af-1716">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="763af-1716">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="763af-1717">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="763af-1717">Az.ServiceFabric</span></span>
* <span data-ttu-id="763af-1718">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="763af-1718">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="763af-1719">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-1719">Az.Sql</span></span>
* <span data-ttu-id="763af-1720">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="763af-1720">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="763af-1721">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="763af-1721">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="763af-1722">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="763af-1722">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="763af-1723">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="763af-1723">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="763af-1724">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="763af-1724">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="763af-1725">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="763af-1725">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="763af-1726">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="763af-1726">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="763af-1727">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="763af-1727">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="763af-1728">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="763af-1728">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="763af-1729">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="763af-1729">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="763af-1730">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="763af-1730">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="763af-1731">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="763af-1731">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="763af-1732">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="763af-1732">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="763af-1733">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="763af-1733">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="763af-1734">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="763af-1734">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="763af-1735">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="763af-1735">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="763af-1736">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="763af-1736">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="763af-1737">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="763af-1737">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="763af-1738">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="763af-1738">General</span></span>
* <span data-ttu-id="763af-1739">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="763af-1739">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="763af-1740">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="763af-1740">Az.Profile</span></span>
* <span data-ttu-id="763af-1741">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="763af-1741">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="763af-1742">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="763af-1742">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="763af-1743">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="763af-1743">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="763af-1744">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="763af-1744">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="763af-1745">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="763af-1745">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="763af-1746">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="763af-1746">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="763af-1747">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="763af-1747">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="763af-1748">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="763af-1748">Az.CognitiveServices</span></span>
* <span data-ttu-id="763af-1749">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="763af-1749">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-1750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-1750">Az.Compute</span></span>
* <span data-ttu-id="763af-1751">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="763af-1751">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="763af-1752">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="763af-1752">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="763af-1753">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="763af-1753">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="763af-1754">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="763af-1754">Az.DataLakeStore</span></span>
* <span data-ttu-id="763af-1755">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="763af-1755">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="763af-1756">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="763af-1756">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="763af-1757">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="763af-1757">Az.Insights</span></span>
* <span data-ttu-id="763af-1758">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="763af-1758">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="763af-1759">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="763af-1759">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="763af-1760">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="763af-1760">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="763af-1761">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="763af-1761">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-1762">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-1762">Az.Network</span></span>
* <span data-ttu-id="763af-1763">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="763af-1763">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="763af-1764">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="763af-1764">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="763af-1765">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="763af-1765">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="763af-1766">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="763af-1766">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="763af-1767">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="763af-1767">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="763af-1768">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="763af-1768">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="763af-1769">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="763af-1769">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="763af-1770">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="763af-1770">Az.PolicyInsights</span></span>
* <span data-ttu-id="763af-1771">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-1771">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-1772">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-1772">Az.Resources</span></span>
* <span data-ttu-id="763af-1773">https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="763af-1773">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="763af-1774">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="763af-1774">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="763af-1775">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="763af-1775">Az.ServiceBus</span></span>
* <span data-ttu-id="763af-1776">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="763af-1776">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="763af-1777">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="763af-1777">Az.ServiceFabric</span></span>
* <span data-ttu-id="763af-1778">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="763af-1778">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="763af-1779">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="763af-1779">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="763af-1780">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="763af-1780">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="763af-1781">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="763af-1781">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="763af-1782">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="763af-1782">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="763af-1783">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="763af-1783">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="763af-1784">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="763af-1784">Az.Profile</span></span>
* <span data-ttu-id="763af-1785">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="763af-1785">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="763af-1786">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="763af-1786">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-1787">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-1787">Az.Compute</span></span>
* <span data-ttu-id="763af-1788">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="763af-1788">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="763af-1789">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="763af-1789">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="763af-1790">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="763af-1790">Az.DataLakeStore</span></span>
* <span data-ttu-id="763af-1791">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="763af-1791">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="763af-1792">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="763af-1792">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="763af-1793">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="763af-1793">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="763af-1794">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="763af-1794">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="763af-1795">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="763af-1795">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-1796">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-1796">Az.Network</span></span>
* <span data-ttu-id="763af-1797">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="763af-1797">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="763af-1798">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="763af-1798">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-1799">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-1799">Az.Resources</span></span>
* <span data-ttu-id="763af-1800">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="763af-1800">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="763af-1801">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="763af-1801">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="763af-1802">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="763af-1802">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="763af-1803">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="763af-1803">Azure.Storage</span></span>
* <span data-ttu-id="763af-1804">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="763af-1804">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="763af-1805">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="763af-1805">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="763af-1806">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="763af-1806">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="763af-1807">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="763af-1807">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="763af-1808">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="763af-1808">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="763af-1809">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="763af-1809">Az.CognitiveServices</span></span>
* <span data-ttu-id="763af-1810">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="763af-1810">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="763af-1811">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="763af-1811">Az.Compute</span></span>
* <span data-ttu-id="763af-1812">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="763af-1812">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="763af-1813">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="763af-1813">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="763af-1814">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="763af-1814">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="763af-1815">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="763af-1815">Az.DataFactoryV2</span></span>
* <span data-ttu-id="763af-1816">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="763af-1816">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="763af-1817">Az.Network</span><span class="sxs-lookup"><span data-stu-id="763af-1817">Az.Network</span></span>
* <span data-ttu-id="763af-1818">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="763af-1818">Added NetworkProfile functionality.</span></span> <span data-ttu-id="763af-1819">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="763af-1819">new cmdlets added</span></span>
    - <span data-ttu-id="763af-1820">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="763af-1820">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="763af-1821">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="763af-1821">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="763af-1822">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="763af-1822">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="763af-1823">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="763af-1823">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="763af-1824">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="763af-1824">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="763af-1825">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="763af-1825">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="763af-1826">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="763af-1826">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="763af-1827">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="763af-1827">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="763af-1828">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="763af-1828">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="763af-1829">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="763af-1829">Az.RedisCache</span></span>
* <span data-ttu-id="763af-1830">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="763af-1830">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="763af-1831">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="763af-1831">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="763af-1832">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="763af-1832">Az.Resources</span></span>
* <span data-ttu-id="763af-1833">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="763af-1833">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="763af-1834">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="763af-1834">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="763af-1835">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="763af-1835">Az.Sql</span></span>
* <span data-ttu-id="763af-1836">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="763af-1836">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="763af-1837">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="763af-1837">Az.Websites</span></span>
* <span data-ttu-id="763af-1838">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="763af-1838">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="763af-1839">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="763af-1839">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="763af-1840">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="763af-1840">0.2.0 - September 2018</span></span>
 <span data-ttu-id="763af-1841">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="763af-1841">Initial Release</span></span>
