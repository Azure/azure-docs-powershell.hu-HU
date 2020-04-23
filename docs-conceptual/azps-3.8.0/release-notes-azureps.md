---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: bee24af99da4b36e89cff9852c77214e2e09a542
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740541"
---
## <a name="380---april-2020"></a><span data-ttu-id="dd3dc-103">3.8.0 – 2020. április</span><span class="sxs-lookup"><span data-stu-id="dd3dc-103">3.8.0 - April 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-104">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-105">Frissítve lett az Azure PowerShell-felmérés URL-címe a következő helyen: Resolve-AzError [#11507]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-105">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dd3dc-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd3dc-106">Az.ApiManagement</span></span>
* <span data-ttu-id="dd3dc-107">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó értesítés az Azure File parancsmagok kimenetére vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-107">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="dd3dc-108">Set-AzApiManagementGroup – Frissítve lett a dokumentáció a GroupId paraméter meghatározása érdekében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-108">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dd3dc-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dd3dc-109">Az.Cdn</span></span>
* <span data-ttu-id="dd3dc-110">Ki lett javítva a díjszabási termékváltozat megjelenítése a ChinaCDN kapcsán</span><span class="sxs-lookup"><span data-stu-id="dd3dc-110">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dd3dc-111">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-111">Az.CognitiveServices</span></span>
* <span data-ttu-id="dd3dc-112">Támogatott identitás, Titkosítás, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-112">Supported Identity, Encryption, UserOwnedStorage</span></span> 

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-113">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-114">Hozzá lett adva a Set-AzVmssOrchestrationServiceState parancsmag.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-114">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="dd3dc-115">A Get-AzVmss az InstanceView használatával az OrchestrationService állapotait mutatja.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-115">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd3dc-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-116">Az.IotHub</span></span>
* <span data-ttu-id="dd3dc-117">Az IoT-ikereszköz konfigurációjának kezelése, Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-117">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="dd3dc-118">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="dd3dc-118">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="dd3dc-119">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="dd3dc-119">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="dd3dc-120">Hozzá lett adva egy parancsmag a közvetlen metódusok az IoT Hubban lévő eszközökön való meghívásához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-120">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="dd3dc-121">Az IoT-ikereszköz modulja konfigurációjának kezelése, Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-121">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="dd3dc-122">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="dd3dc-122">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="dd3dc-123">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="dd3dc-123">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="dd3dc-124">Nagy méretekben történő automatikus IoT-eszközfelügyelet konfigurációjának kezelése.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-124">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="dd3dc-125">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-125">New cmdlets are:</span></span>
    - <span data-ttu-id="dd3dc-126">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd3dc-126">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="dd3dc-127">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd3dc-127">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="dd3dc-128">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd3dc-128">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="dd3dc-129">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd3dc-129">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="dd3dc-130">Hozzá lett adva egy parancsmag az Edge-modul metódusok az IoT Hubban való meghívásához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-130">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dd3dc-131">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd3dc-131">Az.KeyVault</span></span>
* <span data-ttu-id="dd3dc-132">Hozzá lett adva egy új Update-AzKeyVault parancsmag a helyreállító törlés és végleges törlés elleni védelem tárolón való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-132">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="dd3dc-133">Támogatás a következőhöz: Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-133">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="dd3dc-134">Ki lettek javítva a Remove-AzKeyVaultManagedStorageSasDefinition [#11479] példáinak hibái</span><span class="sxs-lookup"><span data-stu-id="dd3dc-134">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="dd3dc-135">Támogatás a privát végponthoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-135">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="dd3dc-136">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="dd3dc-136">Az.Maintenance</span></span>
* <span data-ttu-id="dd3dc-137">Karbantartási parancsmagok végleges verziójának közzététele az általánosan elérhető kiadás számára</span><span class="sxs-lookup"><span data-stu-id="dd3dc-137">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd3dc-138">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-138">Az.Monitor</span></span>
* <span data-ttu-id="dd3dc-139">Parancsmagok hozzáadva a privát kapcsolat hatóköréhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-139">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="dd3dc-140">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="dd3dc-140">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="dd3dc-141">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="dd3dc-141">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="dd3dc-142">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="dd3dc-142">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="dd3dc-143">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="dd3dc-143">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="dd3dc-144">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="dd3dc-144">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="dd3dc-145">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="dd3dc-145">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="dd3dc-146">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="dd3dc-146">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-147">Az.Network</span></span>
* <span data-ttu-id="dd3dc-148">Frissítve lettek a parancsmagok a virtuális hálózati átjáróhoz való csatlakozás engedélyezéséhez magánhálózati IP-cím esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-148">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="dd3dc-149">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dd3dc-149">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="dd3dc-150">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dd3dc-150">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="dd3dc-151">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-151">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="dd3dc-152">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-152">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="dd3dc-153">Frissítve lettek a parancsmagok az FQDN-alapú LocalNetworkGateways és VpnSites engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-153">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="dd3dc-154">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="dd3dc-154">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="dd3dc-155">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="dd3dc-155">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="dd3dc-156">Az IPv6-címcsalád támogatása a következőben: ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="dd3dc-156">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="dd3dc-157">Hozzá lett adva a Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-157">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="dd3dc-158">lehetővé teszi az összes meglévő tulajdonság beállítását, beleértve a következőt is: IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="dd3dc-158">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="dd3dc-159">Frissítve lett az Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-159">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="dd3dc-160">Hozzá lett adva egy másik opcionális AddressPrefixType paraméter a címelőtag címcsaládjának meghatározásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-160">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="dd3dc-161">Frissítve lettek a parancsmagok a DPD-időtúllépés beállításának engedélyezéséhez a virtuális hálózati átjáró kapcsolatain.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-161">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="dd3dc-162">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-162">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="dd3dc-163">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-163">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dd3dc-164">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-164">Az.PolicyInsights</span></span>
* <span data-ttu-id="dd3dc-165">Hozzá lett adva a Start-AzPolicyComplianceScan parancsmag a szabályzatok megfelelőségi vizsgálatának elindításához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-165">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="dd3dc-166">Szabályzatdefiníció, készletdefiníció és hozzárendelési verziók hozzáadva a Get-AzPolicyState kimenetéhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-166">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dd3dc-167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd3dc-167">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd3dc-168">Tovább lett fejlesztve a kódok formázása és a használhatóság a New-AzServiceFabricCluster példái esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-168">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-169">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-170">Hozzá lettek adva a Get-AzSqlInstanceOperation és a Stop-AzSqlInstanceOperation parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-170">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="dd3dc-171">Naplózás támogatása egy VNet-ben található tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-171">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-172">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-173">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó értesítés az Azure File parancsmagok kimenetére vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-173">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="dd3dc-174">Támogatott új SkuName StandardGZRS, StandardRAGZRS a Storage-fiók létrehozása/frissítése során</span><span class="sxs-lookup"><span data-stu-id="dd3dc-174">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="dd3dc-175">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3dc-175">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="dd3dc-176">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3dc-176">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="dd3dc-177">Támogatott Data Lake Gen2</span><span class="sxs-lookup"><span data-stu-id="dd3dc-177">Supported DataLake Gen2</span></span> 
    - <span data-ttu-id="dd3dc-178">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="dd3dc-178">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="dd3dc-179">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="dd3dc-179">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="dd3dc-180">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="dd3dc-180">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="dd3dc-181">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="dd3dc-181">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="dd3dc-182">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="dd3dc-182">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="dd3dc-183">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="dd3dc-183">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="dd3dc-184">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="dd3dc-184">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="dd3dc-185">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="dd3dc-185">'Remove-AzDataLakeGen2Item'</span></span>

# <a name="azure-powershell-release-notes"></a><span data-ttu-id="dd3dc-186">Az Azure PowerShell kibocsátási megjegyzései</span><span class="sxs-lookup"><span data-stu-id="dd3dc-186">Azure PowerShell release notes</span></span>
## <a name="370---march-2020"></a><span data-ttu-id="dd3dc-187">3.7.0 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="dd3dc-187">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-188">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-189">Ki lett javítva az a hiba, hogy a Get-AzTenant/Get-AzDefault/Set-AzDefault parancs NullReferenceException hibát ad vissza kijelentkezett állapotban [#10292]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-189">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-190">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-190">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-191">A következő paraméterek lettek hozzáadva a New-AzDiskConfig parancsmaghoz:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-191">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="dd3dc-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="dd3dc-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="dd3dc-193">Engedélyezve lett a New-AzGalleryImageVersion parancsmag célparaméterének titkosítási tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-193">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="dd3dc-194">Ki lett javítva a tempDisk hibája a Set-AzVmss -Reimage és az Invoke-AzVMReimage parancsmag esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-194">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="dd3dc-195">[#11354]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-195">[#11354]</span></span>
* <span data-ttu-id="dd3dc-196">Az alábbi parancsmagok mostantól támogatottak az új SAP-bővítmény esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-196">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="dd3dc-197">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="dd3dc-197">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="dd3dc-198">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="dd3dc-198">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="dd3dc-199">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="dd3dc-199">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="dd3dc-200">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="dd3dc-200">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="dd3dc-201">Ki lettek javítva a súgódokumentáció példáinak hibái</span><span class="sxs-lookup"><span data-stu-id="dd3dc-201">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="dd3dc-202">Táblázatos formátumban jelenítette meg a sztring pontos értékét a PowerState virtuális gép esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-202">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="dd3dc-203">New-AzVmssConfig: ki lett javítva az AutomaticRepairs tulajdonság szerializálása a SinglePlacementGroup letiltott állapota esetén.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-203">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="dd3dc-204">[#11257]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-204">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd3dc-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd3dc-205">Az.DataFactory</span></span>
* <span data-ttu-id="dd3dc-206">Az ADF .Net SDK a 4.8.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="dd3dc-206">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="dd3dc-207">Opcionális paraméterek lettek hozzáadva az Invoke-AzDataFactoryV2Pipeline parancshoz az újrafuttatás támogatásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-207">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd3dc-208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd3dc-208">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd3dc-209">Hozzá lett adva a kompatibilitástörő változás leírása az Export-AzDataLakeStoreItem és az Import-AzDataLakeStoreItem parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-209">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="dd3dc-210">A bájtkódolási lehetőség hozzá lett adva a New-AzDataLakeStoreItem, az Add-AzDAtaLakeStoreItemContent és a Get-AzDAtaLakeStoreItemContent parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-210">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dd3dc-211">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dd3dc-211">Az.HDInsight</span></span>
* <span data-ttu-id="dd3dc-212">Fürt létrehozásakor a minimálisan támogatott TLS-verzió megadása támogatott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-212">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd3dc-213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-213">Az.IotHub</span></span>
* <span data-ttu-id="dd3dc-214">Hozzá lett adva az elosztott beállítások eszközönkénti felügyeletének támogatása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-214">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="dd3dc-215">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-215">New Cmdlets are:</span></span>
    - <span data-ttu-id="dd3dc-216">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="dd3dc-216">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="dd3dc-217">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="dd3dc-217">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dd3dc-218">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd3dc-218">Az.KeyVault</span></span>
* <span data-ttu-id="dd3dc-219">Kompatibilitástörő változást okozó attribútumok lettek hozzáadva a New-AzKeyVault parancshoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-219">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd3dc-220">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-220">Az.Monitor</span></span>
* <span data-ttu-id="dd3dc-221">Frissült a New-AzScheduledQueryRuleLogMetricTrigger dokumentációja</span><span class="sxs-lookup"><span data-stu-id="dd3dc-221">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-222">Az.Network</span></span>
* <span data-ttu-id="dd3dc-223">Frissültek a parancsmagok a több-bérlős VirtualHubVnetConnections engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-223">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="dd3dc-224">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-224">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="dd3dc-225">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-225">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="dd3dc-226">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-226">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="dd3dc-227">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-227">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="dd3dc-228">Az SQL Management SDK-függőség el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-228">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dd3dc-229">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-229">Az.PolicyInsights</span></span>
* <span data-ttu-id="dd3dc-230">Továbbfejlesztett hibaüzenetek</span><span class="sxs-lookup"><span data-stu-id="dd3dc-230">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-231">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-231">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-232">Hozzá lett adva az Azure Site Recovery-támogatás az Azure Diskkel titkosított virtuális gépek védelmének újbóli beállítása és frissített virtuálisgép-tulajdonságai esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-232">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="dd3dc-233">Hozzá lett adva az Azure Site Recovery VmwareToAzure tulajdonságainak vészhelyreállítási monitorozása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-233">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="dd3dc-234">Hozzá lett adva az Azure Backup-támogatás a sikertelen elemekre vonatkozó szabályzatfrissítés újbóli végrehajtása esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-234">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="dd3dc-235">Hozzá lett adva az Azure Backup-támogatás a lemezkizárási beállításokhoz a biztonsági mentés és a visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-235">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="dd3dc-236">Hozzá lett adva az Azure Backup-támogatás több fájl/mappa visszaállításához az AzureFileShare-ben</span><span class="sxs-lookup"><span data-stu-id="dd3dc-236">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="dd3dc-237">Hozzá lett adva az Azure Backup-támogatás a felhasználó által megadott erőforráscsoport támogatásához az IaasVM-szabályzat frissítésekor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-237">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-238">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-238">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-239">Ki lett javítva a Get-AzResource-ResourceGroupName-Name-ExpandProperties-ResourceType parancs, hogy ezentúl az erőforrások aktuális API-verzióját használja az alapértelmezett verzió helyett [#11267]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-239">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="dd3dc-240">Hozzá lett adva a CorrelationId-naplózás a hibaforgatókönyvek esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-240">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="dd3dc-241">A Get-AzResourceLock dokumentációjában kisebb módosítás történt.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-241">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="dd3dc-242">Példa hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-242">Added example.</span></span>
* <span data-ttu-id="dd3dc-243">A szimpla idézőjel fel lett oldva a Get-AzADUser paraméterértékében [#11317]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-243">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="dd3dc-244">Új parancsmagok lettek hozzáadva az üzembehelyezési szkriptekhez (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript)</span><span class="sxs-lookup"><span data-stu-id="dd3dc-244">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-245">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-246">Olvasható másodlagos paraméter lett hozzáadva az Invoke-AzSqlDatabaseFailover parancshoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-246">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="dd3dc-247">A Disable-AzSqlServerActiveDirectoryOnlyAuthentication parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-247">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="dd3dc-248">Az érzékenységi besorolás mentése megtörténik az adatbázis oszlopainak osztályozásakor.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-248">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="dd3dc-249">Az.Support</span><span class="sxs-lookup"><span data-stu-id="dd3dc-249">Az.Support</span></span>
* <span data-ttu-id="dd3dc-250">Az Az.Support modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-250">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-251">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-252">Mostantól támogatott a webalkalmazások forgalom-útválasztási szabályainak az alábbi új parancsmagokkal történő használata</span><span class="sxs-lookup"><span data-stu-id="dd3dc-252">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="dd3dc-253">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="dd3dc-253">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="dd3dc-254">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="dd3dc-254">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="dd3dc-255">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="dd3dc-255">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="dd3dc-256">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="dd3dc-256">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="dd3dc-257">3.6.1 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="dd3dc-257">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-258">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-259">Azure PowerShell felmérési oldal megnyitása itt: Send-Feedback [#11020]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-259">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="dd3dc-260">Azure PowerShell-felmérés URL-címének megjelenítése itt: Resolve-Error [#11021]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-260">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="dd3dc-261">Az-verzió hozzáadva az UserAgenthez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-261">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dd3dc-262">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd3dc-262">Az.ApiManagement</span></span>
* <span data-ttu-id="dd3dc-263">Mostantól támogatott az egyéni tartomány lekérése és konfigurálása a DeveloperPortal végpontján [#11007]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-263">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="dd3dc-264">Export-AzApiManagementAPi – Mostantól támogatott az Api-definíció Json formátumban való letöltése [#9987]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-264">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="dd3dc-265">Import-AzApiManagementApi – Az OpenAPI 3.0-definíció Json-dokumentumokból való importálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-265">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="dd3dc-266">New-AzApiManagementIdentityProvider és Set-AzApiManagementIdentityProvider – A Signin Tenant konfigurálása az AAD B2C-szolgáltató esetében mostantól támogatott. [#9784]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-266">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd3dc-267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd3dc-267">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd3dc-268">A System.Buffershez hivatkozásának explicit hozzáadása a következőkben: csproj és psd1</span><span class="sxs-lookup"><span data-stu-id="dd3dc-268">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd3dc-269">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-269">Az.IotHub</span></span>
* <span data-ttu-id="dd3dc-270">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-270">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="dd3dc-271">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-271">New Cmdlets are:</span></span>
    - <span data-ttu-id="dd3dc-272">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="dd3dc-272">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="dd3dc-273">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="dd3dc-273">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="dd3dc-274">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="dd3dc-274">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="dd3dc-275">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="dd3dc-275">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="dd3dc-276">A cél IoT-eszközökön lévő modulok IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-276">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="dd3dc-277">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-277">New Cmdlets are:</span></span>
    - <span data-ttu-id="dd3dc-278">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="dd3dc-278">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="dd3dc-279">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="dd3dc-279">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="dd3dc-280">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="dd3dc-280">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="dd3dc-281">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="dd3dc-281">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="dd3dc-282">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-282">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="dd3dc-283">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz modulja kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-283">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="dd3dc-284">Az IoT-eszközök szülő eszközének lekérése/beállítása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-284">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="dd3dc-285">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-285">New Cmdlets are:</span></span>
    - <span data-ttu-id="dd3dc-286">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="dd3dc-286">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="dd3dc-287">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="dd3dc-287">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="dd3dc-288">Az eszközök szülő-gyermek kapcsolatainak kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-288">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd3dc-289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-289">Az.Monitor</span></span>
* <span data-ttu-id="dd3dc-290">A Get-AzMetricDefinition kimeneti értéke javítva [#9714]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-290">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-291">Az.Network</span></span>
* <span data-ttu-id="dd3dc-292">SQL Management SDK frissítve.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-292">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="dd3dc-293">Kijavítottuk a PrivateLinkServiceConnectionState osztály eltérő elnevezéssel kapcsolatos hibáját.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-293">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="dd3dc-294">Az ActionsRequired mező leképezése a követezőre: ActionRequired</span><span class="sxs-lookup"><span data-stu-id="dd3dc-294">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="dd3dc-295">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="dd3dc-295">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-296">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-296">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-297">A Get-AzRoleAssignment null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-297">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="dd3dc-298">A -Force és a -PassThru kapcsoló nem kötelezőként lett megjelölve a Remove-AzADGroup esetében [#10849]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-298">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="dd3dc-299">Javítva a hiba, amely miatt a MailNickname nem lett visszaadva Remove-AzADGroup esetében [#11167]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-299">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="dd3dc-300">A Remove-AzADGroup folyamatművelet működési hibája kijavítva [#11171]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-300">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="dd3dc-301">A GetAzureRoleAssignmentCommand null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-301">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="dd3dc-302">Kompatibilitástörő változás hozzáadva a szabályzati parancsmagok soron következő változásaihoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-302">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="dd3dc-303">Frissült a Get-AzResourceGroup az erőforráscsoport-címke kiszolgálóoldali szűrésének elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-303">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="dd3dc-304">A címkeparancsmagok kiterjesztése a -ResourceID elfogadása érdekében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-304">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="dd3dc-305">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd3dc-305">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="dd3dc-306">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd3dc-306">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="dd3dc-307">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd3dc-307">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="dd3dc-308">Új címkeparancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-308">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="dd3dc-309">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd3dc-309">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="dd3dc-310">A ScopedDeployment áthozva az SDK 3.3.0-ból</span><span class="sxs-lookup"><span data-stu-id="dd3dc-310">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-311">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-311">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-312">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="dd3dc-312">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="dd3dc-313">Támogatás hozzáadva a biztonsági másolatok hosszú távú megőrzési konfigurációjához a felügyelt adatbázisok esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-313">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="dd3dc-314">LTR-szabályzat lekérése/beállítása felügyelt adatbázison</span><span class="sxs-lookup"><span data-stu-id="dd3dc-314">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="dd3dc-315">LTR biztonsági másolat(ok) lekérése felügyelt adatbázis, felügyelt példány vagy hely szerint</span><span class="sxs-lookup"><span data-stu-id="dd3dc-315">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="dd3dc-316">LTR biztonsági másolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-316">Remove an LTR backup</span></span>
    - <span data-ttu-id="dd3dc-317">LTR biztonsági másolat visszaállítása új felügyelt adatbázis létrehozásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-317">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="dd3dc-318">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="dd3dc-318">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="dd3dc-319">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlInstance és Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dd3dc-319">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="dd3dc-320">Az SQL SDK-verzió felléptetése a következőhöz: AZ.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-320">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-321">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-321">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-322">Támogatott AllowProtectedAppendWrite a következőben: ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="dd3dc-322">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="dd3dc-323">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="dd3dc-323">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="dd3dc-324">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet az AzureStorageTable típusának módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-324">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="dd3dc-325">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="dd3dc-325">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="dd3dc-326">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="dd3dc-326">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-327">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-327">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-328">Címke paraméter hozzáadva a következőkhöz: New-AzAppServicePlan és Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="dd3dc-328">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="dd3dc-329">A parancsmag végrehajtásának leállítása, ha egy egyéni tartomány webhelyhez történő hozzáadásakor a rendszer kivételt ad vissza</span><span class="sxs-lookup"><span data-stu-id="dd3dc-329">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="dd3dc-330">Támogatás hozzáadva az olyan App Services műveletek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag</span><span class="sxs-lookup"><span data-stu-id="dd3dc-330">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="dd3dc-331">Hozzáférési korlátozás alkalmazva a különböző erőforráscsoportokban lévő webalkalmazásokra/függvényekre</span><span class="sxs-lookup"><span data-stu-id="dd3dc-331">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="dd3dc-332">Az egyéni WebAppSlots-gazdanevek beállítására vonatkozó hiba kijavítva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-332">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="dd3dc-333">3.5.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="dd3dc-333">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dd3dc-334">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-334">Highlights since the last major release</span></span>
* <span data-ttu-id="dd3dc-335">Frissült az ügyféloldali telemetria.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-335">Updated client side telemetry.</span></span>
* <span data-ttu-id="dd3dc-336">Az.IotHub: parancsmagok hozzáadva az eszközkezelés támogatásához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-336">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="dd3dc-337">Az.SqlVirtualMachine: parancsmagok hozzáadva a rendelkezésreállási csoport figyelőjéhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-337">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-338">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-338">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-339">A SubscriptionId, a TenantId és a végrehajtási idő hozzáadva az ügyféloldali telemetria adataihoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-339">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd3dc-340">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd3dc-340">Az.Automation</span></span>
* <span data-ttu-id="dd3dc-341">Ki lett javítva a „New-AzAutomationSoftwareUpdateConfiguration” referenciadokumentációjának 1. példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="dd3dc-341">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dd3dc-342">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-342">Az.CognitiveServices</span></span>
* <span data-ttu-id="dd3dc-343">Az SDK a 7.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="dd3dc-343">Updated SDK to 7.0</span></span>
* <span data-ttu-id="dd3dc-344">Tovább lett fejlesztve a hibaüzenet, amely akkor jelenik meg, ha a kiszolgáló üres törzset ad vissza válaszként</span><span class="sxs-lookup"><span data-stu-id="dd3dc-344">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-345">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-346">A ProximityPlacementGroupId mostantól üres értékkel is rendelkezhet a frissítés során</span><span class="sxs-lookup"><span data-stu-id="dd3dc-346">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dd3dc-347">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-347">Az.FrontDoor</span></span>
* <span data-ttu-id="dd3dc-348">Új parancsmag hozzáadva a WAF-ban használható felügyelt szabálydefiníciók lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-348">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd3dc-349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-349">Az.IotHub</span></span>
* <span data-ttu-id="dd3dc-350">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-350">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="dd3dc-351">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-351">New Cmdlets are:</span></span>
    - <span data-ttu-id="dd3dc-352">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="dd3dc-352">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="dd3dc-353">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="dd3dc-353">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="dd3dc-354">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="dd3dc-354">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="dd3dc-355">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="dd3dc-355">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dd3dc-356">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd3dc-356">Az.KeyVault</span></span>
* <span data-ttu-id="dd3dc-357">Ki lett javítva az Add-AzKeyVaultKey.md duplikált szövege</span><span class="sxs-lookup"><span data-stu-id="dd3dc-357">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd3dc-358">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-358">Az.Monitor</span></span>
* <span data-ttu-id="dd3dc-359">Ki lett javítva a Get-AzLog parancsmag leírása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-359">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="dd3dc-360">Egy új, ActionGroupId nevű paraméter lett hozzáadva a „New-AzMetricAlertRuleV2” parancshoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-360">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="dd3dc-361">A felhasználó a következőket adhatja meg: ActionGroupId(string) vagy ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-361">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-362">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-362">Az.Network</span></span>
* <span data-ttu-id="dd3dc-363">Hozzá lett adva egy extra paramétermegjegyzés a „New-AzPrivateLinkService” parancsmag „-EnableProxyProtocol” paraméteréhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-363">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="dd3dc-364">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-364">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="dd3dc-365">Hozzá lett adva egy csomagrögzítési példa a Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és Start-AzVirtualnetworkGatewayPacketCapture.md minden belső és külső csomagjának rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-365">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="dd3dc-366">Az Azure Firewall-szabályzat mostantól támogatott a Vnet-tűzfalakon</span><span class="sxs-lookup"><span data-stu-id="dd3dc-366">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="dd3dc-367">Nem lettek hozzáadva új parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-367">No new cmdlets are added.</span></span> <span data-ttu-id="dd3dc-368">Enyhítve lettek a tűzfalszabályzat korlátozásai a Vnet-tűzfalak esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-368">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-370">A fájlokként történő visszaállítás mostantól támogatott az SQL-adatbázisok esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-370">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-371">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-371">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-372">Újra lettek tervezve a sablonalapú üzembehelyezési parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-372">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="dd3dc-373">Új parancsmagok lettek hozzáadva a felügyeleti csoportban való üzembe helyezés kezeléséhez: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dd3dc-373">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="dd3dc-374">Új parancsmagok lettek hozzáadva a bérlői hatókörben való üzembe helyezés kezeléséhez: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="dd3dc-374">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="dd3dc-375">Az \*-AzDeployment parancsmagok kifejezetten az előfizetési hatókörben való működéshez lettek újratervezve</span><span class="sxs-lookup"><span data-stu-id="dd3dc-375">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="dd3dc-376">Az \*-AzSubscriptionDeployment aliasok lettek létrehozva az \*-AzDeployment parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-376">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="dd3dc-377">Ki lett javítva az „Update-AzADApplication” nem beállított „AvailableToOtherTenants” paraméter esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-377">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="dd3dc-378">Az ApplicationObjectWithoutCredentialParameterSet el lett távolítva az AmbiguousParameterSetException elkerülése érdekében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-378">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="dd3dc-379">A súgófájlok újra létre lettek hozva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-379">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-380">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-380">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-381">Az előfizetések közötti időponthoz kötött visszaállítás mostantól támogatott a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-381">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="dd3dc-382">A már meglévő felügyelt SQL-példány hardvergenerációjának módosítása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="dd3dc-382">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="dd3dc-383">Ki lettek javítva az „Update-AzSqlServerVulnerabilityAssessmentSetting” súgópéldái: paraméter/tulajdonságkimenet – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="dd3dc-383">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="dd3dc-384">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dd3dc-384">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="dd3dc-385">Parancsmagokat hozzáadva a rendelkezésreállási csoport figyelőjéhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-385">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="dd3dc-386">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="dd3dc-386">Az.StorageSync</span></span>
* <span data-ttu-id="dd3dc-387">Frissültek az „Invoke-AzStorageSyncCompatibilityCheck” támogatott karakterkészletei.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-387">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="dd3dc-388">3.4.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="dd3dc-388">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dd3dc-389">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-389">Highlights since the last major release</span></span>
* <span data-ttu-id="dd3dc-390">Megjelent az Az.CosmosDB 0.1.0-s kezdeti verziója</span><span class="sxs-lookup"><span data-stu-id="dd3dc-390">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="dd3dc-391">Az.Network ConnectionMonitor V2 támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-391">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-392">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-392">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-393">A környezet automatikus mentésének letiltása, ha az AzureRmContext.json nem érhető el</span><span class="sxs-lookup"><span data-stu-id="dd3dc-393">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="dd3dc-394">Az Azure Powershell Common referenciájának frissítése 1.3.5-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="dd3dc-394">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dd3dc-395">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd3dc-395">Az.ApiManagement</span></span>
* <span data-ttu-id="dd3dc-396">**Get-AzApiManagementApiSchema** Az API-val társított Open-API séma kijavítása   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="dd3dc-396">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="dd3dc-397">**New-AzApiManagementProduct**\* és **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="dd3dc-397">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="dd3dc-398">https://github.com/Azure/azure-powershell/issues/10472 dokumentációja kijavítva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-398">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="dd3dc-399">**Set-AzApiManagementApi** A ServiceUrl parancsmaggal való frissítését bemutató példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-399">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-400">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-401">A virtuális gép állapotának korlátozása 100 értékre, hogy ne legyen szabályozás, ha a Get-AzVM -Status a virtuális gép neve nélkül lett végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-401">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="dd3dc-402">Update-AzDiskEncryptionSet parancsmagok hozzáadása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-402">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="dd3dc-403">Az EncryptionType és a DiskEncryptionSetId paraméterek hozzáadása a következő parancsmagokhoz:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-403">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="dd3dc-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="dd3dc-405">A ColocationStatus paraméter hozzáadva a Get-AzProximityPlacementGroup parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-405">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd3dc-406">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd3dc-406">Az.DataFactory</span></span>
* <span data-ttu-id="dd3dc-407">Az ADF .Net SDK frissítve lett a 4.7.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="dd3dc-407">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="dd3dc-408">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="dd3dc-408">Az.DeploymentManager</span></span>
* <span data-ttu-id="dd3dc-409">LIST műveletek hozzáadása az erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-409">Adds LIST operations for resources</span></span>
* <span data-ttu-id="dd3dc-410">Műveletek végrehajtásának lehetősége az állapotellenőrzés lépésein</span><span class="sxs-lookup"><span data-stu-id="dd3dc-410">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dd3dc-411">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dd3dc-411">Az.HDInsight</span></span>
* <span data-ttu-id="dd3dc-412">A New-AzHDInsightCluster dokumentációs hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-412">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dd3dc-413">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd3dc-413">Az.KeyVault</span></span>
* <span data-ttu-id="dd3dc-414">Name alias hozzáadása a VaultName attribútumhoz, hogy a Remove-AzureKeyVault konzisztens legyen a New-AzureKeyVault paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-414">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-415">Az.Network</span></span>
* <span data-ttu-id="dd3dc-416">Új példa hozzáadva a Set-AzNetworkWatcherConfigFlowLog.md fájlhoz a Traffic Analytics-letiltási forgatókönyv szemléltetésére.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-416">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="dd3dc-417">Felügyeleti IP-konfiguráció támogatás hozzáadva az Azure Firewallhoz – egy dedikált alhálózat és nyilvános IP-cím, amelyet a tűzfal a forgalom felügyeléséhez használni fog</span><span class="sxs-lookup"><span data-stu-id="dd3dc-417">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="dd3dc-418">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-418">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="dd3dc-419">Hozzá lett adva a (nem kötelező) -PublicIpAddress-ManagementPublicIpAddress paraméter, amely egy nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="dd3dc-419">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="dd3dc-420">Hozzá lett adva a SetManagementIpConfiguration metódus a tűzfalobjektumok esetében – nyilvános IP-cím-objektumokat fogad el bemeneti adatként – az alhálózat nevének AzureFirewallManagementSubnet értéknek kell lennie</span><span class="sxs-lookup"><span data-stu-id="dd3dc-420">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="dd3dc-421">A Get-AzNetworkSecurityGroup példái javítva, hogy hálózati biztonsági csoportok példáit tartalmazzák hálózati adapterek helyett.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-421">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="dd3dc-422">Javítottunk egy elírást a New-AzVpnSite parancsban, amely megakadályozta, hogy az erőforrásazonosító-kiegészítő kiegészítsen egy paramétert.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-422">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="dd3dc-423">Az Application Gateway szabály-újraírási műveletkészletének URL-konfigurálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-423">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="dd3dc-424">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-424">New cmdlets added:</span></span>
        - <span data-ttu-id="dd3dc-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd3dc-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="dd3dc-426">A parancsmagok frissültek a nem kötelező UrlConfiguration paraméterrel</span><span class="sxs-lookup"><span data-stu-id="dd3dc-426">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="dd3dc-427">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="dd3dc-427">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="dd3dc-428">A Network Watcher Connection Monitor 2-es verziójú erőforrások támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-428">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dd3dc-429">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-429">Az.PolicyInsights</span></span>
* <span data-ttu-id="dd3dc-430">A javítandó erőforrások azonosítása előtti megfelelőségértékelés támogatása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-430">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="dd3dc-431">-ResourceDiscoverMode paraméter hozzáadása a Start-AzPolicyRemediation parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-431">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="dd3dc-432">A szabályzatok metaadat-erőforrásainak elérésére szolgáló Get-AzPolicyMetadata parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-432">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="dd3dc-433">A Get-AzPolicyState és a Get-AzPolicyStateSummary frissült a 2019-10-01 API-verzióhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-433">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-434">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-434">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-435">Azure Site Recovery-támogatás a replikált lemezek eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-435">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="dd3dc-436">Hozzáadott Azure Backup-támogatás a helyreállítási tárak létrehozása közbeni címkehozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-436">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-437">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-438">A -Scope választható a \*-AzPolicyAssignment parancsmagokban; az alapértelmezett érték a környezeti előfizetés</span><span class="sxs-lookup"><span data-stu-id="dd3dc-438">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="dd3dc-439">Az ADServicePrincipal jelszó és kulcs típusú hitelesítő adatokkal való létrehozását szemléltető példák hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-439">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-440">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-440">Az.Sql</span></span>
<span data-ttu-id="dd3dc-441">A New-AzSqlDatabaseSecondary parancsmag javítva, hogy a PartnerDatabaseName létezését ellenőrizze a DatabaseName létezése helyett.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-441">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-442">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-442">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-443">A Table/Queue Encryption Keytype készlet beállításának támogatása Storage-fiók létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-443">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="dd3dc-444">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3dc-444">New-AzStorageAccount</span></span>
* <span data-ttu-id="dd3dc-445">RequestId megjelenítése, ha a StorageException nem rendelkezik ExtendedErrorInformation paraméterrel</span><span class="sxs-lookup"><span data-stu-id="dd3dc-445">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="dd3dc-446">A Start-AzStorageBlobCopy parancsmag 6. példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-446">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-447">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-447">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-448">A Set-AzWebapp és a Set-AzWebappSlot támogatja az AlwaysOn, a MinTls és a FtpsState tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="dd3dc-448">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="dd3dc-449">Javítva a hiba, amely miatt a HttpsOnly és az AppservicePlan Set-AzWebApp paranccsal történő egyidejű módosításakor a HttpsOnly paraméter alaphelyzetbe állt.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-449">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="dd3dc-450">3.3.0 – 2020. január</span><span class="sxs-lookup"><span data-stu-id="dd3dc-450">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-451">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-451">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-452">Frissítve lettek az Add-AzEnvironment és Set-AzEnvironment parancsmagok, amelyek mostantól elfogadják az AzureAttestationServiceEndpointResourceId és AzureAttestationServiceEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="dd3dc-452">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dd3dc-453">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dd3dc-453">Az.Cdn</span></span>
* <span data-ttu-id="dd3dc-454">A hibaválasz részleteinek láthatóvá tétele a New-AzCdnEndpoint parancsmagban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-454">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-455">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-456">Javítva lett a Set-AzVMCustomScriptExtension parancsmag az olyan virtuális gépek esetében, amelyek felügyelt operációsrendszer-lemeze nem rendelkezik operációsrendszer-profillal.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-456">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="dd3dc-457">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dd3dc-457">Az.ContainerInstance</span></span>
* <span data-ttu-id="dd3dc-458">Javítva lettek a New-AzContainerGroup parancsmagpélda által használt paraméternevek</span><span class="sxs-lookup"><span data-stu-id="dd3dc-458">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="dd3dc-459">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="dd3dc-459">Az.DataBoxEdge</span></span>
* <span data-ttu-id="dd3dc-460">Hozzá lett adva a Get-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="dd3dc-460">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="dd3dc-461">Az Edge Storage-tároló lekérése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-461">Get the Edge Storage Container</span></span>
* <span data-ttu-id="dd3dc-462">Hozzá lett adva a New-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="dd3dc-462">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="dd3dc-463">Új Edge Storage-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-463">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="dd3dc-464">Hozzá lett adva a Remove-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="dd3dc-464">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="dd3dc-465">Az Edge Storage-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-465">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="dd3dc-466">Hozzá lett adva az Invoke-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="dd3dc-466">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="dd3dc-467">Meghívási művelet az Edge Storage-tárolóban lévő adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-467">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="dd3dc-468">Hozzá lett adva a Get-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="dd3dc-468">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="dd3dc-469">Az Edge Storage-fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-469">Get the Edge Storage Account</span></span>
* <span data-ttu-id="dd3dc-470">Hozzá lett adva a New-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="dd3dc-470">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="dd3dc-471">Új Edge Storage-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-471">Create new Edge Storage Account</span></span>
* <span data-ttu-id="dd3dc-472">Hozzá lett adva a Remove-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="dd3dc-472">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="dd3dc-473">Az Edge Storage-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-473">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="dd3dc-474">Hozzá lett adva az Invoke-AzDataBoxEdgeShare parancsmag</span><span class="sxs-lookup"><span data-stu-id="dd3dc-474">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="dd3dc-475">Meghívási művelet a megosztott adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-475">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="dd3dc-476">Hozzá lett adva a Set-AzDataBoxEdgeStorageAccountCredential parancsmag</span><span class="sxs-lookup"><span data-stu-id="dd3dc-476">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="dd3dc-477">Az Az.DataBoxEdge tárfiók hitelesítő adatainak beállítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-477">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd3dc-478">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd3dc-478">Az.DataFactory</span></span>
* <span data-ttu-id="dd3dc-479">Hozzá lettek adva az AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId és VersionStatus tulajdonságok a Get-AzDataFactoryV2IntegrationRuntime parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-479">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="dd3dc-480">Az ADF .Net SDK frissítve lett a 4.6.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="dd3dc-480">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="dd3dc-481">A PublicIPs paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz statikus nyilvános IP-címekkel rendelkező Azure-SSIS IR létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-481">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="dd3dc-482">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="dd3dc-482">Az.DevTestLabs</span></span>
* <span data-ttu-id="dd3dc-483">A hibás hivatkozás el lett távolítva a Get-AzDtlAllowedVMSizesPolicy.md parancsmagból</span><span class="sxs-lookup"><span data-stu-id="dd3dc-483">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dd3dc-484">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-484">Az.EventHub</span></span>
* <span data-ttu-id="dd3dc-485">A 10634-es hiba javítása: Ki lett javítva a nullértékű objektumhivatkozás a remove eventhubnamespace esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-485">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dd3dc-486">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dd3dc-486">Az.HDInsight</span></span>
* <span data-ttu-id="dd3dc-487">Ki lett javítva az Invoke-AzHDInsightHiveJob.md hibája.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-487">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="dd3dc-488">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="dd3dc-488">Az.MachineLearning</span></span>
* <span data-ttu-id="dd3dc-489">El lettek távolítva az alábbi parancsmagok, mivel a MachineLearningCompute már nem érhető el</span><span class="sxs-lookup"><span data-stu-id="dd3dc-489">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="dd3dc-490">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="dd3dc-490">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="dd3dc-491">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="dd3dc-491">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="dd3dc-492">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="dd3dc-492">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="dd3dc-493">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="dd3dc-493">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="dd3dc-494">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="dd3dc-494">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="dd3dc-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="dd3dc-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="dd3dc-496">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="dd3dc-496">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-497">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-497">Az.Network</span></span>
* <span data-ttu-id="dd3dc-498">Frissítve lett a Microsoft.Azure.Management.Sql függősége: 1.36-preview helyett 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="dd3dc-498">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-499">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-499">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-500">Módosított Azure Site Recovery-támogatás azon felügyelt lemezeken található, inaktív állapotban titkosított virtuális gépeknél, amelyekhez felhasználó által kezelt kulcsok tartoznak a következő esetében: Azure – Azure-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-500">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="dd3dc-501">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a védelem engedélyezése során a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-501">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="dd3dc-502">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a lemez szintjén a védelem engedélyezéséhez a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-502">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="dd3dc-503">Azure Site Recovery-támogatás a Replikációval védett, lemeztitkosítási csoportleképezéssel ellátott elemek frissítéséhez a következő esetében: HyperV – Azure.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-503">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-504">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-505">Javítva lett egy hiba a Remove-AzTag súgódokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-505">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-506">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-507">Javítva lett a sebezhetőségi felmérés csoportszintű alapkonfigurációs parancsmagjainak működése: az Azure-adatbázis főadatbázisában használható, a felügyelt példányok rendszeradatbázisaiban korlátozott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-507">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="dd3dc-508">Ki lett javítva egy hiba az SQL-példányok feladatátvételi csoportjainak létrehozása esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-508">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="dd3dc-509">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dd3dc-509">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="dd3dc-510">Hozzá lett adva a DR, mint új érvényes licenctípus</span><span class="sxs-lookup"><span data-stu-id="dd3dc-510">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-511">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-512">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet a DefaultAction értékének módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-512">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="dd3dc-513">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd3dc-513">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="dd3dc-514">Támogatott a tárfiók legutóbbi szinkronizálási időpontjának lekérése a get-AzureRMStorageAccount parancsmag -IncludeGeoReplicationStats paraméterrel való futtatásával</span><span class="sxs-lookup"><span data-stu-id="dd3dc-514">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="dd3dc-515">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3dc-515">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="dd3dc-516">3.2.0 – 2019. december</span><span class="sxs-lookup"><span data-stu-id="dd3dc-516">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="dd3dc-517">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="dd3dc-517">General</span></span>
* <span data-ttu-id="dd3dc-518">A .psd1 hivatkozásai frissítve, hogy minden modulhoz a relatív elérési utat használják</span><span class="sxs-lookup"><span data-stu-id="dd3dc-518">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-519">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-519">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-520">A megfelelő felhasználói ügynök beállítva az ügyféloldali telemetriához az Az 4.0 előzetes verziójában</span><span class="sxs-lookup"><span data-stu-id="dd3dc-520">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="dd3dc-521">Felhasználóbarát hibaüzenet megjelenítése, ha az Az 4.0 előzetes verziójában a környezet null értékű</span><span class="sxs-lookup"><span data-stu-id="dd3dc-521">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dd3dc-522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dd3dc-522">Az.Batch</span></span>
* <span data-ttu-id="dd3dc-523">Ki lett javítva a [10602-es](https://github.com/Azure/azure-powershell/issues/10602) számú hiba, amely miatt a **New-AzBatchPool** nem megfelelően küldte el a „VirtualMachineConfiguration.ContainerConfiguration” és a „VirtualMachineConfiguration.DataDisks” paramétereket a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-523">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd3dc-524">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd3dc-524">Az.DataFactory</span></span>
* <span data-ttu-id="dd3dc-525">Az ADF .Net SDK a 4.5.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="dd3dc-525">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dd3dc-526">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-526">Az.FrontDoor</span></span>
* <span data-ttu-id="dd3dc-527">A WAF felügyeleti szabályok kizárása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="dd3dc-527">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="dd3dc-528">Hozzá lett adva a SocketAddr automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-528">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="dd3dc-529">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="dd3dc-529">Az.HealthcareApis</span></span>
* <span data-ttu-id="dd3dc-530">Kivételkezelés</span><span class="sxs-lookup"><span data-stu-id="dd3dc-530">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dd3dc-531">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd3dc-531">Az.KeyVault</span></span>
* <span data-ttu-id="dd3dc-532">Ki lett javítva az esetleg nem beállított értékek hozzáférésével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="dd3dc-532">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="dd3dc-533">Az elliptikus görbéjű titkosítási tanúsítványok kezelése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-533">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="dd3dc-534">A görbe tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-534">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd3dc-535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-535">Az.Monitor</span></span>
* <span data-ttu-id="dd3dc-536">Opcionális argumentum hozzáadva a Diagnosztikai beállítások hozzáadása parancshoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-536">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="dd3dc-537">Ez egy kapcsoló argumentum, amely megléte esetén azt jelzi, hogy a Log Analyticsbe történő exportálást egy rögzített séma (más néven</span><span class="sxs-lookup"><span data-stu-id="dd3dc-537">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="dd3dc-538">dedikált adattípus) szerint kell végrehajtani</span><span class="sxs-lookup"><span data-stu-id="dd3dc-538">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-539">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-539">Az.Network</span></span>
* <span data-ttu-id="dd3dc-540">Támogatás az Ip-csoportok számára az AzureFirewall alkalmazás, valamint a Nat- és a hálózati szabályok esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-540">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-541">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-541">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-542">Ki lett javítva az a hiba, amely miatt a sablonalapú üzembe helyezés során a sablonparamétert nem lehet olvasni, ha a sablonparaméter és egy beépített paraméter neve között névütközés áll fenn.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-542">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="dd3dc-543">Frissültek a szabályzat parancsmagjai a 2019. 09. 01. dátumú új API-verzió használatára, amely bevezeti a szabályzatkészlet-definíciókon belüli csoportos támogatást.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-543">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-544">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-544">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-545">Frissítve lett a sebezhetőségi felmérés automatikus engedélyezéséhez szükséges tárterület létrehozása a Storagev2-ben</span><span class="sxs-lookup"><span data-stu-id="dd3dc-545">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-546">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-546">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-547">A blob-/tárolóidentitás-alapú SAS-token Oauth-hitelesítésen alapuló Storage-környezettel való létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-547">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="dd3dc-548">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="dd3dc-548">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="dd3dc-549">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="dd3dc-549">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="dd3dc-550">Támogatott lett a tárfiókhoz tartozó felhasználódelegálási kulcsok visszavonása, így minden identitásalapú SAS-token visszavonható</span><span class="sxs-lookup"><span data-stu-id="dd3dc-550">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="dd3dc-551">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="dd3dc-551">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="dd3dc-552">Frissítés a Microsoft.Azure.Management.Storage 14.2.0-s verziójára az új API-verzió (2019. 06. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-552">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="dd3dc-553">A QuotaGiB (gigabájtban megadott megosztási kvóta) esetében támogatottak az 5120-nál nagyobb értékek a fájlmegosztási parancsmagok felügyeleti síkján, és hozzá lett adva a Quota paraméteralias a QuotaGiB paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-553">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="dd3dc-554">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dd3dc-554">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="dd3dc-555">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dd3dc-555">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="dd3dc-556">A „QuotaGiB” paraméteralias hozzáadva a „kvóta” paraméterhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-556">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="dd3dc-557">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="dd3dc-557">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="dd3dc-558">Ki lett javítva az a hiba, amely miatt a Set-AzStorageContainerAcl parancsmag el tudta távolítani a tárolt hozzáférési szabályzatot</span><span class="sxs-lookup"><span data-stu-id="dd3dc-558">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="dd3dc-559">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="dd3dc-559">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="dd3dc-560">3.1.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="dd3dc-560">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dd3dc-561">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-561">Highlights since the last major release</span></span>
* <span data-ttu-id="dd3dc-562">Az.DataBoxEdge 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-562">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="dd3dc-563">Az.SqlVirtualMachine 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-563">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-564">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-564">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-565">A virtuális gépek Reapply funkciója</span><span class="sxs-lookup"><span data-stu-id="dd3dc-565">VM Reapply feature</span></span>
    - <span data-ttu-id="dd3dc-566">A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-566">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="dd3dc-567">A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-567">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="dd3dc-568">Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dd3dc-568">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="dd3dc-569">Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-569">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="dd3dc-570">A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-570">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="dd3dc-571">A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-571">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="dd3dc-572">A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező</span><span class="sxs-lookup"><span data-stu-id="dd3dc-572">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="dd3dc-573">A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="dd3dc-573">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="dd3dc-574">A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-574">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="dd3dc-575">A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-575">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="dd3dc-576">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="dd3dc-576">Az.DataBoxEdge</span></span>
* <span data-ttu-id="dd3dc-577">A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-577">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="dd3dc-578">Megrendelés lekérése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-578">Get the Order</span></span>
* <span data-ttu-id="dd3dc-579">A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-579">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="dd3dc-580">Új megrendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-580">Create new Order</span></span>
* <span data-ttu-id="dd3dc-581">A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-581">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="dd3dc-582">Megrendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-582">Remove the Order</span></span>
* <span data-ttu-id="dd3dc-583">`New-AzDataBoxEdgeShare` parancsmag módosítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-583">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="dd3dc-584">Mostantól helyi megosztást hoz létre</span><span class="sxs-lookup"><span data-stu-id="dd3dc-584">Now creates Local Share</span></span>
* <span data-ttu-id="dd3dc-585">A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-585">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="dd3dc-586">Mostantól az IotRole leképezhető a Share-re</span><span class="sxs-lookup"><span data-stu-id="dd3dc-586">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="dd3dc-587">A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-587">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="dd3dc-588">Frissítések keresésének, letöltésének, telepítésének indítása az eszközön</span><span class="sxs-lookup"><span data-stu-id="dd3dc-588">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="dd3dc-589">A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-589">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="dd3dc-590">Triggerek információinak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-590">Gets the information about Triggers</span></span>
* <span data-ttu-id="dd3dc-591">A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-591">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="dd3dc-592">Új triggerek létrehozása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-592">Create new Triggers</span></span>
* <span data-ttu-id="dd3dc-593">A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-593">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="dd3dc-594">Triggerek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-594">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd3dc-595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd3dc-595">Az.DataFactory</span></span>
* <span data-ttu-id="dd3dc-596">Az ADF .Net SDK a 4.4.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="dd3dc-596">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="dd3dc-597">Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-597">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd3dc-598">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd3dc-598">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd3dc-599">Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja</span><span class="sxs-lookup"><span data-stu-id="dd3dc-599">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dd3dc-600">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-600">Az.EventHub</span></span>
* <span data-ttu-id="dd3dc-601">A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-601">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dd3dc-602">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-602">Az.FrontDoor</span></span>
* <span data-ttu-id="dd3dc-603">Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="dd3dc-603">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="dd3dc-604">A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="dd3dc-604">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="dd3dc-605">Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-605">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="dd3dc-606">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="dd3dc-606">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-607">Az.Network</span></span>
* <span data-ttu-id="dd3dc-608">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-608">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="dd3dc-609">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="dd3dc-609">Az.PrivateDns</span></span>
* <span data-ttu-id="dd3dc-610">A PrivateDns .net sdk frissült az 1.0.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="dd3dc-610">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-611">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-611">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-612">Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-612">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="dd3dc-613">Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-613">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="dd3dc-614">SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-614">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="dd3dc-615">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dd3dc-615">Az.RedisCache</span></span>
* <span data-ttu-id="dd3dc-616">A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-616">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="dd3dc-617">Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-617">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="dd3dc-618">Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-618">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-619">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-619">Az.Resources</span></span>
- <span data-ttu-id="dd3dc-620">Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-620">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="dd3dc-621">Frissült a létrehozási szabályzat definíciójának súgóbeli példája</span><span class="sxs-lookup"><span data-stu-id="dd3dc-621">Updated create policy definition help example</span></span>
- <span data-ttu-id="dd3dc-622">Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-622">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="dd3dc-623">Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-623">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="dd3dc-624">A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-624">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-625">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-626">Az adatbázisbeli ReadReplicaCount mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-626">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="dd3dc-627">A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén</span><span class="sxs-lookup"><span data-stu-id="dd3dc-627">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="dd3dc-628">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="dd3dc-628">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="dd3dc-629">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="dd3dc-629">General</span></span>
* <span data-ttu-id="dd3dc-630">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="dd3dc-630">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-631">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-631">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-632">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-632">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="dd3dc-633">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-633">Az.Advisor</span></span>
* <span data-ttu-id="dd3dc-634">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-634">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dd3dc-635">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dd3dc-635">Az.Batch</span></span>
* <span data-ttu-id="dd3dc-636">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-636">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="dd3dc-637">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-637">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="dd3dc-638">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-638">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="dd3dc-639">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-639">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="dd3dc-640">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-640">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="dd3dc-641">Ezek az **New-AzBatchTask**`-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-641">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="dd3dc-642">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-642">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="dd3dc-643">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-643">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="dd3dc-644">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-644">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="dd3dc-645">A `PSApplication`**Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-645">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="dd3dc-646">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-646">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="dd3dc-647">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-647">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="dd3dc-648">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-648">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="dd3dc-649">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-649">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="dd3dc-650">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-650">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="dd3dc-651">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-651">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="dd3dc-652">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-652">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="dd3dc-653">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-653">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="dd3dc-654">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-654">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="dd3dc-655">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-655">This operation is no longer supported.</span></span>
* <span data-ttu-id="dd3dc-656">`PSCloudServiceConfiguration``TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-656">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="dd3dc-657">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-657">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="dd3dc-658">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-658">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="dd3dc-659">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-659">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="dd3dc-660">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-660">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="dd3dc-661">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-661">New non-verified images are also now returned.</span></span> <span data-ttu-id="dd3dc-662">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-662">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="dd3dc-663">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-663">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="dd3dc-664">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-664">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="dd3dc-665">Ez a `PSNetworkSecurityGroupRule``SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-665">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="dd3dc-666">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-666">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="dd3dc-667">Ezt a `PSTaskContainerSettings``WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-667">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="dd3dc-668">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-668">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="dd3dc-669">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-669">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="dd3dc-670">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-670">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="dd3dc-671">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-671">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dd3dc-672">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dd3dc-672">Az.Cdn</span></span>
* <span data-ttu-id="dd3dc-673">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-673">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="dd3dc-674">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-674">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-675">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-676">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="dd3dc-676">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="dd3dc-677">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="dd3dc-677">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="dd3dc-678">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="dd3dc-678">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="dd3dc-679">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-679">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="dd3dc-680">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-680">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="dd3dc-681">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="dd3dc-681">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="dd3dc-682">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-682">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="dd3dc-683">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="dd3dc-683">Breaking changes</span></span>
    - <span data-ttu-id="dd3dc-684">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="dd3dc-684">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="dd3dc-685">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-685">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd3dc-686">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd3dc-686">Az.DataFactory</span></span>
* <span data-ttu-id="dd3dc-687">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="dd3dc-687">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd3dc-688">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd3dc-688">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd3dc-689">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="dd3dc-689">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="dd3dc-690">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-690">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="dd3dc-691">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-691">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="dd3dc-692">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-692">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="dd3dc-693">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-693">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="dd3dc-694">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-694">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dd3dc-695">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-695">Az.FrontDoor</span></span>
* <span data-ttu-id="dd3dc-696">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-696">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dd3dc-697">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dd3dc-697">Az.HDInsight</span></span>
* <span data-ttu-id="dd3dc-698">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-698">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="dd3dc-699">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-699">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="dd3dc-700">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="dd3dc-700">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="dd3dc-701">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-701">Removed five cmdlets:</span></span>
    - <span data-ttu-id="dd3dc-702">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="dd3dc-702">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="dd3dc-703">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="dd3dc-703">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="dd3dc-704">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="dd3dc-704">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="dd3dc-705">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="dd3dc-705">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="dd3dc-706">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="dd3dc-706">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="dd3dc-707">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-707">Added three cmdlets:</span></span>
    - <span data-ttu-id="dd3dc-708">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-708">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="dd3dc-709">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-709">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="dd3dc-710">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-710">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="dd3dc-711">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-711">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="dd3dc-712">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-712">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="dd3dc-713">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-713">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="dd3dc-714">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-714">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="dd3dc-715">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-715">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="dd3dc-716">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-716">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="dd3dc-717">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-717">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="dd3dc-718">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-718">Added some scenario test cases.</span></span>
* <span data-ttu-id="dd3dc-719">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-719">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd3dc-720">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-720">Az.IotHub</span></span>
* <span data-ttu-id="dd3dc-721">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-721">Breaking changes:</span></span>
    - <span data-ttu-id="dd3dc-722">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-722">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="dd3dc-723">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-723">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="dd3dc-724">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-724">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="dd3dc-725">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-725">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="dd3dc-726">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-726">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="dd3dc-727">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-727">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="dd3dc-728">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-728">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="dd3dc-729">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-729">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="dd3dc-730">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-730">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="dd3dc-731">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-731">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="dd3dc-732">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-732">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="dd3dc-733">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-733">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-734">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-734">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-735">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-735">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="dd3dc-736">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-736">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="dd3dc-737">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-737">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="dd3dc-738">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-738">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="dd3dc-739">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-739">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="dd3dc-740">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-740">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="dd3dc-741">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-741">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="dd3dc-742">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-742">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="dd3dc-743">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="dd3dc-743">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-744">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-745">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="dd3dc-745">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-746">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-746">Az.Network</span></span>
* <span data-ttu-id="dd3dc-747">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-747">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="dd3dc-748">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-748">Updated cmdlet:</span></span>
        - <span data-ttu-id="dd3dc-749">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-749">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dd3dc-750">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-750">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dd3dc-751">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-751">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dd3dc-752">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-752">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dd3dc-753">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-753">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="dd3dc-754">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-754">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="dd3dc-755">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-755">New cmdlet:</span></span>
        - <span data-ttu-id="dd3dc-756">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="dd3dc-756">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="dd3dc-757">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-757">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="dd3dc-758">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-758">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="dd3dc-759">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-759">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="dd3dc-760">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-760">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="dd3dc-761">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="dd3dc-761">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="dd3dc-762">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-762">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="dd3dc-763">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-763">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="dd3dc-764">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-764">New cmdlets added:</span></span>
        - <span data-ttu-id="dd3dc-765">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-765">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="dd3dc-766">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd3dc-766">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="dd3dc-767">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd3dc-767">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="dd3dc-768">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd3dc-768">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="dd3dc-769">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-769">Set-AzVirtualHub</span></span>
* <span data-ttu-id="dd3dc-770">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-770">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="dd3dc-771">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-771">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="dd3dc-772">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-772">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="dd3dc-773">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-773">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="dd3dc-774">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-774">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="dd3dc-775">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-775">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="dd3dc-776">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-776">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="dd3dc-777">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-777">New cmdlets added:</span></span>
        - <span data-ttu-id="dd3dc-778">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-778">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="dd3dc-779">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-779">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="dd3dc-780">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-780">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="dd3dc-781">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-781">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="dd3dc-782">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-782">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="dd3dc-783">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-783">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="dd3dc-784">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-784">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="dd3dc-785">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-785">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="dd3dc-786">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-786">New cmdlets added:</span></span>
        - <span data-ttu-id="dd3dc-787">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="dd3dc-787">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="dd3dc-788">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="dd3dc-788">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="dd3dc-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="dd3dc-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="dd3dc-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="dd3dc-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="dd3dc-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="dd3dc-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="dd3dc-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd3dc-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="dd3dc-793">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="dd3dc-794">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-794">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="dd3dc-795">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-795">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="dd3dc-796">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-796">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="dd3dc-797">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-797">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="dd3dc-798">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-798">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="dd3dc-799">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-799">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="dd3dc-800">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-800">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="dd3dc-801">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="dd3dc-801">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="dd3dc-802">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-802">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="dd3dc-803">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-803">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="dd3dc-804">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-804">New cmdlets added:</span></span>
        - <span data-ttu-id="dd3dc-805">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="dd3dc-805">New-AzIpGroup</span></span>
        - <span data-ttu-id="dd3dc-806">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="dd3dc-806">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="dd3dc-807">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="dd3dc-807">Get-AzIpGroup</span></span>
        - <span data-ttu-id="dd3dc-808">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="dd3dc-808">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dd3dc-809">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd3dc-809">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd3dc-810">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-810">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-811">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-811">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-812">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-812">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="dd3dc-813">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-813">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="dd3dc-814">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-814">Removed deprecated aliases:</span></span>
* <span data-ttu-id="dd3dc-815">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="dd3dc-815">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="dd3dc-816">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="dd3dc-816">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="dd3dc-817">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-817">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="dd3dc-818">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-818">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="dd3dc-819">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="dd3dc-819">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="dd3dc-820">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-820">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-821">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-821">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-822">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="dd3dc-822">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="dd3dc-823">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3dc-823">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="dd3dc-824">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3dc-824">Set-AzStorageAccount</span></span>
* <span data-ttu-id="dd3dc-825">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="dd3dc-825">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="dd3dc-826">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="dd3dc-826">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="dd3dc-827">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="dd3dc-827">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="dd3dc-828">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="dd3dc-828">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="dd3dc-829">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="dd3dc-829">General</span></span>
* <span data-ttu-id="dd3dc-830">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="dd3dc-830">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-831">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-832">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-832">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dd3dc-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd3dc-833">Az.ApiManagement</span></span>
* <span data-ttu-id="dd3dc-834">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="dd3dc-834">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="dd3dc-835">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="dd3dc-835">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd3dc-836">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd3dc-836">Az.Automation</span></span>
* <span data-ttu-id="dd3dc-837">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-837">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dd3dc-838">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dd3dc-838">Az.Batch</span></span>
* <span data-ttu-id="dd3dc-839">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-839">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-840">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-840">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-841">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-841">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="dd3dc-842">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-842">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="dd3dc-843">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-843">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="dd3dc-844">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-844">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd3dc-845">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd3dc-845">Az.DataFactory</span></span>
* <span data-ttu-id="dd3dc-846">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-846">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="dd3dc-847">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-847">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="dd3dc-848">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="dd3dc-848">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd3dc-849">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd3dc-849">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd3dc-850">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="dd3dc-850">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="dd3dc-851">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="dd3dc-851">Az.HealthcareApis</span></span>
* <span data-ttu-id="dd3dc-852">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="dd3dc-852">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="dd3dc-853">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="dd3dc-853">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="dd3dc-854">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-854">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="dd3dc-855">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-855">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd3dc-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-856">Az.IotHub</span></span>
* <span data-ttu-id="dd3dc-857">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="dd3dc-857">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="dd3dc-858">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd3dc-858">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd3dc-859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-859">Az.Monitor</span></span>
* <span data-ttu-id="dd3dc-860">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="dd3dc-860">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="dd3dc-861">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-861">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="dd3dc-862">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-862">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="dd3dc-863">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-863">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-864">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-864">Az.Network</span></span>
* <span data-ttu-id="dd3dc-865">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-865">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="dd3dc-866">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-866">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="dd3dc-867">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-867">New cmdlets added:</span></span>
        - <span data-ttu-id="dd3dc-868">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="dd3dc-868">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="dd3dc-869">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-869">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="dd3dc-870">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-870">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="dd3dc-871">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-871">Updated cmdlets:</span></span>
        - <span data-ttu-id="dd3dc-872">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-872">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="dd3dc-873">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-873">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="dd3dc-874">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-874">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="dd3dc-875">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-875">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="dd3dc-876">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="dd3dc-876">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="dd3dc-877">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-877">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="dd3dc-878">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-878">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="dd3dc-879">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dd3dc-879">Az.RedisCache</span></span>
* <span data-ttu-id="dd3dc-880">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-880">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-881">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-881">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-882">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-882">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-883">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-883">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-884">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-884">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="dd3dc-885">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="dd3dc-885">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="dd3dc-886">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="dd3dc-886">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="dd3dc-887">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="dd3dc-887">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="dd3dc-888">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3dc-888">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="dd3dc-889">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="dd3dc-889">Az.StorageSync</span></span>
* <span data-ttu-id="dd3dc-890">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-890">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-891">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-892">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="dd3dc-892">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="dd3dc-893">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="dd3dc-893">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="dd3dc-894">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd3dc-894">Az.ApiManagement</span></span>
* <span data-ttu-id="dd3dc-895">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="dd3dc-895">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="dd3dc-896">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-896">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="dd3dc-897">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-897">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd3dc-898">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd3dc-898">Az.Automation</span></span>
* <span data-ttu-id="dd3dc-899">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="dd3dc-899">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="dd3dc-900">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-900">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="dd3dc-901">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-901">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-902">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-902">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-903">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-903">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="dd3dc-904">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-904">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="dd3dc-905">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-905">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="dd3dc-906">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-906">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="dd3dc-907">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-907">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="dd3dc-908">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-908">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="dd3dc-909">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-909">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="dd3dc-910">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-910">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="dd3dc-911">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-911">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd3dc-912">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd3dc-912">Az.DataFactory</span></span>
* <span data-ttu-id="dd3dc-913">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-913">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="dd3dc-914">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="dd3dc-914">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dd3dc-915">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dd3dc-915">Az.HDInsight</span></span>
* <span data-ttu-id="dd3dc-916">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-916">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd3dc-917">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-917">Az.IotHub</span></span>
* <span data-ttu-id="dd3dc-918">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-918">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="dd3dc-919">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-919">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="dd3dc-920">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-920">New cmdlets are:</span></span>
    - <span data-ttu-id="dd3dc-921">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="dd3dc-921">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="dd3dc-922">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="dd3dc-922">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="dd3dc-923">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="dd3dc-923">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="dd3dc-924">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="dd3dc-924">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd3dc-925">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-925">Az.Monitor</span></span>
* <span data-ttu-id="dd3dc-926">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="dd3dc-926">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="dd3dc-927">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-927">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="dd3dc-928">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-928">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="dd3dc-929">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-929">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="dd3dc-930">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-930">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="dd3dc-931">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-931">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="dd3dc-932">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-932">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="dd3dc-933">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-933">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="dd3dc-934">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-934">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="dd3dc-935">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-935">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="dd3dc-936">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-936">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="dd3dc-937">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-937">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="dd3dc-938">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-938">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="dd3dc-939">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="dd3dc-939">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="dd3dc-940">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="dd3dc-940">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="dd3dc-941">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="dd3dc-941">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="dd3dc-942">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="dd3dc-942">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="dd3dc-943">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-943">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="dd3dc-944">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-944">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="dd3dc-945">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-945">Overall improved help files</span></span>
* <span data-ttu-id="dd3dc-946">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="dd3dc-946">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-947">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-947">Az.Network</span></span>
* <span data-ttu-id="dd3dc-948">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="dd3dc-948">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="dd3dc-949">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="dd3dc-949">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="dd3dc-950">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-950">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="dd3dc-951">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-951">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="dd3dc-952">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-952">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="dd3dc-953">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-953">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="dd3dc-954">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-954">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="dd3dc-955">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-955">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="dd3dc-956">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-956">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="dd3dc-957">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="dd3dc-957">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="dd3dc-958">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-958">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="dd3dc-959">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="dd3dc-959">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="dd3dc-960">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-960">New cmdlets</span></span>
        - <span data-ttu-id="dd3dc-961">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="dd3dc-961">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="dd3dc-962">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-962">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="dd3dc-963">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-963">Updated cmdlet:</span></span>
        - <span data-ttu-id="dd3dc-964">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="dd3dc-964">New-VpnSite</span></span>
        - <span data-ttu-id="dd3dc-965">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="dd3dc-965">Update-VpnSite</span></span>
        - <span data-ttu-id="dd3dc-966">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-966">New-VpnConnection</span></span>
        - <span data-ttu-id="dd3dc-967">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-967">Update-VpnConnection</span></span>
* <span data-ttu-id="dd3dc-968">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="dd3dc-968">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-969">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-969">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-970">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="dd3dc-970">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="dd3dc-971">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-971">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-972">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-973">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-973">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dd3dc-974">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd3dc-974">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd3dc-975">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="dd3dc-975">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="dd3dc-976">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-976">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="dd3dc-977">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dd3dc-977">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dd3dc-978">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="dd3dc-978">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="dd3dc-979">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="dd3dc-979">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="dd3dc-980">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="dd3dc-980">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="dd3dc-981">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dd3dc-981">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dd3dc-982">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dd3dc-982">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dd3dc-983">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="dd3dc-983">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="dd3dc-984">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="dd3dc-984">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="dd3dc-985">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="dd3dc-985">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="dd3dc-986">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dd3dc-986">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dd3dc-987">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="dd3dc-987">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="dd3dc-988">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="dd3dc-988">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="dd3dc-989">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="dd3dc-989">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="dd3dc-990">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-990">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="dd3dc-991">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="dd3dc-991">Az.SignalR</span></span>
* <span data-ttu-id="dd3dc-992">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-992">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-993">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-994">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="dd3dc-994">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="dd3dc-995">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-995">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="dd3dc-996">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-996">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="dd3dc-997">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-997">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="dd3dc-998">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-998">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-999">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-1000">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1000">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="dd3dc-1001">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1001">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="dd3dc-1002">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1002">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="dd3dc-1003">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1003">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="dd3dc-1004">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1004">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="dd3dc-1005">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1005">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="dd3dc-1006">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1006">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="dd3dc-1007">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1007">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="dd3dc-1008">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1008">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="dd3dc-1009">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1009">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="dd3dc-1010">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1010">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-1011">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1011">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-1012">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1012">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="dd3dc-1013">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1013">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="dd3dc-1014">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1014">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="dd3dc-1015">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1015">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="dd3dc-1016">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1016">General</span></span>
* <span data-ttu-id="dd3dc-1017">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1017">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-1018">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1018">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-1019">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1019">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="dd3dc-1020">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1020">Az.Aks</span></span>
* <span data-ttu-id="dd3dc-1021">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1021">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="dd3dc-1022">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1022">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dd3dc-1023">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1023">Az.ApiManagement</span></span>
* <span data-ttu-id="dd3dc-1024">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1024">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="dd3dc-1025">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1025">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="dd3dc-1026">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1026">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="dd3dc-1027">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1027">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="dd3dc-1028">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1028">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dd3dc-1029">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1029">Az.Batch</span></span>
* <span data-ttu-id="dd3dc-1030">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1030">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dd3dc-1031">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1031">Az.Cdn</span></span>
* <span data-ttu-id="dd3dc-1032">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1032">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-1033">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1033">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-1034">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1034">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="dd3dc-1035">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1035">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="dd3dc-1036">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1036">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="dd3dc-1037">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1037">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="dd3dc-1038">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1038">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="dd3dc-1039">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1039">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="dd3dc-1040">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1040">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="dd3dc-1041">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1041">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd3dc-1042">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1042">Az.DataFactory</span></span>
* <span data-ttu-id="dd3dc-1043">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1043">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="dd3dc-1044">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1044">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="dd3dc-1045">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1045">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="dd3dc-1046">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1046">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd3dc-1047">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1047">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd3dc-1048">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1048">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dd3dc-1049">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1049">Az.EventHub</span></span>
* <span data-ttu-id="dd3dc-1050">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1050">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="dd3dc-1051">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1051">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="dd3dc-1052">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1052">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="dd3dc-1053">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1053">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="dd3dc-1054">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1054">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="dd3dc-1055">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1055">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd3dc-1056">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1056">Az.Monitor</span></span>
* <span data-ttu-id="dd3dc-1057">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1057">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-1058">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1058">Az.Network</span></span>
* <span data-ttu-id="dd3dc-1059">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1059">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="dd3dc-1060">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1060">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="dd3dc-1061">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1061">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="dd3dc-1062">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1062">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="dd3dc-1063">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1063">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="dd3dc-1064">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1064">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="dd3dc-1065">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1065">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dd3dc-1066">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1066">Az.OperationalInsights</span></span>
* <span data-ttu-id="dd3dc-1067">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1067">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="dd3dc-1068">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1068">Added example</span></span>
    - <span data-ttu-id="dd3dc-1069">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1069">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="dd3dc-1070">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1070">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="dd3dc-1071">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1071">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-1073">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1073">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1074">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-1075">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1075">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="dd3dc-1076">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1076">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="dd3dc-1077">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1077">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="dd3dc-1078">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1078">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dd3dc-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="dd3dc-1080">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1080">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="dd3dc-1081">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1081">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="dd3dc-1082">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1082">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dd3dc-1083">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1083">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd3dc-1084">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1084">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="dd3dc-1085">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1085">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="dd3dc-1086">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1086">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="dd3dc-1087">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1087">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="dd3dc-1088">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1088">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="dd3dc-1089">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1089">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-1090">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1090">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-1091">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1091">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1092">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-1093">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1093">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="dd3dc-1094">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1094">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="dd3dc-1095">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1095">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="dd3dc-1096">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1096">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="dd3dc-1097">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1097">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="dd3dc-1098">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1098">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-1099">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1099">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-1100">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1100">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="dd3dc-1101">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-1102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1102">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-1103">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="dd3dc-1104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="dd3dc-1105">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd3dc-1106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1106">Az.Automation</span></span>
* <span data-ttu-id="dd3dc-1107">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1107">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dd3dc-1108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1108">Az.CognitiveServices</span></span>
* <span data-ttu-id="dd3dc-1109">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-1110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1110">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-1111">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="dd3dc-1112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="dd3dc-1113">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="dd3dc-1114">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd3dc-1115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1115">Az.DataFactory</span></span>
* <span data-ttu-id="dd3dc-1116">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="dd3dc-1117">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dd3dc-1118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1118">Az.EventHub</span></span>
* <span data-ttu-id="dd3dc-1119">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="dd3dc-1120">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dd3dc-1121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1121">Az.KeyVault</span></span>
* <span data-ttu-id="dd3dc-1122">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dd3dc-1123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1123">Az.LogicApp</span></span>
* <span data-ttu-id="dd3dc-1124">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="dd3dc-1125">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="dd3dc-1126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1126">Az.ManagedServices</span></span>
* <span data-ttu-id="dd3dc-1127">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-1128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1128">Az.Network</span></span>
* <span data-ttu-id="dd3dc-1129">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="dd3dc-1130">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1130">New cmdlets</span></span>
        - <span data-ttu-id="dd3dc-1131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dd3dc-1132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="dd3dc-1133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dd3dc-1134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dd3dc-1135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dd3dc-1136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dd3dc-1137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="dd3dc-1138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="dd3dc-1139">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="dd3dc-1140">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="dd3dc-1141">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="dd3dc-1142">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="dd3dc-1143">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="dd3dc-1144">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="dd3dc-1145">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1145">Updated cmdlets</span></span>
        - <span data-ttu-id="dd3dc-1146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="dd3dc-1147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="dd3dc-1148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="dd3dc-1149">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="dd3dc-1150">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="dd3dc-1151">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1151">Updated cmdlet:</span></span>
        - <span data-ttu-id="dd3dc-1152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="dd3dc-1153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="dd3dc-1154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="dd3dc-1155">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="dd3dc-1156">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="dd3dc-1157">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dd3dc-1158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1158">Az.OperationalInsights</span></span>
* <span data-ttu-id="dd3dc-1159">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1159">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="dd3dc-1160">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1161">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-1162">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="dd3dc-1163">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="dd3dc-1164">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="dd3dc-1165">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="dd3dc-1166">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="dd3dc-1167">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="dd3dc-1168">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="dd3dc-1169">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="dd3dc-1170">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="dd3dc-1171">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1172">Az.Resources</span></span>
- <span data-ttu-id="dd3dc-1173">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="dd3dc-1174">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dd3dc-1175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1175">Az.ServiceBus</span></span>
* <span data-ttu-id="dd3dc-1176">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="dd3dc-1177">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1178">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-1179">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="dd3dc-1180">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="dd3dc-1181">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-1182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1182">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-1183">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="dd3dc-1184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1184">Az.StorageSync</span></span>
* <span data-ttu-id="dd3dc-1185">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="dd3dc-1186">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-1187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1187">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-1188">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="dd3dc-1189">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="dd3dc-1190">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="dd3dc-1191">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-1192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1192">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-1193">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="dd3dc-1194">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="dd3dc-1195">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="dd3dc-1196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1196">Az.Advisor</span></span>
* <span data-ttu-id="dd3dc-1197">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="dd3dc-1198">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dd3dc-1199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1199">Az.ApiManagement</span></span>
* <span data-ttu-id="dd3dc-1200">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="dd3dc-1201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="dd3dc-1202">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="dd3dc-1203">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="dd3dc-1204">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="dd3dc-1205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="dd3dc-1206">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd3dc-1207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1207">Az.Automation</span></span>
* <span data-ttu-id="dd3dc-1208">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1209">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-1210">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd3dc-1211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1211">Az.DataFactory</span></span>
* <span data-ttu-id="dd3dc-1212">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dd3dc-1213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1213">Az.EventGrid</span></span>
* <span data-ttu-id="dd3dc-1214">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd3dc-1215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1215">Az.IotHub</span></span>
* <span data-ttu-id="dd3dc-1216">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1217">Az.Network</span></span>
* <span data-ttu-id="dd3dc-1218">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="dd3dc-1219">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dd3dc-1220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1220">Az.PolicyInsights</span></span>
* <span data-ttu-id="dd3dc-1221">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="dd3dc-1222">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dd3dc-1223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1223">Az.OperationalInsights</span></span>
* <span data-ttu-id="dd3dc-1224">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-1225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1225">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-1226">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-1227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1227">Az.Resources</span></span>
    - <span data-ttu-id="dd3dc-1228">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="dd3dc-1229">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="dd3dc-1230">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="dd3dc-1231">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dd3dc-1232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1232">Az.ServiceBus</span></span>
* <span data-ttu-id="dd3dc-1233">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-1234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1234">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-1235">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="dd3dc-1236">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="dd3dc-1237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="dd3dc-1238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="dd3dc-1239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="dd3dc-1240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="dd3dc-1241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="dd3dc-1242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="dd3dc-1243">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-1244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1244">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-1245">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="dd3dc-1246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="dd3dc-1247">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="dd3dc-1248">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="dd3dc-1249">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="dd3dc-1250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="dd3dc-1251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="dd3dc-1252">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="dd3dc-1253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="dd3dc-1254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="dd3dc-1255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1255">Az.StorageSync</span></span>
* <span data-ttu-id="dd3dc-1256">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="dd3dc-1257">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-1258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1258">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-1259">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="dd3dc-1260">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="dd3dc-1261">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="dd3dc-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="dd3dc-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1264">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-1265">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="dd3dc-1266">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="dd3dc-1267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1267">Az.Dns</span></span>
* <span data-ttu-id="dd3dc-1268">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dd3dc-1269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1269">Az.EventGrid</span></span>
* <span data-ttu-id="dd3dc-1270">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="dd3dc-1271">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1271">New cmdlets:</span></span>
    - <span data-ttu-id="dd3dc-1272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="dd3dc-1273">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="dd3dc-1274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="dd3dc-1275">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="dd3dc-1276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="dd3dc-1277">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="dd3dc-1278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="dd3dc-1279">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="dd3dc-1280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="dd3dc-1281">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="dd3dc-1282">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="dd3dc-1283">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="dd3dc-1284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="dd3dc-1285">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="dd3dc-1286">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="dd3dc-1287">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="dd3dc-1288">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1288">Updated cmdlets:</span></span>
    - <span data-ttu-id="dd3dc-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="dd3dc-1290">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="dd3dc-1291">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="dd3dc-1292">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="dd3dc-1293">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="dd3dc-1294">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="dd3dc-1295">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="dd3dc-1296">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="dd3dc-1297">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="dd3dc-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="dd3dc-1299">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="dd3dc-1300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="dd3dc-1301">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="dd3dc-1302">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dd3dc-1303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1303">Az.FrontDoor</span></span>
* <span data-ttu-id="dd3dc-1304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="dd3dc-1305">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="dd3dc-1306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="dd3dc-1307">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-1308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1308">Az.Network</span></span>
* <span data-ttu-id="dd3dc-1309">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="dd3dc-1310">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1310">New cmdlets</span></span>
        - <span data-ttu-id="dd3dc-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="dd3dc-1312">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="dd3dc-1313">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1313">New cmdlets</span></span>
        - <span data-ttu-id="dd3dc-1314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="dd3dc-1315">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="dd3dc-1316">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1316">New cmdlets</span></span>
        - <span data-ttu-id="dd3dc-1317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1317">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="dd3dc-1318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="dd3dc-1319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="dd3dc-1320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="dd3dc-1321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="dd3dc-1322">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="dd3dc-1323">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1323">New cmdlets</span></span>
        - <span data-ttu-id="dd3dc-1324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dd3dc-1325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dd3dc-1326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dd3dc-1327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="dd3dc-1328">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="dd3dc-1329">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="dd3dc-1330">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="dd3dc-1331">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="dd3dc-1332">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="dd3dc-1333">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="dd3dc-1334">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="dd3dc-1335">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="dd3dc-1336">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="dd3dc-1337">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="dd3dc-1338">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="dd3dc-1339">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="dd3dc-1340">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="dd3dc-1341">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="dd3dc-1342">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="dd3dc-1343">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="dd3dc-1344">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="dd3dc-1345">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="dd3dc-1346">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="dd3dc-1347">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="dd3dc-1348">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="dd3dc-1349">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="dd3dc-1350">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dd3dc-1351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1351">Az.OperationalInsights</span></span>
* <span data-ttu-id="dd3dc-1352">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1353">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-1354">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="dd3dc-1355">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="dd3dc-1356">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="dd3dc-1357">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dd3dc-1358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1358">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd3dc-1359">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-1360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1360">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-1361">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="dd3dc-1362">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="dd3dc-1363">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="dd3dc-1364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="dd3dc-1365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="dd3dc-1366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="dd3dc-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="dd3dc-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-1369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1369">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-1370">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="dd3dc-1371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1371">New-AzStorageAccount</span></span>
* <span data-ttu-id="dd3dc-1372">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="dd3dc-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-1374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1374">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-1375">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="dd3dc-1376">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="dd3dc-1377">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="dd3dc-1378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1378">Az.Cdn</span></span>
* <span data-ttu-id="dd3dc-1379">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1380">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-1381">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="dd3dc-1382">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dd3dc-1383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1383">Az.EventHub</span></span>
* <span data-ttu-id="dd3dc-1384">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="dd3dc-1385">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-1386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1386">Az.Network</span></span>
* <span data-ttu-id="dd3dc-1387">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="dd3dc-1388">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dd3dc-1389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1389">Az.PolicyInsights</span></span>
* <span data-ttu-id="dd3dc-1390">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-1391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1391">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-1392">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dd3dc-1393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1393">Az.ServiceBus</span></span>
* <span data-ttu-id="dd3dc-1394">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dd3dc-1395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1395">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd3dc-1396">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="dd3dc-1397">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1398">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-1399">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="dd3dc-1400">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="dd3dc-1401">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="dd3dc-1402">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-1403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1403">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-1404">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="dd3dc-1405">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="dd3dc-1406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1406">Az.ApiManagement</span></span>
* <span data-ttu-id="dd3dc-1407">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="dd3dc-1408">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="dd3dc-1409">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="dd3dc-1410">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="dd3dc-1411">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="dd3dc-1412">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="dd3dc-1413">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="dd3dc-1414">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="dd3dc-1415">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="dd3dc-1416">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="dd3dc-1417">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="dd3dc-1418">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="dd3dc-1419">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="dd3dc-1420">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="dd3dc-1421">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="dd3dc-1422">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="dd3dc-1423">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="dd3dc-1424">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="dd3dc-1425">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1425">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="dd3dc-1426">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="dd3dc-1427">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="dd3dc-1428">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="dd3dc-1429">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="dd3dc-1430">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="dd3dc-1431">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="dd3dc-1432">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="dd3dc-1433">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="dd3dc-1434">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="dd3dc-1435">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="dd3dc-1436">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="dd3dc-1437">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1437">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="dd3dc-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="dd3dc-1439">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="dd3dc-1440">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="dd3dc-1441">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="dd3dc-1442">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="dd3dc-1443">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="dd3dc-1444">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="dd3dc-1445">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="dd3dc-1446">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1446">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="dd3dc-1447">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="dd3dc-1448">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="dd3dc-1449">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="dd3dc-1450">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="dd3dc-1451">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="dd3dc-1452">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="dd3dc-1453">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1453">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="dd3dc-1454">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="dd3dc-1455">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="dd3dc-1456">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="dd3dc-1457">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="dd3dc-1458">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="dd3dc-1459">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="dd3dc-1460">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="dd3dc-1461">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="dd3dc-1462">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="dd3dc-1463">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="dd3dc-1464">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="dd3dc-1465">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="dd3dc-1466">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="dd3dc-1467">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="dd3dc-1468">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="dd3dc-1469">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="dd3dc-1470">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="dd3dc-1471">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="dd3dc-1472">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="dd3dc-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="dd3dc-1474">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="dd3dc-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="dd3dc-1476">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="dd3dc-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="dd3dc-1478">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="dd3dc-1479">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="dd3dc-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="dd3dc-1481">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1481">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="dd3dc-1482">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="dd3dc-1483">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd3dc-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1484">Az.Automation</span></span>
* <span data-ttu-id="dd3dc-1485">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="dd3dc-1486">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="dd3dc-1487">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="dd3dc-1488">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="dd3dc-1489">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="dd3dc-1490">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="dd3dc-1491">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-1492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1492">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-1493">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="dd3dc-1494">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd3dc-1495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1495">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd3dc-1496">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd3dc-1497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1497">Az.Monitor</span></span>
* <span data-ttu-id="dd3dc-1498">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-1499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1499">Az.Network</span></span>
* <span data-ttu-id="dd3dc-1500">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="dd3dc-1501">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1501">Updated cmdlet:</span></span>
        - <span data-ttu-id="dd3dc-1502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="dd3dc-1503">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-1504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1504">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-1505">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-1506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1506">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-1507">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="dd3dc-1508">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-1509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1509">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-1510">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dd3dc-1511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1511">Az.CognitiveServices</span></span>
* <span data-ttu-id="dd3dc-1512">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="dd3dc-1513">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1514">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-1515">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="dd3dc-1516">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="dd3dc-1517">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="dd3dc-1518">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="dd3dc-1519">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="dd3dc-1520">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="dd3dc-1521">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1521">Breaking changes</span></span>
    - <span data-ttu-id="dd3dc-1522">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="dd3dc-1523">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="dd3dc-1524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1524">Az.DeploymentManager</span></span>
* <span data-ttu-id="dd3dc-1525">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="dd3dc-1526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1526">Az.Dns</span></span>
* <span data-ttu-id="dd3dc-1527">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="dd3dc-1528">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="dd3dc-1529">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dd3dc-1530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1530">Az.FrontDoor</span></span>
* <span data-ttu-id="dd3dc-1531">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="dd3dc-1532">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="dd3dc-1533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1533">Az.HDInsight</span></span>
* <span data-ttu-id="dd3dc-1534">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="dd3dc-1535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="dd3dc-1536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="dd3dc-1537">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="dd3dc-1538">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="dd3dc-1539">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="dd3dc-1540">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd3dc-1541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1541">Az.Monitor</span></span>
* <span data-ttu-id="dd3dc-1542">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="dd3dc-1543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="dd3dc-1544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="dd3dc-1545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="dd3dc-1546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="dd3dc-1547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="dd3dc-1548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="dd3dc-1549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dd3dc-1550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dd3dc-1551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dd3dc-1552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dd3dc-1553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dd3dc-1554">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1554">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="dd3dc-1555">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-1556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1556">Az.Network</span></span>
* <span data-ttu-id="dd3dc-1557">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="dd3dc-1558">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1558">New cmdlets</span></span>
        - <span data-ttu-id="dd3dc-1559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1559">New-AzNatGateway</span></span>
        - <span data-ttu-id="dd3dc-1560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="dd3dc-1561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="dd3dc-1562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="dd3dc-1563">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1563">Updated cmdlets</span></span>
        - <span data-ttu-id="dd3dc-1564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="dd3dc-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="dd3dc-1566">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="dd3dc-1567">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="dd3dc-1568">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dd3dc-1569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1569">Az.PolicyInsights</span></span>
* <span data-ttu-id="dd3dc-1570">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="dd3dc-1571">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="dd3dc-1572">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-1573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1573">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-1574">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="dd3dc-1575">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="dd3dc-1576">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="dd3dc-1577">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="dd3dc-1578">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="dd3dc-1579">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="dd3dc-1580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1580">Az.Relay</span></span>
* <span data-ttu-id="dd3dc-1581">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dd3dc-1582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1582">Az.ServiceBus</span></span>
* <span data-ttu-id="dd3dc-1583">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-1584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1584">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-1585">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="dd3dc-1586">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="dd3dc-1587">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="dd3dc-1588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1588">New-AzStorageAccount</span></span>
* <span data-ttu-id="dd3dc-1589">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="dd3dc-1590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="dd3dc-1591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="dd3dc-1592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-1593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1593">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-1594">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="dd3dc-1595">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="dd3dc-1596">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dd3dc-1597">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1597">Highlights since the last major release</span></span>
* <span data-ttu-id="dd3dc-1598">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1598">General availability of `Az` module</span></span>
* <span data-ttu-id="dd3dc-1599">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="dd3dc-1600">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="dd3dc-1601">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="dd3dc-1602">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dd3dc-1603">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="dd3dc-1604">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-1605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1605">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-1606">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dd3dc-1607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1607">Az.Batch</span></span>
* <span data-ttu-id="dd3dc-1608">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dd3dc-1609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1609">Az.Cdn</span></span>
* <span data-ttu-id="dd3dc-1610">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dd3dc-1611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1611">Az.CognitiveServices</span></span>
* <span data-ttu-id="dd3dc-1612">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-1613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1613">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-1614">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="dd3dc-1615">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dd3dc-1616">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd3dc-1617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1617">Az.DataFactory</span></span>
* <span data-ttu-id="dd3dc-1618">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd3dc-1619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1619">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd3dc-1620">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dd3dc-1621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1621">Az.EventGrid</span></span>
* <span data-ttu-id="dd3dc-1622">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dd3dc-1623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1623">Az.EventHub</span></span>
* <span data-ttu-id="dd3dc-1624">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1624">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dd3dc-1625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1625">Az.HDInsight</span></span>
* <span data-ttu-id="dd3dc-1626">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd3dc-1627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1627">Az.IotHub</span></span>
* <span data-ttu-id="dd3dc-1628">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dd3dc-1629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1629">Az.KeyVault</span></span>
* <span data-ttu-id="dd3dc-1630">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dd3dc-1631">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="dd3dc-1632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1632">Az.MachineLearning</span></span>
* <span data-ttu-id="dd3dc-1633">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="dd3dc-1634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1634">Az.Media</span></span>
* <span data-ttu-id="dd3dc-1635">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd3dc-1636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1636">Az.Monitor</span></span>
  * <span data-ttu-id="dd3dc-1637">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="dd3dc-1638">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="dd3dc-1639">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="dd3dc-1640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="dd3dc-1641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="dd3dc-1642">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="dd3dc-1643">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-1644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1644">Az.Network</span></span>
* <span data-ttu-id="dd3dc-1645">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dd3dc-1646">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="dd3dc-1647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1647">Az.NotificationHubs</span></span>
* <span data-ttu-id="dd3dc-1648">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dd3dc-1649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1649">Az.OperationalInsights</span></span>
* <span data-ttu-id="dd3dc-1650">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="dd3dc-1651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="dd3dc-1652">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-1653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1653">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-1654">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dd3dc-1655">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="dd3dc-1656">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="dd3dc-1657">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="dd3dc-1658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1658">Az.RedisCache</span></span>
* <span data-ttu-id="dd3dc-1659">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1660">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-1661">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-1662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1662">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-1663">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="dd3dc-1664">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dd3dc-1665">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="dd3dc-1666">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="dd3dc-1667">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="dd3dc-1668">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="dd3dc-1669">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-1670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1670">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-1671">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="dd3dc-1672">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dd3dc-1673">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="dd3dc-1674">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="dd3dc-1675">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dd3dc-1676">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1676">Highlights since the last major release</span></span>
* <span data-ttu-id="dd3dc-1677">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1677">General availability of `Az` module</span></span>
* <span data-ttu-id="dd3dc-1678">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="dd3dc-1679">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="dd3dc-1680">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="dd3dc-1681">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dd3dc-1682">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="dd3dc-1683">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-1684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1684">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-1685">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="dd3dc-1686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1686">Az.AnalysisServices</span></span>
* <span data-ttu-id="dd3dc-1687">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="dd3dc-1688">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd3dc-1689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1689">Az.Automation</span></span>
* <span data-ttu-id="dd3dc-1690">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="dd3dc-1691">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="dd3dc-1692">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-1693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1693">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-1694">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="dd3dc-1695">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1695">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="dd3dc-1696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1696">Az.ContainerInstance</span></span>
* <span data-ttu-id="dd3dc-1697">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd3dc-1698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1698">Az.DataFactory</span></span>
* <span data-ttu-id="dd3dc-1699">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="dd3dc-1700">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-1701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1701">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-1702">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="dd3dc-1703">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="dd3dc-1704">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="dd3dc-1705">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="dd3dc-1706">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="dd3dc-1707">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-1708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1708">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-1709">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-1710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1710">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-1711">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="dd3dc-1712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1712">New-AzStorageContext</span></span>
* <span data-ttu-id="dd3dc-1713">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="dd3dc-1714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="dd3dc-1715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="dd3dc-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="dd3dc-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="dd3dc-1718">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="dd3dc-1719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="dd3dc-1720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="dd3dc-1721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="dd3dc-1722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="dd3dc-1723">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dd3dc-1724">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1724">Highlights since the last major release</span></span>
* <span data-ttu-id="dd3dc-1725">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1725">General availability of `Az` module</span></span>
* <span data-ttu-id="dd3dc-1726">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="dd3dc-1727">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="dd3dc-1728">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="dd3dc-1729">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dd3dc-1730">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="dd3dc-1731">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd3dc-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1732">Az.Automation</span></span>
* <span data-ttu-id="dd3dc-1733">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="dd3dc-1734">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1734">Dynamic grouping</span></span>
    * <span data-ttu-id="dd3dc-1735">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1735">Pre-Post script</span></span>
    * <span data-ttu-id="dd3dc-1736">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1737">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-1738">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="dd3dc-1739">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dd3dc-1740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1740">Az.KeyVault</span></span>
* <span data-ttu-id="dd3dc-1741">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-1742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1742">Az.Network</span></span>
* <span data-ttu-id="dd3dc-1743">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="dd3dc-1744">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-1745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1745">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-1746">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="dd3dc-1747">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-1748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1748">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-1749">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="dd3dc-1750">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-1751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1751">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-1752">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-1753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1753">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-1754">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="dd3dc-1755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="dd3dc-1756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="dd3dc-1757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="dd3dc-1758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="dd3dc-1759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="dd3dc-1760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-1761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1761">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-1762">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="dd3dc-1763">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-1764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1764">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-1765">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="dd3dc-1766">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd3dc-1767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1767">Az.Automation</span></span>
* <span data-ttu-id="dd3dc-1768">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="dd3dc-1769">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="dd3dc-1770">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dd3dc-1771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1771">Az.Cdn</span></span>
* <span data-ttu-id="dd3dc-1772">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-1773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1773">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-1774">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd3dc-1775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1775">Az.DataFactory</span></span>
* <span data-ttu-id="dd3dc-1776">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dd3dc-1777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1777">Az.LogicApp</span></span>
* <span data-ttu-id="dd3dc-1778">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-1779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1779">Az.Network</span></span>
* <span data-ttu-id="dd3dc-1780">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-1781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1781">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-1782">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="dd3dc-1783">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1783">SDK Update</span></span>
* <span data-ttu-id="dd3dc-1784">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="dd3dc-1785">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-1786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1786">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-1787">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="dd3dc-1788">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="dd3dc-1789">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="dd3dc-1790">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="dd3dc-1791">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="dd3dc-1792">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-1793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1793">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-1794">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="dd3dc-1795">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-1796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1796">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-1797">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="dd3dc-1798">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="dd3dc-1799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1799">Az.AnalysisServices</span></span>
* <span data-ttu-id="dd3dc-1800">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd3dc-1801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1801">Az.Automation</span></span>
* <span data-ttu-id="dd3dc-1802">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="dd3dc-1803">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="dd3dc-1804">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dd3dc-1805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1805">Az.CognitiveServices</span></span>
* <span data-ttu-id="dd3dc-1806">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-1807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1807">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-1808">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="dd3dc-1809">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="dd3dc-1810">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="dd3dc-1811">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd3dc-1812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1812">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd3dc-1813">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dd3dc-1814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1814">Az.EventHub</span></span>
* <span data-ttu-id="dd3dc-1815">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dd3dc-1816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1816">Az.KeyVault</span></span>
* <span data-ttu-id="dd3dc-1817">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dd3dc-1818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1818">Az.LogicApp</span></span>
* <span data-ttu-id="dd3dc-1819">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="dd3dc-1820">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="dd3dc-1821">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="dd3dc-1822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="dd3dc-1823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="dd3dc-1824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="dd3dc-1825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="dd3dc-1826">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="dd3dc-1827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="dd3dc-1828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="dd3dc-1829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="dd3dc-1830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="dd3dc-1831">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dd3dc-1832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1832">Az.Monitor</span></span>
* <span data-ttu-id="dd3dc-1833">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-1834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1834">Az.Network</span></span>
* <span data-ttu-id="dd3dc-1835">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dd3dc-1836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1836">Az.OperationalInsights</span></span>
* <span data-ttu-id="dd3dc-1837">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="dd3dc-1838">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="dd3dc-1839">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-1840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1840">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-1841">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="dd3dc-1842">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="dd3dc-1843">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="dd3dc-1844">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-1845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1845">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-1846">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="dd3dc-1847">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-1848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1848">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-1849">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="dd3dc-1850">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-1851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1851">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-1852">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="dd3dc-1853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1853">Az.AnalysisServices</span></span>
<span data-ttu-id="dd3dc-1854">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-1855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1855">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-1856">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="dd3dc-1857">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="dd3dc-1858">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-1859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1859">Az.RecoveryServices</span></span>
<span data-ttu-id="dd3dc-1860">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-1861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1861">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-1862">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1862">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="dd3dc-1863">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="dd3dc-1864">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="dd3dc-1865">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-1866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1866">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-1867">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="dd3dc-1868">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="dd3dc-1869">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="dd3dc-1870">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-1871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1871">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-1872">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="dd3dc-1873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1873">Az.AnalysisServices</span></span>
* <span data-ttu-id="dd3dc-1874">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-1875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1875">Az.RecoveryServices</span></span>
* <span data-ttu-id="dd3dc-1876">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="dd3dc-1877">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1878">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-1879">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dd3dc-1880">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dd3dc-1881">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="dd3dc-1882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1882">Az.Aks</span></span>
* <span data-ttu-id="dd3dc-1883">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dd3dc-1884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1884">Az.Automation</span></span>
* <span data-ttu-id="dd3dc-1885">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="dd3dc-1886">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dd3dc-1887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1887">Az.Cdn</span></span>
* <span data-ttu-id="dd3dc-1888">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-1889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1889">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-1890">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="dd3dc-1891">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="dd3dc-1892">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="dd3dc-1893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="dd3dc-1894">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dd3dc-1895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1895">Az.DataFactory</span></span>
* <span data-ttu-id="dd3dc-1896">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd3dc-1897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1897">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd3dc-1898">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="dd3dc-1899">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="dd3dc-1900">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd3dc-1901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1901">Az.IotHub</span></span>
* <span data-ttu-id="dd3dc-1902">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dd3dc-1903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1903">Az.KeyVault</span></span>
* <span data-ttu-id="dd3dc-1904">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-1905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1905">Az.Network</span></span>
* <span data-ttu-id="dd3dc-1906">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-1907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1907">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-1908">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="dd3dc-1909">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="dd3dc-1910">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="dd3dc-1911">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="dd3dc-1912">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="dd3dc-1913">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="dd3dc-1914">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dd3dc-1915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1915">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd3dc-1916">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="dd3dc-1917">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1917">Fix some error messages.</span></span>
* <span data-ttu-id="dd3dc-1918">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="dd3dc-1919">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="dd3dc-1920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1920">Az.SignalR</span></span>
* <span data-ttu-id="dd3dc-1921">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-1922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1922">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-1923">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dd3dc-1924">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="dd3dc-1925">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="dd3dc-1926">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-1927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1927">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-1928">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dd3dc-1929">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="dd3dc-1930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="dd3dc-1931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="dd3dc-1932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1932">Az.TrafficManager</span></span>
* <span data-ttu-id="dd3dc-1933">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-1934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1934">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-1935">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dd3dc-1936">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="dd3dc-1937">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="dd3dc-1938">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dd3dc-1939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1939">Az.Accounts</span></span>
* <span data-ttu-id="dd3dc-1940">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-1941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1941">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-1942">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="dd3dc-1943">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="dd3dc-1944">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd3dc-1945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1945">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd3dc-1946">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="dd3dc-1947">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dd3dc-1948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1948">Az.EventGrid</span></span>
* <span data-ttu-id="dd3dc-1949">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="dd3dc-1950">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="dd3dc-1951">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="dd3dc-1952">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="dd3dc-1953">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="dd3dc-1954">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="dd3dc-1955">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="dd3dc-1956">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="dd3dc-1957">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="dd3dc-1958">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1958">Dead letter endpoint.</span></span>
* <span data-ttu-id="dd3dc-1959">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="dd3dc-1960">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dd3dc-1961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1961">Az.IotHub</span></span>
* <span data-ttu-id="dd3dc-1962">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dd3dc-1963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1963">Az.LogicApp</span></span>
* <span data-ttu-id="dd3dc-1964">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-1965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1965">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-1966">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="dd3dc-1967">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="dd3dc-1968">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="dd3dc-1969">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="dd3dc-1970">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="dd3dc-1971">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="dd3dc-1972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1972">Az.SignalR</span></span>
* <span data-ttu-id="dd3dc-1973">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-1974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1974">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-1975">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dd3dc-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1976">Az.Storage</span></span>
* <span data-ttu-id="dd3dc-1977">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="dd3dc-1978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1978">New-AzStorageContext</span></span>
* <span data-ttu-id="dd3dc-1979">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="dd3dc-1980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1981">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-1982">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="dd3dc-1983">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="dd3dc-1984">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="dd3dc-1985">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1985">General</span></span>

- <span data-ttu-id="dd3dc-1986">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1986">General Availability of Az Module</span></span>
- <span data-ttu-id="dd3dc-1987">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1987">Online help for each module</span></span>
- <span data-ttu-id="dd3dc-1988">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="dd3dc-1989">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="dd3dc-1990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1990">Az.Accounts</span></span>
- <span data-ttu-id="dd3dc-1991">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1991">Changed from Az.Profile</span></span>
- <span data-ttu-id="dd3dc-1992">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="dd3dc-1993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1993">Az.ApiManagement</span></span>
- <span data-ttu-id="dd3dc-1994">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1994">Fixes for #7002</span></span>
- <span data-ttu-id="dd3dc-1995">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="dd3dc-1996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1996">Az.Batch</span></span>
- <span data-ttu-id="dd3dc-1997">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="dd3dc-1998">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="dd3dc-1999">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-1999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="dd3dc-2000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2000">Az.Billing</span></span>
- <span data-ttu-id="dd3dc-2001">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="dd3dc-2002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2002">Az.CognitivServices</span></span>
- <span data-ttu-id="dd3dc-2003">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="dd3dc-2004">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="dd3dc-2005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2005">Az.ContainerInstance</span></span>
- <span data-ttu-id="dd3dc-2006">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="dd3dc-2007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="dd3dc-2008">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="dd3dc-2009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2009">Az.DataLakeStore</span></span>
- <span data-ttu-id="dd3dc-2010">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="dd3dc-2011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2011">Az.Monitor</span></span>
- <span data-ttu-id="dd3dc-2012">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="dd3dc-2013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2013">Az.KeyVault</span></span>
- <span data-ttu-id="dd3dc-2014">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="dd3dc-2015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2015">Az.MachineLearning</span></span>
- <span data-ttu-id="dd3dc-2016">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="dd3dc-2017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2017">Az.Media</span></span>
- <span data-ttu-id="dd3dc-2018">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="dd3dc-2019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2019">Az.Network</span></span>
<span data-ttu-id="dd3dc-2020">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="dd3dc-2021">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2021">New cmdlets added:</span></span>
        - <span data-ttu-id="dd3dc-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dd3dc-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dd3dc-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dd3dc-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dd3dc-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dd3dc-2027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="dd3dc-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="dd3dc-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="dd3dc-2030">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="dd3dc-2031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="dd3dc-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="dd3dc-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="dd3dc-2034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="dd3dc-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="dd3dc-2036">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="dd3dc-2037">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="dd3dc-2038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="dd3dc-2039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="dd3dc-2040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="dd3dc-2041">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="dd3dc-2042">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="dd3dc-2043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2043">Az.OperationalInsights</span></span>
- <span data-ttu-id="dd3dc-2044">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="dd3dc-2045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2045">Az.Profile</span></span>
- <span data-ttu-id="dd3dc-2046">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-2047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2047">Az.RecoveryServices</span></span>
- <span data-ttu-id="dd3dc-2048">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="dd3dc-2049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2049">Az.Resources</span></span>
- <span data-ttu-id="dd3dc-2050">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="dd3dc-2051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2051">Az.ServiceFabric</span></span>
- <span data-ttu-id="dd3dc-2052">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="dd3dc-2053">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="dd3dc-2054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2054">Az.SIgnalR</span></span>
- <span data-ttu-id="dd3dc-2055">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="dd3dc-2056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2056">Az.Sql</span></span>
- <span data-ttu-id="dd3dc-2057">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="dd3dc-2058">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="dd3dc-2059">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="dd3dc-2060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2060">Az.Storage</span></span>
- <span data-ttu-id="dd3dc-2061">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="dd3dc-2062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2062">Az.Websites</span></span>
- <span data-ttu-id="dd3dc-2063">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="dd3dc-2064">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="dd3dc-2065">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2065">General</span></span>

* <span data-ttu-id="dd3dc-2066">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="dd3dc-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2067">Az.Compute</span></span>

* <span data-ttu-id="dd3dc-2068">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="dd3dc-2069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2069">Az.DataLakeStore</span></span>

* <span data-ttu-id="dd3dc-2070">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="dd3dc-2071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2071">Az.FrontDoor</span></span>

* <span data-ttu-id="dd3dc-2072">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2072">Fixed some broken links</span></span>
    - <span data-ttu-id="dd3dc-2073">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="dd3dc-2074">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="dd3dc-2075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2075">Az.RecoveryServices</span></span>

* <span data-ttu-id="dd3dc-2076">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="dd3dc-2077">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="dd3dc-2078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2078">Az.Resources</span></span>

* <span data-ttu-id="dd3dc-2079">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="dd3dc-2080">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="dd3dc-2081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2081">Az.Sql</span></span>

* <span data-ttu-id="dd3dc-2082">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="dd3dc-2083">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="dd3dc-2084">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="dd3dc-2085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2085">Az.Storage</span></span>

* <span data-ttu-id="dd3dc-2086">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="dd3dc-2087">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="dd3dc-2088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="dd3dc-2089">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2089">Support Static Website configuration</span></span>
    - <span data-ttu-id="dd3dc-2090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="dd3dc-2091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="dd3dc-2092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2092">Az.Websites</span></span>

* <span data-ttu-id="dd3dc-2093">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="dd3dc-2094">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="dd3dc-2095">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="dd3dc-2096">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="dd3dc-2097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2097">Az.ApiManagement</span></span>
* <span data-ttu-id="dd3dc-2098">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="dd3dc-2099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2099">Az.Automation</span></span>
* <span data-ttu-id="dd3dc-2100">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="dd3dc-2101">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="dd3dc-2102">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="dd3dc-2103">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="dd3dc-2104">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="dd3dc-2105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2105">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-2106">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="dd3dc-2107">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="dd3dc-2108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2108">Az.ContainerInstance</span></span>
* <span data-ttu-id="dd3dc-2109">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="dd3dc-2110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="dd3dc-2111">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="dd3dc-2112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2112">Az.Network</span></span>
* <span data-ttu-id="dd3dc-2113">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="dd3dc-2114">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="dd3dc-2115">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="dd3dc-2116">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="dd3dc-2117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="dd3dc-2118">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="dd3dc-2119">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="dd3dc-2120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="dd3dc-2121">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="dd3dc-2122">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="dd3dc-2123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2123">Az.Relay</span></span>
* <span data-ttu-id="dd3dc-2124">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="dd3dc-2125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2125">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-2126">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="dd3dc-2127">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="dd3dc-2128">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="dd3dc-2129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2129">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd3dc-2130">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="dd3dc-2131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2131">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-2132">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="dd3dc-2133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dd3dc-2134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dd3dc-2135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dd3dc-2136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dd3dc-2137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="dd3dc-2138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="dd3dc-2139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="dd3dc-2140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="dd3dc-2141">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="dd3dc-2142">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="dd3dc-2143">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="dd3dc-2144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="dd3dc-2145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="dd3dc-2146">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="dd3dc-2147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="dd3dc-2148">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="dd3dc-2149">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="dd3dc-2150">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2150">General</span></span>
* <span data-ttu-id="dd3dc-2151">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="dd3dc-2152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2152">Az.Profile</span></span>
* <span data-ttu-id="dd3dc-2153">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="dd3dc-2154">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="dd3dc-2155">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="dd3dc-2156">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="dd3dc-2157">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="dd3dc-2158">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="dd3dc-2159">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="dd3dc-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="dd3dc-2161">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2162">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-2163">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="dd3dc-2164">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="dd3dc-2165">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd3dc-2166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2166">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd3dc-2167">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="dd3dc-2168">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="dd3dc-2169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2169">Az.Insights</span></span>
* <span data-ttu-id="dd3dc-2170">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="dd3dc-2171">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="dd3dc-2172">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="dd3dc-2173">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-2174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2174">Az.Network</span></span>
* <span data-ttu-id="dd3dc-2175">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="dd3dc-2176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="dd3dc-2177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="dd3dc-2178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="dd3dc-2179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="dd3dc-2180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="dd3dc-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dd3dc-2182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2182">Az.PolicyInsights</span></span>
* <span data-ttu-id="dd3dc-2183">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-2184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2184">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-2185">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="dd3dc-2186">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dd3dc-2187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2187">Az.ServiceBus</span></span>
* <span data-ttu-id="dd3dc-2188">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dd3dc-2189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2189">Az.ServiceFabric</span></span>
* <span data-ttu-id="dd3dc-2190">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="dd3dc-2191">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="dd3dc-2192">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="dd3dc-2193">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="dd3dc-2194">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="dd3dc-2195">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="dd3dc-2196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2196">Az.Profile</span></span>
* <span data-ttu-id="dd3dc-2197">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="dd3dc-2198">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-2199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2199">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-2200">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="dd3dc-2201">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dd3dc-2202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2202">Az.DataLakeStore</span></span>
* <span data-ttu-id="dd3dc-2203">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="dd3dc-2204">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="dd3dc-2205">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="dd3dc-2206">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="dd3dc-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-2208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2208">Az.Network</span></span>
* <span data-ttu-id="dd3dc-2209">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="dd3dc-2210">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-2211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2211">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-2212">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="dd3dc-2213">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="dd3dc-2214">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="dd3dc-2215">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2215">Azure.Storage</span></span>
* <span data-ttu-id="dd3dc-2216">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="dd3dc-2217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="dd3dc-2218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="dd3dc-2219">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="dd3dc-2220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2220">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dd3dc-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="dd3dc-2222">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dd3dc-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2223">Az.Compute</span></span>
* <span data-ttu-id="dd3dc-2224">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="dd3dc-2225">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="dd3dc-2226">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="dd3dc-2227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="dd3dc-2228">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dd3dc-2229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2229">Az.Network</span></span>
* <span data-ttu-id="dd3dc-2230">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="dd3dc-2231">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2231">new cmdlets added</span></span>
    - <span data-ttu-id="dd3dc-2232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="dd3dc-2233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="dd3dc-2234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="dd3dc-2235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="dd3dc-2236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="dd3dc-2237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="dd3dc-2238">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="dd3dc-2239">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="dd3dc-2240">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="dd3dc-2241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2241">Az.RedisCache</span></span>
* <span data-ttu-id="dd3dc-2242">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="dd3dc-2243">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="dd3dc-2244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2244">Az.Resources</span></span>
* <span data-ttu-id="dd3dc-2245">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="dd3dc-2246">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="dd3dc-2247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2247">Az.Sql</span></span>
* <span data-ttu-id="dd3dc-2248">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dd3dc-2249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2249">Az.Websites</span></span>
* <span data-ttu-id="dd3dc-2250">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="dd3dc-2251">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="dd3dc-2252">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="dd3dc-2253">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="dd3dc-2253">Initial Release</span></span>
