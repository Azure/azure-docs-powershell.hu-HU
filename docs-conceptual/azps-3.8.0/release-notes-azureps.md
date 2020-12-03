---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 382883b6a3d6915697b7954e4346613a04a6b870
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427649"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="f1748-103">Az Azure PowerShell kibocsátási megjegyzései</span><span class="sxs-lookup"><span data-stu-id="f1748-103">Azure PowerShell release notes</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="f1748-104">3.8.0 – 2020. április</span><span class="sxs-lookup"><span data-stu-id="f1748-104">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="f1748-105">A legutóbbi kiadás óta bevezetett újdonságok</span><span class="sxs-lookup"><span data-stu-id="f1748-105">Highlights since the last release</span></span>
* <span data-ttu-id="f1748-106">Az Az.Storage által támogatott PowerShell-verziók: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="f1748-106">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1748-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-107">Az.Accounts</span></span>
* <span data-ttu-id="f1748-108">Frissítve lett az Azure PowerShell-felmérés URL-címe a következő helyen: Resolve-AzError [#11507]</span><span class="sxs-lookup"><span data-stu-id="f1748-108">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f1748-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1748-109">Az.ApiManagement</span></span>
* <span data-ttu-id="f1748-110">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó értesítés az Azure File parancsmagok kimenetére vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="f1748-110">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="f1748-111">Set-AzApiManagementGroup – Frissítve lett a dokumentáció a GroupId paraméter meghatározása érdekében</span><span class="sxs-lookup"><span data-stu-id="f1748-111">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f1748-112">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1748-112">Az.Cdn</span></span>
* <span data-ttu-id="f1748-113">Ki lett javítva a díjszabási termékváltozat megjelenítése a ChinaCDN kapcsán</span><span class="sxs-lookup"><span data-stu-id="f1748-113">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1748-114">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1748-114">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1748-115">Támogatott identitás, Titkosítás, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="f1748-115">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-116">Az.Compute</span></span>
* <span data-ttu-id="f1748-117">Hozzá lett adva a Set-AzVmssOrchestrationServiceState parancsmag.</span><span class="sxs-lookup"><span data-stu-id="f1748-117">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="f1748-118">A Get-AzVmss az InstanceView használatával az OrchestrationService állapotait mutatja.</span><span class="sxs-lookup"><span data-stu-id="f1748-118">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1748-119">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1748-119">Az.IotHub</span></span>
* <span data-ttu-id="f1748-120">Az IoT-ikereszköz konfigurációjának kezelése, Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f1748-120">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="f1748-121">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="f1748-121">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="f1748-122">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="f1748-122">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="f1748-123">Hozzá lett adva egy parancsmag a közvetlen metódusok az IoT Hubban lévő eszközökön való meghívásához.</span><span class="sxs-lookup"><span data-stu-id="f1748-123">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="f1748-124">Az IoT-ikereszköz modulja konfigurációjának kezelése, Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f1748-124">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="f1748-125">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="f1748-125">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="f1748-126">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="f1748-126">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="f1748-127">Nagy méretekben történő automatikus IoT-eszközfelügyelet konfigurációjának kezelése.</span><span class="sxs-lookup"><span data-stu-id="f1748-127">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="f1748-128">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f1748-128">New cmdlets are:</span></span>
    - <span data-ttu-id="f1748-129">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1748-129">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f1748-130">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1748-130">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f1748-131">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1748-131">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f1748-132">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1748-132">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="f1748-133">Hozzá lett adva egy parancsmag az Edge-modul metódusok az IoT Hubban való meghívásához.</span><span class="sxs-lookup"><span data-stu-id="f1748-133">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1748-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1748-134">Az.KeyVault</span></span>
* <span data-ttu-id="f1748-135">Hozzá lett adva egy új Update-AzKeyVault parancsmag a helyreállító törlés és végleges törlés elleni védelem tárolón való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-135">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="f1748-136">Támogatás a következőhöz: Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="f1748-136">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="f1748-137">Ki lettek javítva a Remove-AzKeyVaultManagedStorageSasDefinition [#11479] példáinak hibái</span><span class="sxs-lookup"><span data-stu-id="f1748-137">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="f1748-138">Támogatás a privát végponthoz</span><span class="sxs-lookup"><span data-stu-id="f1748-138">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="f1748-139">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="f1748-139">Az.Maintenance</span></span>
* <span data-ttu-id="f1748-140">Karbantartási parancsmagok végleges verziójának közzététele az általánosan elérhető kiadás számára</span><span class="sxs-lookup"><span data-stu-id="f1748-140">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1748-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1748-141">Az.Monitor</span></span>
* <span data-ttu-id="f1748-142">Parancsmagok hozzáadva a privát kapcsolat hatóköréhez</span><span class="sxs-lookup"><span data-stu-id="f1748-142">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="f1748-143">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f1748-143">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f1748-144">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f1748-144">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f1748-145">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f1748-145">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f1748-146">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f1748-146">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f1748-147">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f1748-147">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="f1748-148">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f1748-148">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="f1748-149">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f1748-149">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-150">Az.Network</span></span>
* <span data-ttu-id="f1748-151">Frissítve lettek a parancsmagok a virtuális hálózati átjáróhoz való csatlakozás engedélyezéséhez magánhálózati IP-cím esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-151">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="f1748-152">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f1748-152">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="f1748-153">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f1748-153">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="f1748-154">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-154">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="f1748-155">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-155">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="f1748-156">Frissítve lettek a parancsmagok az FQDN-alapú LocalNetworkGateways és VpnSites engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-156">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="f1748-157">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f1748-157">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="f1748-158">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="f1748-158">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="f1748-159">Az IPv6-címcsalád támogatása a következőben: ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="f1748-159">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="f1748-160">Hozzá lett adva a Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-160">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="f1748-161">lehetővé teszi az összes meglévő tulajdonság beállítását, beleértve a következőt is: IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="f1748-161">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="f1748-162">Frissítve lett az Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-162">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="f1748-163">Hozzá lett adva egy másik opcionális AddressPrefixType paraméter a címelőtag címcsaládjának meghatározásához</span><span class="sxs-lookup"><span data-stu-id="f1748-163">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="f1748-164">Frissítve lettek a parancsmagok a DPD-időtúllépés beállításának engedélyezéséhez a virtuális hálózati átjáró kapcsolatain.</span><span class="sxs-lookup"><span data-stu-id="f1748-164">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="f1748-165">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-165">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="f1748-166">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-166">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f1748-167">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f1748-167">Az.PolicyInsights</span></span>
* <span data-ttu-id="f1748-168">Hozzá lett adva a Start-AzPolicyComplianceScan parancsmag a szabályzatok megfelelőségi vizsgálatának elindításához</span><span class="sxs-lookup"><span data-stu-id="f1748-168">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="f1748-169">Szabályzatdefiníció, készletdefiníció és hozzárendelési verziók hozzáadva a Get-AzPolicyState kimenetéhez</span><span class="sxs-lookup"><span data-stu-id="f1748-169">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1748-170">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1748-170">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1748-171">Tovább lett fejlesztve a kódok formázása és a használhatóság a New-AzServiceFabricCluster példái esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-171">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-172">Az.Sql</span></span>
* <span data-ttu-id="f1748-173">Hozzá lettek adva a Get-AzSqlInstanceOperation és a Stop-AzSqlInstanceOperation parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1748-173">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="f1748-174">Naplózás támogatása egy VNet-ben található tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-174">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-175">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-175">Az.Storage</span></span>
* <span data-ttu-id="f1748-176">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó értesítés az Azure File parancsmagok kimenetére vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="f1748-176">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="f1748-177">Támogatott új SkuName StandardGZRS, StandardRAGZRS a Storage-fiók létrehozása/frissítése során</span><span class="sxs-lookup"><span data-stu-id="f1748-177">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="f1748-178">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1748-178">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="f1748-179">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1748-179">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f1748-180">Támogatott Data Lake Gen2</span><span class="sxs-lookup"><span data-stu-id="f1748-180">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="f1748-181">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f1748-181">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f1748-182">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f1748-182">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f1748-183">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="f1748-183">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="f1748-184">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f1748-184">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f1748-185">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="f1748-185">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="f1748-186">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f1748-186">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f1748-187">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="f1748-187">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="f1748-188">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f1748-188">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="f1748-189">0.10.0-s előzetes verzió – 2020. április</span><span class="sxs-lookup"><span data-stu-id="f1748-189">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="f1748-190">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f1748-190">General</span></span>
* <span data-ttu-id="f1748-191">Az Az modulok előzetes verziója mostantól elérhető az Azure Stack Hubon.</span><span class="sxs-lookup"><span data-stu-id="f1748-191">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="f1748-192">Ez lehetővé teszi a platformok közötti kompatibilitást a Linux és a macOs rendszerekkel.</span><span class="sxs-lookup"><span data-stu-id="f1748-192">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="f1748-193">A Azure Stack Hub mostantól támogatja a PowerShell Core-t az Az modulokkal, további információt [itt](/azure-stack/operator/powershell-install-az-module) talál</span><span class="sxs-lookup"><span data-stu-id="f1748-193">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="f1748-194">Az Az modulok támogatják a 2019-03-01-hybrid profilt:</span><span class="sxs-lookup"><span data-stu-id="f1748-194">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="f1748-195">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f1748-195">Az.Billing</span></span>
  - <span data-ttu-id="f1748-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-196">Az.Compute</span></span>
  - <span data-ttu-id="f1748-197">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f1748-197">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="f1748-198">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1748-198">Az.EventHub</span></span>
  - <span data-ttu-id="f1748-199">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1748-199">Az.IotHub</span></span>
  - <span data-ttu-id="f1748-200">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1748-200">Az.KeyVault</span></span>
  - <span data-ttu-id="f1748-201">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1748-201">Az.Monitor</span></span>
  - <span data-ttu-id="f1748-202">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-202">Az.Network</span></span>
  - <span data-ttu-id="f1748-203">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-203">Az.Resources</span></span>
  - <span data-ttu-id="f1748-204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-204">Az.Storage</span></span>
  - <span data-ttu-id="f1748-205">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-205">Az.Websites</span></span>
* <span data-ttu-id="f1748-206">A következő három új PowerShell-modul lett bevezetve, amelyek használhatók az Azure Stack Hubbal: Az.Databox, Az.IotHub és Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1748-206">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="f1748-207">A parancsok viszonylag változatlanok maradnak, kisebb módosításokkal. Például az Az helyébe az AzureRM lép.</span><span class="sxs-lookup"><span data-stu-id="f1748-207">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="f1748-208">Az Azure Stack Hubhoz kapcsolódó PowerShell-dokumentáció frissített hivatkozását [itt](/azure-stack/operator/powershell-install-az-module) találja</span><span class="sxs-lookup"><span data-stu-id="f1748-208">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="f1748-209">3.7.0 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="f1748-209">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1748-210">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-210">Az.Accounts</span></span>
* <span data-ttu-id="f1748-211">Ki lett javítva az a hiba, hogy a Get-AzTenant/Get-AzDefault/Set-AzDefault parancs NullReferenceException hibát ad vissza kijelentkezett állapotban [#10292]</span><span class="sxs-lookup"><span data-stu-id="f1748-211">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-212">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-212">Az.Compute</span></span>
* <span data-ttu-id="f1748-213">A következő paraméterek lettek hozzáadva a New-AzDiskConfig parancsmaghoz:</span><span class="sxs-lookup"><span data-stu-id="f1748-213">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="f1748-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="f1748-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="f1748-215">Engedélyezve lett a New-AzGalleryImageVersion parancsmag célparaméterének titkosítási tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="f1748-215">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="f1748-216">Ki lett javítva a tempDisk hibája a Set-AzVmss -Reimage és az Invoke-AzVMReimage parancsmag esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-216">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="f1748-217">[#11354]</span><span class="sxs-lookup"><span data-stu-id="f1748-217">[#11354]</span></span>
* <span data-ttu-id="f1748-218">Az alábbi parancsmagok mostantól támogatottak az új SAP-bővítmény esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-218">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="f1748-219">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f1748-219">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f1748-220">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f1748-220">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f1748-221">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f1748-221">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f1748-222">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f1748-222">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="f1748-223">Ki lettek javítva a súgódokumentáció példáinak hibái</span><span class="sxs-lookup"><span data-stu-id="f1748-223">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="f1748-224">Táblázatos formátumban jelenítette meg a sztring pontos értékét a PowerState virtuális gép esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-224">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="f1748-225">New-AzVmssConfig: ki lett javítva az AutomaticRepairs tulajdonság szerializálása a SinglePlacementGroup letiltott állapota esetén.</span><span class="sxs-lookup"><span data-stu-id="f1748-225">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="f1748-226">[#11257]</span><span class="sxs-lookup"><span data-stu-id="f1748-226">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1748-227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1748-227">Az.DataFactory</span></span>
* <span data-ttu-id="f1748-228">Az ADF .Net SDK a 4.8.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f1748-228">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="f1748-229">Opcionális paraméterek lettek hozzáadva az Invoke-AzDataFactoryV2Pipeline parancshoz az újrafuttatás támogatásához</span><span class="sxs-lookup"><span data-stu-id="f1748-229">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1748-230">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1748-230">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1748-231">Hozzá lett adva a kompatibilitástörő változás leírása az Export-AzDataLakeStoreItem és az Import-AzDataLakeStoreItem parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-231">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="f1748-232">A bájtkódolási lehetőség hozzá lett adva a New-AzDataLakeStoreItem, az Add-AzDAtaLakeStoreItemContent és a Get-AzDAtaLakeStoreItemContent parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-232">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1748-233">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1748-233">Az.HDInsight</span></span>
* <span data-ttu-id="f1748-234">Fürt létrehozásakor a minimálisan támogatott TLS-verzió megadása támogatott.</span><span class="sxs-lookup"><span data-stu-id="f1748-234">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1748-235">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1748-235">Az.IotHub</span></span>
* <span data-ttu-id="f1748-236">Hozzá lett adva az elosztott beállítások eszközönkénti felügyeletének támogatása.</span><span class="sxs-lookup"><span data-stu-id="f1748-236">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="f1748-237">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f1748-237">New Cmdlets are:</span></span>
    - <span data-ttu-id="f1748-238">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="f1748-238">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="f1748-239">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="f1748-239">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1748-240">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1748-240">Az.KeyVault</span></span>
* <span data-ttu-id="f1748-241">Kompatibilitástörő változást okozó attribútumok lettek hozzáadva a New-AzKeyVault parancshoz</span><span class="sxs-lookup"><span data-stu-id="f1748-241">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1748-242">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1748-242">Az.Monitor</span></span>
* <span data-ttu-id="f1748-243">Frissült a New-AzScheduledQueryRuleLogMetricTrigger dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f1748-243">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-244">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-244">Az.Network</span></span>
* <span data-ttu-id="f1748-245">Frissültek a parancsmagok a több-bérlős VirtualHubVnetConnections engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-245">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="f1748-246">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-246">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f1748-247">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-247">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f1748-248">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f1748-248">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="f1748-249">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f1748-249">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="f1748-250">Az SQL Management SDK-függőség el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="f1748-250">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f1748-251">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f1748-251">Az.PolicyInsights</span></span>
* <span data-ttu-id="f1748-252">Továbbfejlesztett hibaüzenetek</span><span class="sxs-lookup"><span data-stu-id="f1748-252">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-254">Hozzá lett adva az Azure Site Recovery-támogatás az Azure Diskkel titkosított virtuális gépek védelmének újbóli beállítása és frissített virtuálisgép-tulajdonságai esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-254">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="f1748-255">Hozzá lett adva az Azure Site Recovery VmwareToAzure tulajdonságainak vészhelyreállítási monitorozása</span><span class="sxs-lookup"><span data-stu-id="f1748-255">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="f1748-256">Hozzá lett adva az Azure Backup-támogatás a sikertelen elemekre vonatkozó szabályzatfrissítés újbóli végrehajtása esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-256">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="f1748-257">Hozzá lett adva az Azure Backup-támogatás a lemezkizárási beállításokhoz a biztonsági mentés és a visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="f1748-257">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="f1748-258">Hozzá lett adva az Azure Backup-támogatás több fájl/mappa visszaállításához az AzureFileShare-ben</span><span class="sxs-lookup"><span data-stu-id="f1748-258">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="f1748-259">Hozzá lett adva az Azure Backup-támogatás a felhasználó által megadott erőforráscsoport támogatásához az IaasVM-szabályzat frissítésekor</span><span class="sxs-lookup"><span data-stu-id="f1748-259">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-260">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-260">Az.Resources</span></span>
* <span data-ttu-id="f1748-261">Ki lett javítva a Get-AzResource-ResourceGroupName-Name-ExpandProperties-ResourceType parancs, hogy ezentúl az erőforrások aktuális API-verzióját használja az alapértelmezett verzió helyett [#11267]</span><span class="sxs-lookup"><span data-stu-id="f1748-261">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="f1748-262">Hozzá lett adva a CorrelationId-naplózás a hibaforgatókönyvek esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-262">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="f1748-263">A Get-AzResourceLock dokumentációjában kisebb módosítás történt.</span><span class="sxs-lookup"><span data-stu-id="f1748-263">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="f1748-264">Példa hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f1748-264">Added example.</span></span>
* <span data-ttu-id="f1748-265">A szimpla idézőjel fel lett oldva a Get-AzADUser paraméterértékében [#11317]</span><span class="sxs-lookup"><span data-stu-id="f1748-265">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="f1748-266">Új parancsmagok lettek hozzáadva az üzembehelyezési szkriptekhez (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript)</span><span class="sxs-lookup"><span data-stu-id="f1748-266">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-267">Az.Sql</span></span>
* <span data-ttu-id="f1748-268">Olvasható másodlagos paraméter lett hozzáadva az Invoke-AzSqlDatabaseFailover parancshoz</span><span class="sxs-lookup"><span data-stu-id="f1748-268">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="f1748-269">A Disable-AzSqlServerActiveDirectoryOnlyAuthentication parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f1748-269">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="f1748-270">Az érzékenységi besorolás mentése megtörténik az adatbázis oszlopainak osztályozásakor.</span><span class="sxs-lookup"><span data-stu-id="f1748-270">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="f1748-271">Az.Support</span><span class="sxs-lookup"><span data-stu-id="f1748-271">Az.Support</span></span>
* <span data-ttu-id="f1748-272">Az Az.Support modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="f1748-272">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-273">Az.Websites</span></span>
* <span data-ttu-id="f1748-274">Mostantól támogatott a webalkalmazások forgalom-útválasztási szabályainak az alábbi új parancsmagokkal történő használata</span><span class="sxs-lookup"><span data-stu-id="f1748-274">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="f1748-275">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f1748-275">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f1748-276">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f1748-276">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f1748-277">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f1748-277">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f1748-278">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f1748-278">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="f1748-279">3.6.1 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="f1748-279">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1748-280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-280">Az.Accounts</span></span>
* <span data-ttu-id="f1748-281">Azure PowerShell felmérési oldal megnyitása itt: Send-Feedback [#11020]</span><span class="sxs-lookup"><span data-stu-id="f1748-281">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="f1748-282">Azure PowerShell-felmérés URL-címének megjelenítése itt: Resolve-Error [#11021]</span><span class="sxs-lookup"><span data-stu-id="f1748-282">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="f1748-283">Az-verzió hozzáadva az UserAgenthez</span><span class="sxs-lookup"><span data-stu-id="f1748-283">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f1748-284">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1748-284">Az.ApiManagement</span></span>
* <span data-ttu-id="f1748-285">Mostantól támogatott az egyéni tartomány lekérése és konfigurálása a DeveloperPortal végpontján [#11007]</span><span class="sxs-lookup"><span data-stu-id="f1748-285">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="f1748-286">Export-AzApiManagementAPi – Mostantól támogatott az Api-definíció Json formátumban való letöltése [#9987]</span><span class="sxs-lookup"><span data-stu-id="f1748-286">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="f1748-287">Import-AzApiManagementApi – Az OpenAPI 3.0-definíció Json-dokumentumokból való importálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f1748-287">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="f1748-288">New-AzApiManagementIdentityProvider és Set-AzApiManagementIdentityProvider – A Signin Tenant konfigurálása az AAD B2C-szolgáltató esetében mostantól támogatott. [#9784]</span><span class="sxs-lookup"><span data-stu-id="f1748-288">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1748-289">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1748-289">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1748-290">A System.Buffershez hivatkozásának explicit hozzáadása a következőkben: csproj és psd1</span><span class="sxs-lookup"><span data-stu-id="f1748-290">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1748-291">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1748-291">Az.IotHub</span></span>
* <span data-ttu-id="f1748-292">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f1748-292">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f1748-293">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f1748-293">New Cmdlets are:</span></span>
    - <span data-ttu-id="f1748-294">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1748-294">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f1748-295">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1748-295">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f1748-296">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1748-296">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f1748-297">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1748-297">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="f1748-298">A cél IoT-eszközökön lévő modulok IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f1748-298">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="f1748-299">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f1748-299">New Cmdlets are:</span></span>
    - <span data-ttu-id="f1748-300">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="f1748-300">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="f1748-301">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="f1748-301">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="f1748-302">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="f1748-302">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="f1748-303">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="f1748-303">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="f1748-304">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-304">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f1748-305">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz modulja kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-305">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f1748-306">Az IoT-eszközök szülő eszközének lekérése/beállítása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f1748-306">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="f1748-307">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f1748-307">New Cmdlets are:</span></span>
    - <span data-ttu-id="f1748-308">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="f1748-308">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="f1748-309">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1748-309">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="f1748-310">Az eszközök szülő-gyermek kapcsolatainak kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f1748-310">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1748-311">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1748-311">Az.Monitor</span></span>
* <span data-ttu-id="f1748-312">A Get-AzMetricDefinition kimeneti értéke javítva [#9714]</span><span class="sxs-lookup"><span data-stu-id="f1748-312">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-313">Az.Network</span></span>
* <span data-ttu-id="f1748-314">SQL Management SDK frissítve.</span><span class="sxs-lookup"><span data-stu-id="f1748-314">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="f1748-315">Kijavítottuk a PrivateLinkServiceConnectionState osztály eltérő elnevezéssel kapcsolatos hibáját.</span><span class="sxs-lookup"><span data-stu-id="f1748-315">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="f1748-316">Az ActionsRequired mező leképezése a követezőre: ActionRequired</span><span class="sxs-lookup"><span data-stu-id="f1748-316">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="f1748-317">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="f1748-317">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-318">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-318">Az.Resources</span></span>
* <span data-ttu-id="f1748-319">A Get-AzRoleAssignment null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="f1748-319">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="f1748-320">A -Force és a -PassThru kapcsoló nem kötelezőként lett megjelölve a Remove-AzADGroup esetében [#10849]</span><span class="sxs-lookup"><span data-stu-id="f1748-320">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="f1748-321">Javítva a hiba, amely miatt a MailNickname nem lett visszaadva Remove-AzADGroup esetében [#11167]</span><span class="sxs-lookup"><span data-stu-id="f1748-321">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="f1748-322">A Remove-AzADGroup folyamatművelet működési hibája kijavítva [#11171]</span><span class="sxs-lookup"><span data-stu-id="f1748-322">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="f1748-323">A GetAzureRoleAssignmentCommand null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="f1748-323">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="f1748-324">Kompatibilitástörő változás hozzáadva a szabályzati parancsmagok soron következő változásaihoz</span><span class="sxs-lookup"><span data-stu-id="f1748-324">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="f1748-325">Frissült a Get-AzResourceGroup az erőforráscsoport-címke kiszolgálóoldali szűrésének elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-325">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="f1748-326">A címkeparancsmagok kiterjesztése a -ResourceID elfogadása érdekében</span><span class="sxs-lookup"><span data-stu-id="f1748-326">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="f1748-327">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1748-327">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f1748-328">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1748-328">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f1748-329">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1748-329">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="f1748-330">Új címkeparancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-330">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="f1748-331">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1748-331">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="f1748-332">A ScopedDeployment áthozva az SDK 3.3.0-ból</span><span class="sxs-lookup"><span data-stu-id="f1748-332">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-333">Az.Sql</span></span>
* <span data-ttu-id="f1748-334">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="f1748-334">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="f1748-335">Támogatás hozzáadva a biztonsági másolatok hosszú távú megőrzési konfigurációjához a felügyelt adatbázisok esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-335">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="f1748-336">LTR-szabályzat lekérése/beállítása felügyelt adatbázison</span><span class="sxs-lookup"><span data-stu-id="f1748-336">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="f1748-337">LTR biztonsági másolat(ok) lekérése felügyelt adatbázis, felügyelt példány vagy hely szerint</span><span class="sxs-lookup"><span data-stu-id="f1748-337">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="f1748-338">LTR biztonsági másolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f1748-338">Remove an LTR backup</span></span>
    - <span data-ttu-id="f1748-339">LTR biztonsági másolat visszaállítása új felügyelt adatbázis létrehozásához</span><span class="sxs-lookup"><span data-stu-id="f1748-339">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="f1748-340">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="f1748-340">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="f1748-341">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlInstance és Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f1748-341">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="f1748-342">Az SQL SDK-verzió felléptetése a következőhöz: AZ.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-342">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-343">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-343">Az.Storage</span></span>
* <span data-ttu-id="f1748-344">Támogatott AllowProtectedAppendWrite a következőben: ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f1748-344">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="f1748-345">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f1748-345">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="f1748-346">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet az AzureStorageTable típusának módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="f1748-346">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="f1748-347">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="f1748-347">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="f1748-348">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="f1748-348">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-349">Az.Websites</span></span>
* <span data-ttu-id="f1748-350">Címke paraméter hozzáadva a következőkhöz: New-AzAppServicePlan és Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f1748-350">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="f1748-351">A parancsmag végrehajtásának leállítása, ha egy egyéni tartomány webhelyhez történő hozzáadásakor a rendszer kivételt ad vissza</span><span class="sxs-lookup"><span data-stu-id="f1748-351">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="f1748-352">Támogatás hozzáadva az olyan App Services műveletek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag</span><span class="sxs-lookup"><span data-stu-id="f1748-352">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="f1748-353">Hozzáférési korlátozás alkalmazva a különböző erőforráscsoportokban lévő webalkalmazásokra/függvényekre</span><span class="sxs-lookup"><span data-stu-id="f1748-353">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="f1748-354">Az egyéni WebAppSlots-gazdanevek beállítására vonatkozó hiba kijavítva</span><span class="sxs-lookup"><span data-stu-id="f1748-354">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="f1748-355">3.5.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="f1748-355">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f1748-356">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="f1748-356">Highlights since the last major release</span></span>
* <span data-ttu-id="f1748-357">Frissült az ügyféloldali telemetria.</span><span class="sxs-lookup"><span data-stu-id="f1748-357">Updated client side telemetry.</span></span>
* <span data-ttu-id="f1748-358">Az.IotHub: parancsmagok hozzáadva az eszközkezelés támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f1748-358">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="f1748-359">Az.SqlVirtualMachine: parancsmagok hozzáadva a rendelkezésreállási csoport figyelőjéhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-359">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1748-360">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-360">Az.Accounts</span></span>
* <span data-ttu-id="f1748-361">A SubscriptionId, a TenantId és a végrehajtási idő hozzáadva az ügyféloldali telemetria adataihoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-361">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1748-362">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1748-362">Az.Automation</span></span>
* <span data-ttu-id="f1748-363">Ki lett javítva a „New-AzAutomationSoftwareUpdateConfiguration” referenciadokumentációjának 1. példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="f1748-363">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1748-364">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1748-364">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1748-365">Az SDK a 7.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f1748-365">Updated SDK to 7.0</span></span>
* <span data-ttu-id="f1748-366">Tovább lett fejlesztve a hibaüzenet, amely akkor jelenik meg, ha a kiszolgáló üres törzset ad vissza válaszként</span><span class="sxs-lookup"><span data-stu-id="f1748-366">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-367">Az.Compute</span></span>
* <span data-ttu-id="f1748-368">A ProximityPlacementGroupId mostantól üres értékkel is rendelkezhet a frissítés során</span><span class="sxs-lookup"><span data-stu-id="f1748-368">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f1748-369">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1748-369">Az.FrontDoor</span></span>
* <span data-ttu-id="f1748-370">Új parancsmag hozzáadva a WAF-ban használható felügyelt szabálydefiníciók lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-370">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1748-371">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1748-371">Az.IotHub</span></span>
* <span data-ttu-id="f1748-372">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f1748-372">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f1748-373">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f1748-373">New Cmdlets are:</span></span>
    - <span data-ttu-id="f1748-374">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1748-374">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f1748-375">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1748-375">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f1748-376">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1748-376">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f1748-377">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f1748-377">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1748-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1748-378">Az.KeyVault</span></span>
* <span data-ttu-id="f1748-379">Ki lett javítva az Add-AzKeyVaultKey.md duplikált szövege</span><span class="sxs-lookup"><span data-stu-id="f1748-379">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1748-380">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1748-380">Az.Monitor</span></span>
* <span data-ttu-id="f1748-381">Ki lett javítva a Get-AzLog parancsmag leírása.</span><span class="sxs-lookup"><span data-stu-id="f1748-381">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="f1748-382">Egy új, ActionGroupId nevű paraméter lett hozzáadva a „New-AzMetricAlertRuleV2” parancshoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-382">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="f1748-383">A felhasználó a következőket adhatja meg: ActionGroupId(string) vagy ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="f1748-383">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-384">Az.Network</span></span>
* <span data-ttu-id="f1748-385">Hozzá lett adva egy extra paramétermegjegyzés a „New-AzPrivateLinkService” parancsmag „-EnableProxyProtocol” paraméteréhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-385">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="f1748-386">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-386">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f1748-387">Hozzá lett adva egy csomagrögzítési példa a Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és Start-AzVirtualnetworkGatewayPacketCapture.md minden belső és külső csomagjának rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-387">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f1748-388">Az Azure Firewall-szabályzat mostantól támogatott a Vnet-tűzfalakon</span><span class="sxs-lookup"><span data-stu-id="f1748-388">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="f1748-389">Nem lettek hozzáadva új parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="f1748-389">No new cmdlets are added.</span></span> <span data-ttu-id="f1748-390">Enyhítve lettek a tűzfalszabályzat korlátozásai a Vnet-tűzfalak esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-390">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-392">A fájlokként történő visszaállítás mostantól támogatott az SQL-adatbázisok esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-392">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-393">Az.Resources</span></span>
* <span data-ttu-id="f1748-394">Újra lettek tervezve a sablonalapú üzembehelyezési parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1748-394">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="f1748-395">Új parancsmagok lettek hozzáadva a felügyeleti csoportban való üzembe helyezés kezeléséhez: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f1748-395">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="f1748-396">Új parancsmagok lettek hozzáadva a bérlői hatókörben való üzembe helyezés kezeléséhez: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f1748-396">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="f1748-397">Az \*-AzDeployment parancsmagok kifejezetten az előfizetési hatókörben való működéshez lettek újratervezve</span><span class="sxs-lookup"><span data-stu-id="f1748-397">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="f1748-398">Az \*-AzSubscriptionDeployment aliasok lettek létrehozva az \*-AzDeployment parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-398">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="f1748-399">Ki lett javítva az „Update-AzADApplication” nem beállított „AvailableToOtherTenants” paraméter esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-399">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="f1748-400">Az ApplicationObjectWithoutCredentialParameterSet el lett távolítva az AmbiguousParameterSetException elkerülése érdekében.</span><span class="sxs-lookup"><span data-stu-id="f1748-400">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="f1748-401">A súgófájlok újra létre lettek hozva</span><span class="sxs-lookup"><span data-stu-id="f1748-401">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-402">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-402">Az.Sql</span></span>
* <span data-ttu-id="f1748-403">Az előfizetések közötti időponthoz kötött visszaállítás mostantól támogatott a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="f1748-403">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="f1748-404">A már meglévő felügyelt SQL-példány hardvergenerációjának módosítása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="f1748-404">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="f1748-405">Ki lettek javítva az „Update-AzSqlServerVulnerabilityAssessmentSetting” súgópéldái: paraméter/tulajdonságkimenet – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="f1748-405">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f1748-406">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f1748-406">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f1748-407">Parancsmagokat hozzáadva a rendelkezésreállási csoport figyelőjéhez</span><span class="sxs-lookup"><span data-stu-id="f1748-407">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f1748-408">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f1748-408">Az.StorageSync</span></span>
* <span data-ttu-id="f1748-409">Frissültek az „Invoke-AzStorageSyncCompatibilityCheck” támogatott karakterkészletei.</span><span class="sxs-lookup"><span data-stu-id="f1748-409">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="f1748-410">3.4.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="f1748-410">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f1748-411">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="f1748-411">Highlights since the last major release</span></span>
* <span data-ttu-id="f1748-412">Megjelent az Az.CosmosDB 0.1.0-s kezdeti verziója</span><span class="sxs-lookup"><span data-stu-id="f1748-412">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="f1748-413">Az.Network ConnectionMonitor V2 támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f1748-413">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1748-414">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-414">Az.Accounts</span></span>
* <span data-ttu-id="f1748-415">A környezet automatikus mentésének letiltása, ha az AzureRmContext.json nem érhető el</span><span class="sxs-lookup"><span data-stu-id="f1748-415">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="f1748-416">Az Azure Powershell Common referenciájának frissítése 1.3.5-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="f1748-416">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f1748-417">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1748-417">Az.ApiManagement</span></span>
* <span data-ttu-id="f1748-418">**Get-AzApiManagementApiSchema** Az API-val társított Open-API séma kijavítása   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="f1748-418">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="f1748-419">**New-AzApiManagementProduct** _ és _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="f1748-419">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="f1748-420"> https://github.com/Azure/azure-powershell/issues/10472 dokumentációja kijavítva</span><span class="sxs-lookup"><span data-stu-id="f1748-420">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="f1748-421">**Set-AzApiManagementApi** A ServiceUrl parancsmaggal való frissítését bemutató példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-421">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-422">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-422">Az.Compute</span></span>
* <span data-ttu-id="f1748-423">A virtuális gép állapotának korlátozása 100 értékre, hogy ne legyen szabályozás, ha a Get-AzVM -Status a virtuális gép neve nélkül lett végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="f1748-423">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="f1748-424">Update-AzDiskEncryptionSet parancsmagok hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f1748-424">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="f1748-425">Az EncryptionType és a DiskEncryptionSetId paraméterek hozzáadása a következő parancsmagokhoz:</span><span class="sxs-lookup"><span data-stu-id="f1748-425">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="f1748-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="f1748-427">A ColocationStatus paraméter hozzáadva a Get-AzProximityPlacementGroup parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-427">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1748-428">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1748-428">Az.DataFactory</span></span>
* <span data-ttu-id="f1748-429">Az ADF .Net SDK frissítve lett a 4.7.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="f1748-429">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f1748-430">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f1748-430">Az.DeploymentManager</span></span>
* <span data-ttu-id="f1748-431">LIST műveletek hozzáadása az erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-431">Adds LIST operations for resources</span></span>
* <span data-ttu-id="f1748-432">Műveletek végrehajtásának lehetősége az állapotellenőrzés lépésein</span><span class="sxs-lookup"><span data-stu-id="f1748-432">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1748-433">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1748-433">Az.HDInsight</span></span>
* <span data-ttu-id="f1748-434">A New-AzHDInsightCluster dokumentációs hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="f1748-434">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1748-435">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1748-435">Az.KeyVault</span></span>
* <span data-ttu-id="f1748-436">Name alias hozzáadása a VaultName attribútumhoz, hogy a Remove-AzureKeyVault konzisztens legyen a New-AzureKeyVault paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="f1748-436">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-437">Az.Network</span></span>
* <span data-ttu-id="f1748-438">Új példa hozzáadva a Set-AzNetworkWatcherConfigFlowLog.md fájlhoz a Traffic Analytics-letiltási forgatókönyv szemléltetésére.</span><span class="sxs-lookup"><span data-stu-id="f1748-438">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="f1748-439">Felügyeleti IP-konfiguráció támogatás hozzáadva az Azure Firewallhoz – egy dedikált alhálózat és nyilvános IP-cím, amelyet a tűzfal a forgalom felügyeléséhez használni fog</span><span class="sxs-lookup"><span data-stu-id="f1748-439">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="f1748-440">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="f1748-440">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f1748-441">Hozzá lett adva a (nem kötelező) -PublicIpAddress-ManagementPublicIpAddress paraméter, amely egy nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="f1748-441">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="f1748-442">Hozzá lett adva a SetManagementIpConfiguration metódus a tűzfalobjektumok esetében – nyilvános IP-cím-objektumokat fogad el bemeneti adatként – az alhálózat nevének AzureFirewallManagementSubnet értéknek kell lennie</span><span class="sxs-lookup"><span data-stu-id="f1748-442">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="f1748-443">A Get-AzNetworkSecurityGroup példái javítva, hogy hálózati biztonsági csoportok példáit tartalmazzák hálózati adapterek helyett.</span><span class="sxs-lookup"><span data-stu-id="f1748-443">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="f1748-444">Javítottunk egy elírást a New-AzVpnSite parancsban, amely megakadályozta, hogy az erőforrásazonosító-kiegészítő kiegészítsen egy paramétert.</span><span class="sxs-lookup"><span data-stu-id="f1748-444">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="f1748-445">Az Application Gateway szabály-újraírási műveletkészletének URL-konfigurálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f1748-445">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="f1748-446">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f1748-446">New cmdlets added:</span></span>
        - <span data-ttu-id="f1748-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1748-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="f1748-448">A parancsmagok frissültek a nem kötelező UrlConfiguration paraméterrel</span><span class="sxs-lookup"><span data-stu-id="f1748-448">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="f1748-449">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f1748-449">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="f1748-450">A Network Watcher Connection Monitor 2-es verziójú erőforrások támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-450">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f1748-451">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f1748-451">Az.PolicyInsights</span></span>
* <span data-ttu-id="f1748-452">A javítandó erőforrások azonosítása előtti megfelelőségértékelés támogatása</span><span class="sxs-lookup"><span data-stu-id="f1748-452">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="f1748-453">-ResourceDiscoverMode paraméter hozzáadása a Start-AzPolicyRemediation parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-453">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="f1748-454">A szabályzatok metaadat-erőforrásainak elérésére szolgáló Get-AzPolicyMetadata parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f1748-454">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="f1748-455">A Get-AzPolicyState és a Get-AzPolicyStateSummary frissült a 2019-10-01 API-verzióhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-455">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-456">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-456">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-457">Azure Site Recovery-támogatás a replikált lemezek eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="f1748-457">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="f1748-458">Hozzáadott Azure Backup-támogatás a helyreállítási tárak létrehozása közbeni címkehozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-458">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-459">Az.Resources</span></span>
* <span data-ttu-id="f1748-460">A -Scope választható a \*-AzPolicyAssignment parancsmagokban; az alapértelmezett érték a környezeti előfizetés</span><span class="sxs-lookup"><span data-stu-id="f1748-460">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="f1748-461">Az ADServicePrincipal jelszó és kulcs típusú hitelesítő adatokkal való létrehozását szemléltető példák hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-461">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-462">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-462">Az.Sql</span></span>
<span data-ttu-id="f1748-463">A New-AzSqlDatabaseSecondary parancsmag javítva, hogy a PartnerDatabaseName létezését ellenőrizze a DatabaseName létezése helyett.</span><span class="sxs-lookup"><span data-stu-id="f1748-463">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-464">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-464">Az.Storage</span></span>
* <span data-ttu-id="f1748-465">A Table/Queue Encryption Keytype készlet beállításának támogatása Storage-fiók létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="f1748-465">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="f1748-466">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1748-466">New-AzStorageAccount</span></span>
* <span data-ttu-id="f1748-467">RequestId megjelenítése, ha a StorageException nem rendelkezik ExtendedErrorInformation paraméterrel</span><span class="sxs-lookup"><span data-stu-id="f1748-467">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="f1748-468">A Start-AzStorageBlobCopy parancsmag 6. példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="f1748-468">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-469">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-469">Az.Websites</span></span>
* <span data-ttu-id="f1748-470">A Set-AzWebapp és a Set-AzWebappSlot támogatja az AlwaysOn, a MinTls és a FtpsState tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="f1748-470">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="f1748-471">Javítva a hiba, amely miatt a HttpsOnly és az AppservicePlan Set-AzWebApp paranccsal történő egyidejű módosításakor a HttpsOnly paraméter alaphelyzetbe állt.</span><span class="sxs-lookup"><span data-stu-id="f1748-471">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="f1748-472">3.3.0 – 2020. január</span><span class="sxs-lookup"><span data-stu-id="f1748-472">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1748-473">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-473">Az.Accounts</span></span>
* <span data-ttu-id="f1748-474">Frissítve lettek az Add-AzEnvironment és Set-AzEnvironment parancsmagok, amelyek mostantól elfogadják az AzureAttestationServiceEndpointResourceId és AzureAttestationServiceEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="f1748-474">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f1748-475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1748-475">Az.Cdn</span></span>
* <span data-ttu-id="f1748-476">A hibaválasz részleteinek láthatóvá tétele a New-AzCdnEndpoint parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f1748-476">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-477">Az.Compute</span></span>
* <span data-ttu-id="f1748-478">Javítva lett a Set-AzVMCustomScriptExtension parancsmag az olyan virtuális gépek esetében, amelyek felügyelt operációsrendszer-lemeze nem rendelkezik operációsrendszer-profillal.</span><span class="sxs-lookup"><span data-stu-id="f1748-478">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f1748-479">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f1748-479">Az.ContainerInstance</span></span>
* <span data-ttu-id="f1748-480">Javítva lettek a New-AzContainerGroup parancsmagpélda által használt paraméternevek</span><span class="sxs-lookup"><span data-stu-id="f1748-480">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f1748-481">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f1748-481">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f1748-482">Hozzá lett adva a Get-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="f1748-482">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f1748-483">Az Edge Storage-tároló lekérése</span><span class="sxs-lookup"><span data-stu-id="f1748-483">Get the Edge Storage Container</span></span>
* <span data-ttu-id="f1748-484">Hozzá lett adva a New-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="f1748-484">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f1748-485">Új Edge Storage-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="f1748-485">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="f1748-486">Hozzá lett adva a Remove-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="f1748-486">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f1748-487">Az Edge Storage-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f1748-487">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="f1748-488">Hozzá lett adva az Invoke-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="f1748-488">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f1748-489">Meghívási művelet az Edge Storage-tárolóban lévő adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-489">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="f1748-490">Hozzá lett adva a Get-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="f1748-490">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f1748-491">Az Edge Storage-fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="f1748-491">Get the Edge Storage Account</span></span>
* <span data-ttu-id="f1748-492">Hozzá lett adva a New-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="f1748-492">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f1748-493">Új Edge Storage-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="f1748-493">Create new Edge Storage Account</span></span>
* <span data-ttu-id="f1748-494">Hozzá lett adva a Remove-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="f1748-494">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f1748-495">Az Edge Storage-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f1748-495">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="f1748-496">Hozzá lett adva az Invoke-AzDataBoxEdgeShare parancsmag</span><span class="sxs-lookup"><span data-stu-id="f1748-496">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="f1748-497">Meghívási művelet a megosztott adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-497">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="f1748-498">Hozzá lett adva a Set-AzDataBoxEdgeStorageAccountCredential parancsmag</span><span class="sxs-lookup"><span data-stu-id="f1748-498">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="f1748-499">Az Az.DataBoxEdge tárfiók hitelesítő adatainak beállítása</span><span class="sxs-lookup"><span data-stu-id="f1748-499">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1748-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1748-500">Az.DataFactory</span></span>
* <span data-ttu-id="f1748-501">Hozzá lettek adva az AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId és VersionStatus tulajdonságok a Get-AzDataFactoryV2IntegrationRuntime parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-501">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="f1748-502">Az ADF .Net SDK frissítve lett a 4.6.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="f1748-502">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="f1748-503">A PublicIPs paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz statikus nyilvános IP-címekkel rendelkező Azure-SSIS IR létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="f1748-503">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="f1748-504">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="f1748-504">Az.DevTestLabs</span></span>
* <span data-ttu-id="f1748-505">A hibás hivatkozás el lett távolítva a Get-AzDtlAllowedVMSizesPolicy.md parancsmagból</span><span class="sxs-lookup"><span data-stu-id="f1748-505">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f1748-506">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1748-506">Az.EventHub</span></span>
* <span data-ttu-id="f1748-507">A 10634-es hiba javítása: Ki lett javítva a nullértékű objektumhivatkozás a remove eventhubnamespace esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-507">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1748-508">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1748-508">Az.HDInsight</span></span>
* <span data-ttu-id="f1748-509">Ki lett javítva az Invoke-AzHDInsightHiveJob.md hibája.</span><span class="sxs-lookup"><span data-stu-id="f1748-509">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f1748-510">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f1748-510">Az.MachineLearning</span></span>
* <span data-ttu-id="f1748-511">El lettek távolítva az alábbi parancsmagok, mivel a MachineLearningCompute már nem érhető el</span><span class="sxs-lookup"><span data-stu-id="f1748-511">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="f1748-512">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f1748-512">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="f1748-513">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="f1748-513">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="f1748-514">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f1748-514">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="f1748-515">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f1748-515">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="f1748-516">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f1748-516">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="f1748-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="f1748-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="f1748-518">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="f1748-518">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-519">Az.Network</span></span>
* <span data-ttu-id="f1748-520">Frissítve lett a Microsoft.Azure.Management.Sql függősége: 1.36-preview helyett 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="f1748-520">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-521">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-521">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-522">Módosított Azure Site Recovery-támogatás azon felügyelt lemezeken található, inaktív állapotban titkosított virtuális gépeknél, amelyekhez felhasználó által kezelt kulcsok tartoznak a következő esetében: Azure – Azure-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="f1748-522">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="f1748-523">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a védelem engedélyezése során a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="f1748-523">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f1748-524">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a lemez szintjén a védelem engedélyezéséhez a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="f1748-524">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f1748-525">Azure Site Recovery-támogatás a Replikációval védett, lemeztitkosítási csoportleképezéssel ellátott elemek frissítéséhez a következő esetében: HyperV – Azure.</span><span class="sxs-lookup"><span data-stu-id="f1748-525">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-526">Az.Resources</span></span>
* <span data-ttu-id="f1748-527">Javítva lett egy hiba a Remove-AzTag súgódokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="f1748-527">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-528">Az.Sql</span></span>
* <span data-ttu-id="f1748-529">Javítva lett a sebezhetőségi felmérés csoportszintű alapkonfigurációs parancsmagjainak működése: az Azure-adatbázis főadatbázisában használható, a felügyelt példányok rendszeradatbázisaiban korlátozott.</span><span class="sxs-lookup"><span data-stu-id="f1748-529">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="f1748-530">Ki lett javítva egy hiba az SQL-példányok feladatátvételi csoportjainak létrehozása esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-530">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f1748-531">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f1748-531">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f1748-532">Hozzá lett adva a DR, mint új érvényes licenctípus</span><span class="sxs-lookup"><span data-stu-id="f1748-532">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-533">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-533">Az.Storage</span></span>
* <span data-ttu-id="f1748-534">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet a DefaultAction értékének módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="f1748-534">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="f1748-535">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1748-535">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="f1748-536">Támogatott a tárfiók legutóbbi szinkronizálási időpontjának lekérése a get-AzureRMStorageAccount parancsmag -IncludeGeoReplicationStats paraméterrel való futtatásával</span><span class="sxs-lookup"><span data-stu-id="f1748-536">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="f1748-537">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1748-537">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="f1748-538">3.2.0 – 2019. december</span><span class="sxs-lookup"><span data-stu-id="f1748-538">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="f1748-539">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f1748-539">General</span></span>
* <span data-ttu-id="f1748-540">A .psd1 hivatkozásai frissítve, hogy minden modulhoz a relatív elérési utat használják</span><span class="sxs-lookup"><span data-stu-id="f1748-540">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1748-541">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-541">Az.Accounts</span></span>
* <span data-ttu-id="f1748-542">A megfelelő felhasználói ügynök beállítva az ügyféloldali telemetriához az Az 4.0 előzetes verziójában</span><span class="sxs-lookup"><span data-stu-id="f1748-542">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="f1748-543">Felhasználóbarát hibaüzenet megjelenítése, ha az Az 4.0 előzetes verziójában a környezet null értékű</span><span class="sxs-lookup"><span data-stu-id="f1748-543">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f1748-544">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f1748-544">Az.Batch</span></span>
* <span data-ttu-id="f1748-545">Ki lett javítva a [10602-es](https://github.com/Azure/azure-powershell/issues/10602) számú hiba, amely miatt a **New-AzBatchPool** nem megfelelően küldte el a „VirtualMachineConfiguration.ContainerConfiguration” és a „VirtualMachineConfiguration.DataDisks” paramétereket a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="f1748-545">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1748-546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1748-546">Az.DataFactory</span></span>
* <span data-ttu-id="f1748-547">Az ADF .Net SDK a 4.5.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f1748-547">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f1748-548">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1748-548">Az.FrontDoor</span></span>
* <span data-ttu-id="f1748-549">A WAF felügyeleti szabályok kizárása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="f1748-549">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="f1748-550">Hozzá lett adva a SocketAddr automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="f1748-550">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f1748-551">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f1748-551">Az.HealthcareApis</span></span>
* <span data-ttu-id="f1748-552">Kivételkezelés</span><span class="sxs-lookup"><span data-stu-id="f1748-552">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1748-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1748-553">Az.KeyVault</span></span>
* <span data-ttu-id="f1748-554">Ki lett javítva az esetleg nem beállított értékek hozzáférésével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="f1748-554">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="f1748-555">Az elliptikus görbéjű titkosítási tanúsítványok kezelése</span><span class="sxs-lookup"><span data-stu-id="f1748-555">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="f1748-556">A görbe tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="f1748-556">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1748-557">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1748-557">Az.Monitor</span></span>
* <span data-ttu-id="f1748-558">Opcionális argumentum hozzáadva a Diagnosztikai beállítások hozzáadása parancshoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-558">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="f1748-559">Ez egy kapcsoló argumentum, amely megléte esetén azt jelzi, hogy a Log Analyticsbe történő exportálást egy rögzített séma (más néven</span><span class="sxs-lookup"><span data-stu-id="f1748-559">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="f1748-560">dedikált adattípus) szerint kell végrehajtani</span><span class="sxs-lookup"><span data-stu-id="f1748-560">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-561">Az.Network</span></span>
* <span data-ttu-id="f1748-562">Támogatás az Ip-csoportok számára az AzureFirewall alkalmazás, valamint a Nat- és a hálózati szabályok esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-562">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-563">Az.Resources</span></span>
* <span data-ttu-id="f1748-564">Ki lett javítva az a hiba, amely miatt a sablonalapú üzembe helyezés során a sablonparamétert nem lehet olvasni, ha a sablonparaméter és egy beépített paraméter neve között névütközés áll fenn.</span><span class="sxs-lookup"><span data-stu-id="f1748-564">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="f1748-565">Frissültek a szabályzat parancsmagjai a 2019. 09. 01. dátumú új API-verzió használatára, amely bevezeti a szabályzatkészlet-definíciókon belüli csoportos támogatást.</span><span class="sxs-lookup"><span data-stu-id="f1748-565">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-566">Az.Sql</span></span>
* <span data-ttu-id="f1748-567">Frissítve lett a sebezhetőségi felmérés automatikus engedélyezéséhez szükséges tárterület létrehozása a Storagev2-ben</span><span class="sxs-lookup"><span data-stu-id="f1748-567">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-568">Az.Storage</span></span>
* <span data-ttu-id="f1748-569">A blob-/tárolóidentitás-alapú SAS-token Oauth-hitelesítésen alapuló Storage-környezettel való létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="f1748-569">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="f1748-570">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="f1748-570">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="f1748-571">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f1748-571">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="f1748-572">Támogatott lett a tárfiókhoz tartozó felhasználódelegálási kulcsok visszavonása, így minden identitásalapú SAS-token visszavonható</span><span class="sxs-lookup"><span data-stu-id="f1748-572">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="f1748-573">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="f1748-573">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="f1748-574">Frissítés a Microsoft.Azure.Management.Storage 14.2.0-s verziójára az új API-verzió (2019. 06. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f1748-574">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="f1748-575">A QuotaGiB (gigabájtban megadott megosztási kvóta) esetében támogatottak az 5120-nál nagyobb értékek a fájlmegosztási parancsmagok felügyeleti síkján, és hozzá lett adva a Quota paraméteralias a QuotaGiB paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-575">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="f1748-576">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1748-576">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="f1748-577">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1748-577">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="f1748-578">A „QuotaGiB” paraméteralias hozzáadva a „kvóta” paraméterhez</span><span class="sxs-lookup"><span data-stu-id="f1748-578">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="f1748-579">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="f1748-579">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="f1748-580">Ki lett javítva az a hiba, amely miatt a Set-AzStorageContainerAcl parancsmag el tudta távolítani a tárolt hozzáférési szabályzatot</span><span class="sxs-lookup"><span data-stu-id="f1748-580">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="f1748-581">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="f1748-581">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="f1748-582">3.1.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="f1748-582">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f1748-583">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="f1748-583">Highlights since the last major release</span></span>
* <span data-ttu-id="f1748-584">Az.DataBoxEdge 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="f1748-584">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="f1748-585">Az.SqlVirtualMachine 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="f1748-585">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-586">Az.Compute</span></span>
* <span data-ttu-id="f1748-587">A virtuális gépek Reapply funkciója</span><span class="sxs-lookup"><span data-stu-id="f1748-587">VM Reapply feature</span></span>
    - <span data-ttu-id="f1748-588">A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-588">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="f1748-589">A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:</span><span class="sxs-lookup"><span data-stu-id="f1748-589">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="f1748-590">Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1748-590">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="f1748-591">Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-591">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="f1748-592">A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez</span><span class="sxs-lookup"><span data-stu-id="f1748-592">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f1748-593">A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-593">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="f1748-594">A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező</span><span class="sxs-lookup"><span data-stu-id="f1748-594">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="f1748-595">A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="f1748-595">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="f1748-596">A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f1748-596">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="f1748-597">A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-597">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f1748-598">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f1748-598">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f1748-599">A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f1748-599">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f1748-600">Megrendelés lekérése</span><span class="sxs-lookup"><span data-stu-id="f1748-600">Get the Order</span></span>
* <span data-ttu-id="f1748-601">A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f1748-601">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f1748-602">Új megrendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="f1748-602">Create new Order</span></span>
* <span data-ttu-id="f1748-603">A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f1748-603">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f1748-604">Megrendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f1748-604">Remove the Order</span></span>
* <span data-ttu-id="f1748-605">`New-AzDataBoxEdgeShare` parancsmag módosítása</span><span class="sxs-lookup"><span data-stu-id="f1748-605">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="f1748-606">Mostantól helyi megosztást hoz létre</span><span class="sxs-lookup"><span data-stu-id="f1748-606">Now creates Local Share</span></span>
* <span data-ttu-id="f1748-607">A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f1748-607">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="f1748-608">Mostantól az IotRole leképezhető a Share-re</span><span class="sxs-lookup"><span data-stu-id="f1748-608">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="f1748-609">A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f1748-609">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="f1748-610">Frissítések keresésének, letöltésének, telepítésének indítása az eszközön</span><span class="sxs-lookup"><span data-stu-id="f1748-610">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="f1748-611">A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f1748-611">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f1748-612">Triggerek információinak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="f1748-612">Gets the information about Triggers</span></span>
* <span data-ttu-id="f1748-613">A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f1748-613">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f1748-614">Új triggerek létrehozása</span><span class="sxs-lookup"><span data-stu-id="f1748-614">Create new Triggers</span></span>
* <span data-ttu-id="f1748-615">A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f1748-615">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f1748-616">Triggerek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f1748-616">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1748-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1748-617">Az.DataFactory</span></span>
* <span data-ttu-id="f1748-618">Az ADF .Net SDK a 4.4.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f1748-618">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="f1748-619">Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-619">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1748-620">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1748-620">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1748-621">Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f1748-621">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f1748-622">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1748-622">Az.EventHub</span></span>
* <span data-ttu-id="f1748-623">A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása</span><span class="sxs-lookup"><span data-stu-id="f1748-623">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f1748-624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1748-624">Az.FrontDoor</span></span>
* <span data-ttu-id="f1748-625">Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="f1748-625">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="f1748-626">A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="f1748-626">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="f1748-627">Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához</span><span class="sxs-lookup"><span data-stu-id="f1748-627">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="f1748-628">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="f1748-628">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-629">Az.Network</span></span>
* <span data-ttu-id="f1748-630">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.</span><span class="sxs-lookup"><span data-stu-id="f1748-630">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="f1748-631">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="f1748-631">Az.PrivateDns</span></span>
* <span data-ttu-id="f1748-632">A PrivateDns .net sdk frissült az 1.0.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="f1748-632">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-633">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-633">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-634">Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="f1748-634">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="f1748-635">Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-635">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="f1748-636">SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="f1748-636">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f1748-637">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f1748-637">Az.RedisCache</span></span>
* <span data-ttu-id="f1748-638">A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="f1748-638">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="f1748-639">Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-639">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="f1748-640">Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-640">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-641">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-641">Az.Resources</span></span>
- <span data-ttu-id="f1748-642">Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.</span><span class="sxs-lookup"><span data-stu-id="f1748-642">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="f1748-643">Frissült a létrehozási szabályzat definíciójának súgóbeli példája</span><span class="sxs-lookup"><span data-stu-id="f1748-643">Updated create policy definition help example</span></span>
- <span data-ttu-id="f1748-644">Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.</span><span class="sxs-lookup"><span data-stu-id="f1748-644">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="f1748-645">Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.</span><span class="sxs-lookup"><span data-stu-id="f1748-645">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="f1748-646">A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="f1748-646">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-647">Az.Sql</span></span>
* <span data-ttu-id="f1748-648">Az adatbázisbeli ReadReplicaCount mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f1748-648">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="f1748-649">A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén</span><span class="sxs-lookup"><span data-stu-id="f1748-649">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="f1748-650">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="f1748-650">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="f1748-651">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f1748-651">General</span></span>
* <span data-ttu-id="f1748-652">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f1748-652">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1748-653">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-653">Az.Accounts</span></span>
* <span data-ttu-id="f1748-654">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="f1748-654">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f1748-655">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f1748-655">Az.Advisor</span></span>
* <span data-ttu-id="f1748-656">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-656">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f1748-657">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f1748-657">Az.Batch</span></span>
* <span data-ttu-id="f1748-658">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="f1748-658">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="f1748-659">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="f1748-659">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="f1748-660">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="f1748-660">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="f1748-661">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="f1748-661">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="f1748-662">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-662">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="f1748-663">Ezek az **New-AzBatchTask**`-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="f1748-663">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="f1748-664">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="f1748-664">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="f1748-665">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="f1748-665">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="f1748-666">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="f1748-666">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="f1748-667">A `PSApplication`**Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-667">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f1748-668">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="f1748-668">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="f1748-669">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="f1748-669">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="f1748-670">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-670">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f1748-671">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="f1748-671">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="f1748-672">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="f1748-672">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="f1748-673">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-673">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="f1748-674">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-674">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="f1748-675">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f1748-675">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="f1748-676">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-676">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="f1748-677">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="f1748-677">This operation is no longer supported.</span></span>
* <span data-ttu-id="f1748-678">`PSCloudServiceConfiguration``TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-678">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f1748-679">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-679">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f1748-680">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="f1748-680">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="f1748-681">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="f1748-681">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="f1748-682">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="f1748-682">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="f1748-683">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="f1748-683">New non-verified images are also now returned.</span></span> <span data-ttu-id="f1748-684">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="f1748-684">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="f1748-685">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="f1748-685">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="f1748-686">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="f1748-686">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="f1748-687">Ez a `PSNetworkSecurityGroupRule``SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="f1748-687">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="f1748-688">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="f1748-688">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="f1748-689">Ezt a `PSTaskContainerSettings``WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="f1748-689">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="f1748-690">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="f1748-690">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="f1748-691">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="f1748-691">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="f1748-692">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="f1748-692">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="f1748-693">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="f1748-693">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f1748-694">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1748-694">Az.Cdn</span></span>
* <span data-ttu-id="f1748-695">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="f1748-695">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="f1748-696">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="f1748-696">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-697">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-697">Az.Compute</span></span>
* <span data-ttu-id="f1748-698">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="f1748-698">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="f1748-699">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f1748-699">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="f1748-700">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f1748-700">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="f1748-701">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-701">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f1748-702">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-702">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="f1748-703">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="f1748-703">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="f1748-704">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-704">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="f1748-705">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="f1748-705">Breaking changes</span></span>
    - <span data-ttu-id="f1748-706">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="f1748-706">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="f1748-707">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="f1748-707">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1748-708">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1748-708">Az.DataFactory</span></span>
* <span data-ttu-id="f1748-709">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f1748-709">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1748-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1748-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1748-711">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="f1748-711">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="f1748-712">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="f1748-712">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="f1748-713">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="f1748-713">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="f1748-714">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="f1748-714">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="f1748-715">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-715">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="f1748-716">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="f1748-716">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f1748-717">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1748-717">Az.FrontDoor</span></span>
* <span data-ttu-id="f1748-718">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="f1748-718">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1748-719">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1748-719">Az.HDInsight</span></span>
* <span data-ttu-id="f1748-720">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-720">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="f1748-721">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-721">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="f1748-722">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="f1748-722">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="f1748-723">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="f1748-723">Removed five cmdlets:</span></span>
    - <span data-ttu-id="f1748-724">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f1748-724">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f1748-725">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f1748-725">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f1748-726">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f1748-726">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f1748-727">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f1748-727">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="f1748-728">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f1748-728">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="f1748-729">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="f1748-729">Added three cmdlets:</span></span>
    - <span data-ttu-id="f1748-730">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="f1748-730">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f1748-731">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="f1748-731">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f1748-732">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="f1748-732">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="f1748-733">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="f1748-733">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="f1748-734">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="f1748-734">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="f1748-735">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="f1748-735">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="f1748-736">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="f1748-736">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="f1748-737">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="f1748-737">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="f1748-738">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="f1748-738">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="f1748-739">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="f1748-739">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="f1748-740">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f1748-740">Added some scenario test cases.</span></span>
* <span data-ttu-id="f1748-741">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="f1748-741">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1748-742">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1748-742">Az.IotHub</span></span>
* <span data-ttu-id="f1748-743">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="f1748-743">Breaking changes:</span></span>
    - <span data-ttu-id="f1748-744">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-744">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f1748-745">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-745">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f1748-746">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-746">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f1748-747">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-747">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f1748-748">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-748">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="f1748-749">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-749">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="f1748-750">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="f1748-750">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="f1748-751">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="f1748-751">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="f1748-752">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-752">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f1748-753">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-753">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f1748-754">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-754">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f1748-755">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-755">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-756">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-756">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-757">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="f1748-757">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="f1748-758">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="f1748-758">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="f1748-759">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="f1748-759">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="f1748-760">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="f1748-760">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="f1748-761">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="f1748-761">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="f1748-762">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="f1748-762">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="f1748-763">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="f1748-763">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="f1748-764">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="f1748-764">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="f1748-765">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="f1748-765">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-766">Az.Resources</span></span>
* <span data-ttu-id="f1748-767">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="f1748-767">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-768">Az.Network</span></span>
* <span data-ttu-id="f1748-769">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f1748-769">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="f1748-770">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="f1748-770">Updated cmdlet:</span></span>
        - <span data-ttu-id="f1748-771">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-771">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1748-772">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-772">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1748-773">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-773">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1748-774">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-774">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1748-775">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-775">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f1748-776">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="f1748-776">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="f1748-777">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="f1748-777">New cmdlet:</span></span>
        - <span data-ttu-id="f1748-778">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="f1748-778">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="f1748-779">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-779">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="f1748-780">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="f1748-780">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="f1748-781">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="f1748-781">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="f1748-782">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="f1748-782">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="f1748-783">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="f1748-783">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="f1748-784">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="f1748-784">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="f1748-785">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-785">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="f1748-786">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f1748-786">New cmdlets added:</span></span>
        - <span data-ttu-id="f1748-787">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="f1748-787">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="f1748-788">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1748-788">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f1748-789">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1748-789">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f1748-790">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1748-790">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f1748-791">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f1748-791">Set-AzVirtualHub</span></span>
* <span data-ttu-id="f1748-792">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-792">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="f1748-793">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f1748-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f1748-794">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-794">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f1748-795">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-795">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f1748-796">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-796">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="f1748-797">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-797">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="f1748-798">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-798">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="f1748-799">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f1748-799">New cmdlets added:</span></span>
        - <span data-ttu-id="f1748-800">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-800">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="f1748-801">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f1748-801">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f1748-802">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-802">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f1748-803">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-803">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f1748-804">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-804">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f1748-805">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-805">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f1748-806">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-806">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="f1748-807">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-807">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="f1748-808">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f1748-808">New cmdlets added:</span></span>
        - <span data-ttu-id="f1748-809">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="f1748-809">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="f1748-810">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="f1748-810">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="f1748-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f1748-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="f1748-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="f1748-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="f1748-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="f1748-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="f1748-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1748-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="f1748-815">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f1748-815">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f1748-816">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-816">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="f1748-817">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-817">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="f1748-818">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="f1748-818">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="f1748-819">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-819">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="f1748-820">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f1748-820">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f1748-821">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-821">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="f1748-822">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-822">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="f1748-823">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="f1748-823">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="f1748-824">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="f1748-824">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="f1748-825">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-825">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="f1748-826">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f1748-826">New cmdlets added:</span></span>
        - <span data-ttu-id="f1748-827">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f1748-827">New-AzIpGroup</span></span>
        - <span data-ttu-id="f1748-828">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f1748-828">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="f1748-829">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f1748-829">Get-AzIpGroup</span></span>
        - <span data-ttu-id="f1748-830">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f1748-830">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1748-831">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1748-831">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1748-832">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="f1748-832">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-833">Az.Sql</span></span>
* <span data-ttu-id="f1748-834">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="f1748-834">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="f1748-835">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="f1748-835">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="f1748-836">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="f1748-836">Removed deprecated aliases:</span></span>
* <span data-ttu-id="f1748-837">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="f1748-837">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="f1748-838">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="f1748-838">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="f1748-839">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="f1748-839">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f1748-840">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="f1748-840">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="f1748-841">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="f1748-841">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="f1748-842">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="f1748-842">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-843">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-843">Az.Storage</span></span>
* <span data-ttu-id="f1748-844">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="f1748-844">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="f1748-845">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1748-845">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f1748-846">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1748-846">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f1748-847">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="f1748-847">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="f1748-848">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f1748-848">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="f1748-849">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f1748-849">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="f1748-850">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="f1748-850">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="f1748-851">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f1748-851">General</span></span>
* <span data-ttu-id="f1748-852">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="f1748-852">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1748-853">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-853">Az.Accounts</span></span>
* <span data-ttu-id="f1748-854">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="f1748-854">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f1748-855">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1748-855">Az.ApiManagement</span></span>
* <span data-ttu-id="f1748-856">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f1748-856">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="f1748-857">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="f1748-857">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1748-858">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1748-858">Az.Automation</span></span>
* <span data-ttu-id="f1748-859">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="f1748-859">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f1748-860">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f1748-860">Az.Batch</span></span>
* <span data-ttu-id="f1748-861">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="f1748-861">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-862">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-862">Az.Compute</span></span>
* <span data-ttu-id="f1748-863">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-863">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f1748-864">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="f1748-864">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="f1748-865">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="f1748-865">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="f1748-866">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="f1748-866">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1748-867">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1748-867">Az.DataFactory</span></span>
* <span data-ttu-id="f1748-868">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="f1748-868">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="f1748-869">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="f1748-869">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="f1748-870">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f1748-870">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1748-871">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1748-871">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1748-872">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="f1748-872">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f1748-873">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f1748-873">Az.HealthcareApis</span></span>
* <span data-ttu-id="f1748-874">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f1748-874">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="f1748-875">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f1748-875">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="f1748-876">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="f1748-876">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="f1748-877">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="f1748-877">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1748-878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1748-878">Az.IotHub</span></span>
* <span data-ttu-id="f1748-879">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="f1748-879">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="f1748-880">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1748-880">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1748-881">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1748-881">Az.Monitor</span></span>
* <span data-ttu-id="f1748-882">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="f1748-882">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="f1748-883">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="f1748-883">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="f1748-884">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="f1748-884">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="f1748-885">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="f1748-885">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-886">Az.Network</span></span>
* <span data-ttu-id="f1748-887">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="f1748-887">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="f1748-888">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="f1748-888">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="f1748-889">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f1748-889">New cmdlets added:</span></span>
        - <span data-ttu-id="f1748-890">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="f1748-890">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="f1748-891">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-891">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f1748-892">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="f1748-892">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="f1748-893">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f1748-893">Updated cmdlets:</span></span>
        - <span data-ttu-id="f1748-894">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-894">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f1748-895">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-895">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f1748-896">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-896">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f1748-897">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="f1748-897">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="f1748-898">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="f1748-898">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="f1748-899">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="f1748-899">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="f1748-900">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="f1748-900">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f1748-901">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f1748-901">Az.RedisCache</span></span>
* <span data-ttu-id="f1748-902">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="f1748-902">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-903">Az.Sql</span></span>
* <span data-ttu-id="f1748-904">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="f1748-904">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-905">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-905">Az.Storage</span></span>
* <span data-ttu-id="f1748-906">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="f1748-906">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="f1748-907">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="f1748-907">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f1748-908">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f1748-908">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="f1748-909">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="f1748-909">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f1748-910">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1748-910">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f1748-911">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f1748-911">Az.StorageSync</span></span>
* <span data-ttu-id="f1748-912">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="f1748-912">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-913">Az.Websites</span></span>
* <span data-ttu-id="f1748-914">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="f1748-914">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="f1748-915">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="f1748-915">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f1748-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1748-916">Az.ApiManagement</span></span>
* <span data-ttu-id="f1748-917">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="f1748-917">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="f1748-918">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="f1748-918">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="f1748-919">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="f1748-919">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1748-920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1748-920">Az.Automation</span></span>
* <span data-ttu-id="f1748-921">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="f1748-921">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="f1748-922">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-922">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="f1748-923">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="f1748-923">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-924">Az.Compute</span></span>
* <span data-ttu-id="f1748-925">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-925">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="f1748-926">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-926">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f1748-927">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="f1748-927">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="f1748-928">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-928">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="f1748-929">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-929">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="f1748-930">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="f1748-930">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="f1748-931">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="f1748-931">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="f1748-932">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-932">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="f1748-933">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-933">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1748-934">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1748-934">Az.DataFactory</span></span>
* <span data-ttu-id="f1748-935">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="f1748-935">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="f1748-936">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f1748-936">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1748-937">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1748-937">Az.HDInsight</span></span>
* <span data-ttu-id="f1748-938">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="f1748-938">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1748-939">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1748-939">Az.IotHub</span></span>
* <span data-ttu-id="f1748-940">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="f1748-940">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="f1748-941">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="f1748-941">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="f1748-942">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f1748-942">New cmdlets are:</span></span>
    - <span data-ttu-id="f1748-943">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f1748-943">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f1748-944">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f1748-944">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f1748-945">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f1748-945">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f1748-946">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f1748-946">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1748-947">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1748-947">Az.Monitor</span></span>
* <span data-ttu-id="f1748-948">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="f1748-948">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="f1748-949">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="f1748-949">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="f1748-950">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="f1748-950">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="f1748-951">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="f1748-951">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="f1748-952">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-952">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="f1748-953">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="f1748-953">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="f1748-954">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="f1748-954">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="f1748-955">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="f1748-955">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="f1748-956">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="f1748-956">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f1748-957">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="f1748-957">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="f1748-958">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="f1748-958">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f1748-959">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="f1748-959">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="f1748-960">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-960">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="f1748-961">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="f1748-961">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="f1748-962">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="f1748-962">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="f1748-963">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="f1748-963">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="f1748-964">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="f1748-964">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="f1748-965">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="f1748-965">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="f1748-966">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="f1748-966">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="f1748-967">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="f1748-967">Overall improved help files</span></span>
* <span data-ttu-id="f1748-968">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="f1748-968">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-969">Az.Network</span></span>
* <span data-ttu-id="f1748-970">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="f1748-970">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="f1748-971">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="f1748-971">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="f1748-972">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="f1748-972">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="f1748-973">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="f1748-973">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="f1748-974">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="f1748-974">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="f1748-975">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="f1748-975">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="f1748-976">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="f1748-976">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="f1748-977">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-977">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="f1748-978">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-978">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="f1748-979">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="f1748-979">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="f1748-980">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="f1748-980">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="f1748-981">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="f1748-981">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="f1748-982">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1748-982">New cmdlets</span></span>
        - <span data-ttu-id="f1748-983">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="f1748-983">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="f1748-984">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-984">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="f1748-985">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="f1748-985">Updated cmdlet:</span></span>
        - <span data-ttu-id="f1748-986">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f1748-986">New-VpnSite</span></span>
        - <span data-ttu-id="f1748-987">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f1748-987">Update-VpnSite</span></span>
        - <span data-ttu-id="f1748-988">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-988">New-VpnConnection</span></span>
        - <span data-ttu-id="f1748-989">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-989">Update-VpnConnection</span></span>
* <span data-ttu-id="f1748-990">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="f1748-990">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-992">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="f1748-992">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="f1748-993">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="f1748-993">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-994">Az.Resources</span></span>
* <span data-ttu-id="f1748-995">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="f1748-995">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1748-996">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1748-996">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1748-997">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="f1748-997">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="f1748-998">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="f1748-998">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="f1748-999">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f1748-999">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f1748-1000">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f1748-1000">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f1748-1001">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f1748-1001">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f1748-1002">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f1748-1002">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="f1748-1003">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f1748-1003">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f1748-1004">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f1748-1004">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f1748-1005">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f1748-1005">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f1748-1006">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f1748-1006">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f1748-1007">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f1748-1007">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="f1748-1008">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f1748-1008">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f1748-1009">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f1748-1009">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f1748-1010">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f1748-1010">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f1748-1011">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="f1748-1011">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="f1748-1012">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="f1748-1012">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f1748-1013">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f1748-1013">Az.SignalR</span></span>
* <span data-ttu-id="f1748-1014">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1748-1014">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-1015">Az.Sql</span></span>
* <span data-ttu-id="f1748-1016">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="f1748-1016">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="f1748-1017">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="f1748-1017">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="f1748-1018">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f1748-1018">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="f1748-1019">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="f1748-1019">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="f1748-1020">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="f1748-1020">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-1021">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-1021">Az.Storage</span></span>
* <span data-ttu-id="f1748-1022">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="f1748-1022">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="f1748-1023">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1023">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="f1748-1024">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f1748-1024">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="f1748-1025">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f1748-1025">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="f1748-1026">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-1026">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="f1748-1027">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f1748-1027">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="f1748-1028">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="f1748-1028">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="f1748-1029">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1748-1029">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f1748-1030">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1748-1030">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f1748-1031">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1748-1031">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f1748-1032">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1748-1032">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-1033">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-1033">Az.Websites</span></span>
* <span data-ttu-id="f1748-1034">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="f1748-1034">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="f1748-1035">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="f1748-1035">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="f1748-1036">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="f1748-1036">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="f1748-1037">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="f1748-1037">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="f1748-1038">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f1748-1038">General</span></span>
* <span data-ttu-id="f1748-1039">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="f1748-1039">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1748-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-1040">Az.Accounts</span></span>
* <span data-ttu-id="f1748-1041">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="f1748-1041">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="f1748-1042">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f1748-1042">Az.Aks</span></span>
* <span data-ttu-id="f1748-1043">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="f1748-1043">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="f1748-1044">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="f1748-1044">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f1748-1045">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1748-1045">Az.ApiManagement</span></span>
* <span data-ttu-id="f1748-1046">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="f1748-1046">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="f1748-1047">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="f1748-1047">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="f1748-1048">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f1748-1048">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="f1748-1049">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="f1748-1049">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="f1748-1050">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="f1748-1050">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f1748-1051">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f1748-1051">Az.Batch</span></span>
* <span data-ttu-id="f1748-1052">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="f1748-1052">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f1748-1053">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1748-1053">Az.Cdn</span></span>
* <span data-ttu-id="f1748-1054">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="f1748-1054">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-1055">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-1055">Az.Compute</span></span>
* <span data-ttu-id="f1748-1056">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1056">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="f1748-1057">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1057">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="f1748-1058">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1058">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="f1748-1059">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="f1748-1059">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="f1748-1060">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="f1748-1060">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="f1748-1061">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1061">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="f1748-1062">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="f1748-1062">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="f1748-1063">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="f1748-1063">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1748-1064">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1748-1064">Az.DataFactory</span></span>
* <span data-ttu-id="f1748-1065">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="f1748-1065">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="f1748-1066">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f1748-1066">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="f1748-1067">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="f1748-1067">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="f1748-1068">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="f1748-1068">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1748-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1748-1069">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1748-1070">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="f1748-1070">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f1748-1071">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1748-1071">Az.EventHub</span></span>
* <span data-ttu-id="f1748-1072">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f1748-1072">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="f1748-1073">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="f1748-1073">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="f1748-1074">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1074">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="f1748-1075">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="f1748-1075">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="f1748-1076">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f1748-1076">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f1748-1077">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="f1748-1077">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1748-1078">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1748-1078">Az.Monitor</span></span>
* <span data-ttu-id="f1748-1079">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="f1748-1079">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-1080">Az.Network</span></span>
* <span data-ttu-id="f1748-1081">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-1081">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="f1748-1082">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="f1748-1082">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="f1748-1083">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="f1748-1083">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="f1748-1084">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="f1748-1084">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="f1748-1085">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1085">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="f1748-1086">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="f1748-1086">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="f1748-1087">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="f1748-1087">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1748-1088">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1748-1088">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1748-1089">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f1748-1089">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="f1748-1090">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-1090">Added example</span></span>
    - <span data-ttu-id="f1748-1091">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="f1748-1091">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="f1748-1092">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1092">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="f1748-1093">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="f1748-1093">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-1094">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1094">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-1095">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="f1748-1095">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-1096">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-1096">Az.Resources</span></span>
* <span data-ttu-id="f1748-1097">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="f1748-1097">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="f1748-1098">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1098">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="f1748-1099">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="f1748-1099">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="f1748-1100">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1100">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f1748-1101">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f1748-1101">Az.ServiceBus</span></span>
* <span data-ttu-id="f1748-1102">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f1748-1102">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="f1748-1103">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="f1748-1103">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="f1748-1104">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="f1748-1104">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1748-1105">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1748-1105">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1748-1106">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="f1748-1106">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="f1748-1107">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="f1748-1107">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="f1748-1108">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="f1748-1108">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="f1748-1109">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="f1748-1109">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="f1748-1110">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="f1748-1110">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="f1748-1111">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="f1748-1111">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-1112">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-1112">Az.Sql</span></span>
* <span data-ttu-id="f1748-1113">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="f1748-1113">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-1114">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-1114">Az.Storage</span></span>
* <span data-ttu-id="f1748-1115">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="f1748-1115">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="f1748-1116">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1116">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="f1748-1117">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f1748-1117">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="f1748-1118">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f1748-1118">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="f1748-1119">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="f1748-1119">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="f1748-1120">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f1748-1120">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-1121">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-1121">Az.Websites</span></span>
* <span data-ttu-id="f1748-1122">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1122">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="f1748-1123">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="f1748-1123">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1748-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-1124">Az.Accounts</span></span>
* <span data-ttu-id="f1748-1125">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="f1748-1125">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="f1748-1126">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f1748-1126">Az.ApplicationInsights</span></span>
* <span data-ttu-id="f1748-1127">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1127">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1748-1128">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1748-1128">Az.Automation</span></span>
* <span data-ttu-id="f1748-1129">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1129">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1748-1130">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1130">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1748-1131">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f1748-1131">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-1132">Az.Compute</span></span>
* <span data-ttu-id="f1748-1133">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="f1748-1133">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f1748-1134">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f1748-1134">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f1748-1135">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1135">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="f1748-1136">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="f1748-1136">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1748-1137">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1748-1137">Az.DataFactory</span></span>
* <span data-ttu-id="f1748-1138">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f1748-1138">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="f1748-1139">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1139">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f1748-1140">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1748-1140">Az.EventHub</span></span>
* <span data-ttu-id="f1748-1141">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f1748-1141">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f1748-1142">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="f1748-1142">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1748-1143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1748-1143">Az.KeyVault</span></span>
* <span data-ttu-id="f1748-1144">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="f1748-1144">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f1748-1145">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f1748-1145">Az.LogicApp</span></span>
* <span data-ttu-id="f1748-1146">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="f1748-1146">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="f1748-1147">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="f1748-1147">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="f1748-1148">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1148">Az.ManagedServices</span></span>
* <span data-ttu-id="f1748-1149">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-1149">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-1150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-1150">Az.Network</span></span>
* <span data-ttu-id="f1748-1151">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-1151">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="f1748-1152">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1748-1152">New cmdlets</span></span>
        - <span data-ttu-id="f1748-1153">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1748-1153">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f1748-1154">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f1748-1154">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f1748-1155">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-1155">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1748-1156">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-1156">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1748-1157">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-1157">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1748-1158">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-1158">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f1748-1159">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="f1748-1159">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="f1748-1160">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f1748-1160">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="f1748-1161">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="f1748-1161">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="f1748-1162">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="f1748-1162">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="f1748-1163">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-1163">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="f1748-1164">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-1164">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="f1748-1165">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="f1748-1165">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="f1748-1166">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1166">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="f1748-1167">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1748-1167">Updated cmdlets</span></span>
        - <span data-ttu-id="f1748-1168">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-1168">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f1748-1169">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-1169">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f1748-1170">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-1170">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f1748-1171">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="f1748-1171">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f1748-1172">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="f1748-1172">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="f1748-1173">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="f1748-1173">Updated cmdlet:</span></span>
        - <span data-ttu-id="f1748-1174">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-1174">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f1748-1175">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-1175">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f1748-1176">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-1176">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="f1748-1177">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="f1748-1177">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="f1748-1178">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="f1748-1178">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="f1748-1179">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="f1748-1179">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1748-1180">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1748-1180">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1748-1181">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="f1748-1181">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="f1748-1182">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="f1748-1182">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-1183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1183">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-1184">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1184">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f1748-1185">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1185">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="f1748-1186">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1186">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="f1748-1187">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1187">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f1748-1188">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1188">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="f1748-1189">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1189">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f1748-1190">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1190">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="f1748-1191">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1191">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f1748-1192">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1192">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="f1748-1193">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1193">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-1194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-1194">Az.Resources</span></span>
- <span data-ttu-id="f1748-1195">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1195">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="f1748-1196">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="f1748-1196">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f1748-1197">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f1748-1197">Az.ServiceBus</span></span>
* <span data-ttu-id="f1748-1198">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f1748-1198">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f1748-1199">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="f1748-1199">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-1200">Az.Sql</span></span>
* <span data-ttu-id="f1748-1201">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1201">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="f1748-1202">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1202">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="f1748-1203">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="f1748-1203">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-1204">Az.Storage</span></span>
* <span data-ttu-id="f1748-1205">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="f1748-1205">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f1748-1206">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f1748-1206">Az.StorageSync</span></span>
* <span data-ttu-id="f1748-1207">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="f1748-1207">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="f1748-1208">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="f1748-1208">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-1209">Az.Websites</span></span>
* <span data-ttu-id="f1748-1210">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="f1748-1210">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="f1748-1211">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1211">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="f1748-1212">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1212">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="f1748-1213">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="f1748-1213">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1748-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-1214">Az.Accounts</span></span>
* <span data-ttu-id="f1748-1215">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f1748-1215">Add support for profile cmdlets</span></span>
* <span data-ttu-id="f1748-1216">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f1748-1216">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="f1748-1217">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="f1748-1217">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f1748-1218">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f1748-1218">Az.Advisor</span></span>
* <span data-ttu-id="f1748-1219">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="f1748-1219">GA release of Az.Advisor</span></span>
* <span data-ttu-id="f1748-1220">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="f1748-1220">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f1748-1221">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1748-1221">Az.ApiManagement</span></span>
* <span data-ttu-id="f1748-1222">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="f1748-1222">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="f1748-1223">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f1748-1223">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="f1748-1224">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-1224">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="f1748-1225">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-1225">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="f1748-1226">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="f1748-1226">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="f1748-1227">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f1748-1227">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="f1748-1228">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="f1748-1228">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1748-1229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1748-1229">Az.Automation</span></span>
* <span data-ttu-id="f1748-1230">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="f1748-1230">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-1231">Az.Compute</span></span>
* <span data-ttu-id="f1748-1232">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1232">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1748-1233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1748-1233">Az.DataFactory</span></span>
* <span data-ttu-id="f1748-1234">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f1748-1234">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f1748-1235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f1748-1235">Az.EventGrid</span></span>
* <span data-ttu-id="f1748-1236">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="f1748-1236">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1748-1237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1748-1237">Az.IotHub</span></span>
* <span data-ttu-id="f1748-1238">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f1748-1238">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-1239">Az.Network</span></span>
* <span data-ttu-id="f1748-1240">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1240">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="f1748-1241">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="f1748-1241">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f1748-1242">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f1748-1242">Az.PolicyInsights</span></span>
* <span data-ttu-id="f1748-1243">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f1748-1243">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="f1748-1244">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="f1748-1244">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1748-1245">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1748-1245">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1748-1246">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="f1748-1246">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-1247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1247">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-1248">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1248">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-1249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-1249">Az.Resources</span></span>
    - <span data-ttu-id="f1748-1250">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1250">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="f1748-1251">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1251">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="f1748-1252">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1252">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="f1748-1253">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1253">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f1748-1254">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f1748-1254">Az.ServiceBus</span></span>
* <span data-ttu-id="f1748-1255">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="f1748-1255">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-1256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-1256">Az.Sql</span></span>
* <span data-ttu-id="f1748-1257">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1257">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="f1748-1258">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="f1748-1258">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="f1748-1259">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f1748-1259">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f1748-1260">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f1748-1260">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f1748-1261">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f1748-1261">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f1748-1262">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f1748-1262">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f1748-1263">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f1748-1263">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f1748-1264">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f1748-1264">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="f1748-1265">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="f1748-1265">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-1266">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-1266">Az.Storage</span></span>
* <span data-ttu-id="f1748-1267">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="f1748-1267">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="f1748-1268">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f1748-1268">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="f1748-1269">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="f1748-1269">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="f1748-1270">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="f1748-1270">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="f1748-1271">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="f1748-1271">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="f1748-1272">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1748-1272">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f1748-1273">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1748-1273">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f1748-1274">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="f1748-1274">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="f1748-1275">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f1748-1275">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="f1748-1276">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f1748-1276">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f1748-1277">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f1748-1277">Az.StorageSync</span></span>
* <span data-ttu-id="f1748-1278">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="f1748-1278">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="f1748-1279">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="f1748-1279">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1748-1280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-1280">Az.Accounts</span></span>
* <span data-ttu-id="f1748-1281">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1281">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="f1748-1282">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="f1748-1282">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="f1748-1283">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1283">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="f1748-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f1748-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="f1748-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="f1748-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-1286">Az.Compute</span></span>
* <span data-ttu-id="f1748-1287">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="f1748-1287">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="f1748-1288">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="f1748-1288">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="f1748-1289">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f1748-1289">Az.Dns</span></span>
* <span data-ttu-id="f1748-1290">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="f1748-1290">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f1748-1291">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f1748-1291">Az.EventGrid</span></span>
* <span data-ttu-id="f1748-1292">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="f1748-1292">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="f1748-1293">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f1748-1293">New cmdlets:</span></span>
    - <span data-ttu-id="f1748-1294">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f1748-1294">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f1748-1295">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="f1748-1295">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f1748-1296">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f1748-1296">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f1748-1297">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="f1748-1297">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="f1748-1298">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f1748-1298">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f1748-1299">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="f1748-1299">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f1748-1300">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f1748-1300">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f1748-1301">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-1301">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f1748-1302">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f1748-1302">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f1748-1303">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="f1748-1303">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="f1748-1304">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f1748-1304">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f1748-1305">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f1748-1305">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="f1748-1306">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f1748-1306">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="f1748-1307">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="f1748-1307">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="f1748-1308">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f1748-1308">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f1748-1309">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="f1748-1309">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="f1748-1310">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f1748-1310">Updated cmdlets:</span></span>
    - <span data-ttu-id="f1748-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f1748-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="f1748-1312">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="f1748-1312">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f1748-1313">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="f1748-1313">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f1748-1314">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="f1748-1314">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="f1748-1315">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="f1748-1315">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="f1748-1316">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="f1748-1316">Event subscription expiration date,</span></span>
            - <span data-ttu-id="f1748-1317">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="f1748-1317">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="f1748-1318">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="f1748-1318">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="f1748-1319">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="f1748-1319">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="f1748-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f1748-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="f1748-1321">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f1748-1321">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="f1748-1322">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f1748-1322">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="f1748-1323">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="f1748-1323">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="f1748-1324">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="f1748-1324">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f1748-1325">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1748-1325">Az.FrontDoor</span></span>
* <span data-ttu-id="f1748-1326">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="f1748-1326">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="f1748-1327">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="f1748-1327">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="f1748-1328">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f1748-1328">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="f1748-1329">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="f1748-1329">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-1330">Az.Network</span></span>
* <span data-ttu-id="f1748-1331">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-1331">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="f1748-1332">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1748-1332">New cmdlets</span></span>
        - <span data-ttu-id="f1748-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="f1748-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="f1748-1334">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-1334">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="f1748-1335">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1748-1335">New cmdlets</span></span>
        - <span data-ttu-id="f1748-1336">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f1748-1336">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="f1748-1337">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-1337">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="f1748-1338">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1748-1338">New cmdlets</span></span>
        - <span data-ttu-id="f1748-1339">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f1748-1339">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f1748-1340">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f1748-1340">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f1748-1341">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f1748-1341">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f1748-1342">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-1342">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="f1748-1343">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-1343">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f1748-1344">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-1344">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="f1748-1345">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1748-1345">New cmdlets</span></span>
        - <span data-ttu-id="f1748-1346">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1748-1346">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f1748-1347">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1748-1347">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f1748-1348">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1748-1348">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f1748-1349">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="f1748-1349">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="f1748-1350">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="f1748-1350">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="f1748-1351">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="f1748-1351">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="f1748-1352">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="f1748-1352">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="f1748-1353">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-1353">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="f1748-1354">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-1354">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="f1748-1355">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="f1748-1355">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="f1748-1356">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="f1748-1356">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="f1748-1357">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="f1748-1357">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="f1748-1358">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1358">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="f1748-1359">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="f1748-1359">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="f1748-1360">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1360">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="f1748-1361">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1361">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="f1748-1362">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="f1748-1362">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="f1748-1363">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1363">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="f1748-1364">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="f1748-1364">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f1748-1365">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="f1748-1365">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="f1748-1366">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="f1748-1366">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="f1748-1367">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="f1748-1367">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="f1748-1368">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="f1748-1368">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="f1748-1369">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-1369">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="f1748-1370">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-1370">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f1748-1371">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-1371">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f1748-1372">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-1372">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1748-1373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1748-1373">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1748-1374">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1374">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-1375">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-1375">Az.Resources</span></span>
* <span data-ttu-id="f1748-1376">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="f1748-1376">Support for additional Template Export options</span></span>
    - <span data-ttu-id="f1748-1377">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1377">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f1748-1378">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1378">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f1748-1379">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1379">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1748-1380">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1748-1380">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1748-1381">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="f1748-1381">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-1382">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-1382">Az.Sql</span></span>
* <span data-ttu-id="f1748-1383">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="f1748-1383">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="f1748-1384">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="f1748-1384">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="f1748-1385">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1385">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="f1748-1386">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f1748-1386">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f1748-1387">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f1748-1387">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f1748-1388">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f1748-1388">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f1748-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f1748-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="f1748-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f1748-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-1391">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-1391">Az.Storage</span></span>
* <span data-ttu-id="f1748-1392">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="f1748-1392">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="f1748-1393">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1748-1393">New-AzStorageAccount</span></span>
* <span data-ttu-id="f1748-1394">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="f1748-1394">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="f1748-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f1748-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-1396">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-1396">Az.Websites</span></span>
* <span data-ttu-id="f1748-1397">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="f1748-1397">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="f1748-1398">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1398">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="f1748-1399">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="f1748-1399">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="f1748-1400">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1748-1400">Az.Cdn</span></span>
* <span data-ttu-id="f1748-1401">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="f1748-1401">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-1402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-1402">Az.Compute</span></span>
* <span data-ttu-id="f1748-1403">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="f1748-1403">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="f1748-1404">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f1748-1404">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f1748-1405">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1748-1405">Az.EventHub</span></span>
* <span data-ttu-id="f1748-1406">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="f1748-1406">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="f1748-1407">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="f1748-1407">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-1408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-1408">Az.Network</span></span>
* <span data-ttu-id="f1748-1409">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="f1748-1409">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="f1748-1410">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f1748-1410">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f1748-1411">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f1748-1411">Az.PolicyInsights</span></span>
* <span data-ttu-id="f1748-1412">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f1748-1412">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-1413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1413">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-1414">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="f1748-1414">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f1748-1415">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f1748-1415">Az.ServiceBus</span></span>
* <span data-ttu-id="f1748-1416">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="f1748-1416">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1748-1417">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1748-1417">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1748-1418">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1418">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="f1748-1419">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="f1748-1419">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-1420">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-1420">Az.Sql</span></span>
* <span data-ttu-id="f1748-1421">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f1748-1421">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="f1748-1422">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="f1748-1422">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f1748-1423">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="f1748-1423">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="f1748-1424">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="f1748-1424">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-1425">Az.Websites</span></span>
* <span data-ttu-id="f1748-1426">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="f1748-1426">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="f1748-1427">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="f1748-1427">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f1748-1428">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1748-1428">Az.ApiManagement</span></span>
* <span data-ttu-id="f1748-1429">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="f1748-1429">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="f1748-1430">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="f1748-1430">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="f1748-1431">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="f1748-1431">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="f1748-1432">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="f1748-1432">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="f1748-1433">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-1433">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="f1748-1434">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1434">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="f1748-1435">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="f1748-1435">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="f1748-1436">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="f1748-1436">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="f1748-1437">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1437">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="f1748-1438">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="f1748-1438">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="f1748-1439">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="f1748-1439">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="f1748-1440">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1440">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="f1748-1441">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1441">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="f1748-1442">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1442">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="f1748-1443">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1443">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="f1748-1444">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="f1748-1444">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="f1748-1445">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1445">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="f1748-1446">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1446">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="f1748-1447">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="f1748-1447">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="f1748-1448">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="f1748-1448">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="f1748-1449">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1449">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="f1748-1450">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="f1748-1450">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="f1748-1451">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="f1748-1451">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="f1748-1452">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1452">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="f1748-1453">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="f1748-1453">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="f1748-1454">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="f1748-1454">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="f1748-1455">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="f1748-1455">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="f1748-1456">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="f1748-1456">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="f1748-1457">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="f1748-1457">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="f1748-1458">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="f1748-1458">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="f1748-1459">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1459">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="f1748-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="f1748-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="f1748-1461">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="f1748-1461">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="f1748-1462">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1462">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f1748-1463">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="f1748-1463">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="f1748-1464">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="f1748-1464">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="f1748-1465">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="f1748-1465">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="f1748-1466">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="f1748-1466">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="f1748-1467">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="f1748-1467">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="f1748-1468">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1468">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f1748-1469">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="f1748-1469">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f1748-1470">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="f1748-1470">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f1748-1471">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="f1748-1471">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="f1748-1472">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="f1748-1472">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f1748-1473">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1473">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f1748-1474">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="f1748-1474">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f1748-1475">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="f1748-1475">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f1748-1476">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="f1748-1476">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f1748-1477">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1477">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="f1748-1478">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="f1748-1478">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="f1748-1479">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="f1748-1479">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="f1748-1480">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1480">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="f1748-1481">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="f1748-1481">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="f1748-1482">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1482">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="f1748-1483">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="f1748-1483">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="f1748-1484">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1484">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="f1748-1485">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1485">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f1748-1486">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1486">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f1748-1487">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1487">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f1748-1488">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1488">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f1748-1489">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1489">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f1748-1490">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1490">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f1748-1491">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1491">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f1748-1492">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1492">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f1748-1493">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="f1748-1493">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="f1748-1494">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f1748-1494">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="f1748-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="f1748-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="f1748-1496">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f1748-1496">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="f1748-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="f1748-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="f1748-1498">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f1748-1498">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="f1748-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="f1748-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="f1748-1500">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="f1748-1500">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="f1748-1501">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f1748-1501">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="f1748-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="f1748-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="f1748-1503">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f1748-1503">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="f1748-1504">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f1748-1504">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="f1748-1505">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f1748-1505">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1748-1506">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1748-1506">Az.Automation</span></span>
* <span data-ttu-id="f1748-1507">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1507">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="f1748-1508">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="f1748-1508">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="f1748-1509">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="f1748-1509">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="f1748-1510">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="f1748-1510">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="f1748-1511">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="f1748-1511">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="f1748-1512">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="f1748-1512">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="f1748-1513">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="f1748-1513">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-1514">Az.Compute</span></span>
* <span data-ttu-id="f1748-1515">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1515">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="f1748-1516">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="f1748-1516">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1748-1517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1748-1517">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1748-1518">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="f1748-1518">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1748-1519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1748-1519">Az.Monitor</span></span>
* <span data-ttu-id="f1748-1520">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="f1748-1520">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-1521">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-1521">Az.Network</span></span>
* <span data-ttu-id="f1748-1522">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1522">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="f1748-1523">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="f1748-1523">Updated cmdlet:</span></span>
        - <span data-ttu-id="f1748-1524">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1748-1524">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="f1748-1525">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="f1748-1525">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-1526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-1526">Az.Resources</span></span>
* <span data-ttu-id="f1748-1527">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1527">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-1528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-1528">Az.Sql</span></span>
* <span data-ttu-id="f1748-1529">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="f1748-1529">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="f1748-1530">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="f1748-1530">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1748-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-1531">Az.Accounts</span></span>
* <span data-ttu-id="f1748-1532">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="f1748-1532">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1748-1533">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1533">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1748-1534">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="f1748-1534">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="f1748-1535">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="f1748-1535">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-1536">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-1536">Az.Compute</span></span>
* <span data-ttu-id="f1748-1537">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="f1748-1537">Proximity placement group feature.</span></span>
    - <span data-ttu-id="f1748-1538">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f1748-1538">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="f1748-1539">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-1539">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="f1748-1540">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-1540">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="f1748-1541">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="f1748-1541">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="f1748-1542">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1542">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="f1748-1543">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="f1748-1543">Breaking changes</span></span>
    - <span data-ttu-id="f1748-1544">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="f1748-1544">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="f1748-1545">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="f1748-1545">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f1748-1546">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f1748-1546">Az.DeploymentManager</span></span>
* <span data-ttu-id="f1748-1547">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="f1748-1547">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="f1748-1548">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f1748-1548">Az.Dns</span></span>
* <span data-ttu-id="f1748-1549">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="f1748-1549">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="f1748-1550">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1550">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="f1748-1551">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="f1748-1551">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f1748-1552">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1748-1552">Az.FrontDoor</span></span>
* <span data-ttu-id="f1748-1553">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="f1748-1553">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="f1748-1554">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="f1748-1554">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="f1748-1555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1748-1555">Az.HDInsight</span></span>
* <span data-ttu-id="f1748-1556">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="f1748-1556">Removed two cmdlets:</span></span>
    - <span data-ttu-id="f1748-1557">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f1748-1557">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="f1748-1558">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f1748-1558">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f1748-1559">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="f1748-1559">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f1748-1560">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="f1748-1560">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="f1748-1561">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="f1748-1561">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="f1748-1562">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="f1748-1562">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1748-1563">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1748-1563">Az.Monitor</span></span>
* <span data-ttu-id="f1748-1564">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="f1748-1564">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="f1748-1565">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f1748-1565">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="f1748-1566">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="f1748-1566">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="f1748-1567">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f1748-1567">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="f1748-1568">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="f1748-1568">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="f1748-1569">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f1748-1569">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="f1748-1570">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f1748-1570">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="f1748-1571">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f1748-1571">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f1748-1572">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f1748-1572">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f1748-1573">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f1748-1573">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f1748-1574">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f1748-1574">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f1748-1575">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f1748-1575">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f1748-1576">[További](/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="f1748-1576">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="f1748-1577">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="f1748-1577">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-1578">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-1578">Az.Network</span></span>
* <span data-ttu-id="f1748-1579">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-1579">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="f1748-1580">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1748-1580">New cmdlets</span></span>
        - <span data-ttu-id="f1748-1581">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f1748-1581">New-AzNatGateway</span></span>
        - <span data-ttu-id="f1748-1582">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f1748-1582">Get-AzNatGateway</span></span>
        - <span data-ttu-id="f1748-1583">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f1748-1583">Set-AzNatGateway</span></span>
        - <span data-ttu-id="f1748-1584">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f1748-1584">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="f1748-1585">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1748-1585">Updated cmdlets</span></span>
        - <span data-ttu-id="f1748-1586">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f1748-1586">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="f1748-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f1748-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="f1748-1588">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="f1748-1588">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="f1748-1589">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="f1748-1589">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="f1748-1590">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="f1748-1590">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f1748-1591">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f1748-1591">Az.PolicyInsights</span></span>
* <span data-ttu-id="f1748-1592">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="f1748-1592">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="f1748-1593">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-1593">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="f1748-1594">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="f1748-1594">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-1595">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1595">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-1596">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="f1748-1596">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="f1748-1597">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="f1748-1597">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="f1748-1598">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="f1748-1598">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="f1748-1599">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="f1748-1599">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="f1748-1600">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="f1748-1600">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="f1748-1601">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="f1748-1601">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="f1748-1602">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f1748-1602">Az.Relay</span></span>
* <span data-ttu-id="f1748-1603">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="f1748-1603">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f1748-1604">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f1748-1604">Az.ServiceBus</span></span>
* <span data-ttu-id="f1748-1605">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="f1748-1605">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-1606">Az.Storage</span></span>
* <span data-ttu-id="f1748-1607">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="f1748-1607">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="f1748-1608">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f1748-1608">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="f1748-1609">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="f1748-1609">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="f1748-1610">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1748-1610">New-AzStorageAccount</span></span>
* <span data-ttu-id="f1748-1611">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="f1748-1611">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="f1748-1612">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1748-1612">New-AzStorageAccount</span></span>
    - <span data-ttu-id="f1748-1613">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1748-1613">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="f1748-1614">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1748-1614">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-1615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-1615">Az.Websites</span></span>
* <span data-ttu-id="f1748-1616">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1616">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="f1748-1617">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="f1748-1617">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="f1748-1618">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="f1748-1618">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f1748-1619">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="f1748-1619">Highlights since the last major release</span></span>
* <span data-ttu-id="f1748-1620">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="f1748-1620">General availability of `Az` module</span></span>
* <span data-ttu-id="f1748-1621">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f1748-1621">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f1748-1622">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f1748-1622">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f1748-1623">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1623">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f1748-1624">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1624">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f1748-1625">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1625">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f1748-1626">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1626">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1748-1627">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-1627">Az.Accounts</span></span>
* <span data-ttu-id="f1748-1628">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1628">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f1748-1629">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f1748-1629">Az.Batch</span></span>
* <span data-ttu-id="f1748-1630">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f1748-1631">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1748-1631">Az.Cdn</span></span>
* <span data-ttu-id="f1748-1632">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1632">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1748-1633">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1633">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1748-1634">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1634">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-1635">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-1635">Az.Compute</span></span>
* <span data-ttu-id="f1748-1636">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="f1748-1636">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="f1748-1637">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1637">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f1748-1638">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f1748-1638">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1748-1639">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1748-1639">Az.DataFactory</span></span>
* <span data-ttu-id="f1748-1640">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="f1748-1640">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1748-1641">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1748-1641">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1748-1642">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1642">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f1748-1643">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f1748-1643">Az.EventGrid</span></span>
* <span data-ttu-id="f1748-1644">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="f1748-1644">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f1748-1645">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1748-1645">Az.EventHub</span></span>
* <span data-ttu-id="f1748-1646">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="f1748-1646">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f1748-1647">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f1748-1647">Az.HDInsight</span></span>
* <span data-ttu-id="f1748-1648">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1748-1649">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1748-1649">Az.IotHub</span></span>
* <span data-ttu-id="f1748-1650">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1748-1651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1748-1651">Az.KeyVault</span></span>
* <span data-ttu-id="f1748-1652">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f1748-1653">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f1748-1653">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f1748-1654">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f1748-1654">Az.MachineLearning</span></span>
* <span data-ttu-id="f1748-1655">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1655">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="f1748-1656">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f1748-1656">Az.Media</span></span>
* <span data-ttu-id="f1748-1657">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1657">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1748-1658">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1748-1658">Az.Monitor</span></span>
  * <span data-ttu-id="f1748-1659">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1748-1659">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="f1748-1660">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f1748-1660">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="f1748-1661">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="f1748-1661">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="f1748-1662">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f1748-1662">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f1748-1663">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f1748-1663">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f1748-1664">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f1748-1664">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="f1748-1665">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="f1748-1665">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-1666">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-1666">Az.Network</span></span>
* <span data-ttu-id="f1748-1667">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1667">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f1748-1668">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f1748-1668">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="f1748-1669">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f1748-1669">Az.NotificationHubs</span></span>
* <span data-ttu-id="f1748-1670">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1670">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1748-1671">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1748-1671">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1748-1672">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f1748-1673">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f1748-1673">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f1748-1674">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1674">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-1675">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1675">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-1676">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1676">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f1748-1677">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="f1748-1677">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="f1748-1678">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="f1748-1678">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="f1748-1679">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="f1748-1679">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f1748-1680">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f1748-1680">Az.RedisCache</span></span>
* <span data-ttu-id="f1748-1681">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1681">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-1682">Az.Resources</span></span>
* <span data-ttu-id="f1748-1683">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f1748-1683">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-1684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-1684">Az.Sql</span></span>
* <span data-ttu-id="f1748-1685">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="f1748-1685">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="f1748-1686">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1686">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f1748-1687">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="f1748-1687">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="f1748-1688">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f1748-1688">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="f1748-1689">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="f1748-1689">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="f1748-1690">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="f1748-1690">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="f1748-1691">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f1748-1691">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-1692">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-1692">Az.Websites</span></span>
* <span data-ttu-id="f1748-1693">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="f1748-1693">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="f1748-1694">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f1748-1694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f1748-1695">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="f1748-1695">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="f1748-1696">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="f1748-1696">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="f1748-1697">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="f1748-1697">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f1748-1698">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="f1748-1698">Highlights since the last major release</span></span>
* <span data-ttu-id="f1748-1699">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="f1748-1699">General availability of `Az` module</span></span>
* <span data-ttu-id="f1748-1700">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f1748-1700">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f1748-1701">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f1748-1701">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f1748-1702">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1702">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f1748-1703">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1703">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f1748-1704">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1704">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f1748-1705">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1705">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f1748-1706">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-1706">Az.Accounts</span></span>
* <span data-ttu-id="f1748-1707">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="f1748-1707">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f1748-1708">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1708">Az.AnalysisServices</span></span>
* <span data-ttu-id="f1748-1709">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1709">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="f1748-1710">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1710">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1748-1711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1748-1711">Az.Automation</span></span>
* <span data-ttu-id="f1748-1712">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="f1748-1712">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="f1748-1713">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="f1748-1713">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="f1748-1714">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1714">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-1715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-1715">Az.Compute</span></span>
* <span data-ttu-id="f1748-1716">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1716">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f1748-1717">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="f1748-1717">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f1748-1718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f1748-1718">Az.ContainerInstance</span></span>
* <span data-ttu-id="f1748-1719">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="f1748-1719">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1748-1720">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1748-1720">Az.DataFactory</span></span>
* <span data-ttu-id="f1748-1721">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="f1748-1721">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="f1748-1722">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="f1748-1722">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-1723">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-1723">Az.Resources</span></span>
* <span data-ttu-id="f1748-1724">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="f1748-1724">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="f1748-1725">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1725">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f1748-1726">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="f1748-1726">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="f1748-1727">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f1748-1727">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="f1748-1728">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1728">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="f1748-1729">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f1748-1729">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-1730">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-1730">Az.Sql</span></span>
* <span data-ttu-id="f1748-1731">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="f1748-1731">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-1732">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-1732">Az.Storage</span></span>
* <span data-ttu-id="f1748-1733">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="f1748-1733">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="f1748-1734">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f1748-1734">New-AzStorageContext</span></span>
* <span data-ttu-id="f1748-1735">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="f1748-1735">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="f1748-1736">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f1748-1736">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f1748-1737">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f1748-1737">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f1748-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1748-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="f1748-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1748-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="f1748-1740">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-1740">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="f1748-1741">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f1748-1741">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f1748-1742">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f1748-1742">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f1748-1743">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f1748-1743">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="f1748-1744">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f1748-1744">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="f1748-1745">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="f1748-1745">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f1748-1746">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="f1748-1746">Highlights since the last major release</span></span>
* <span data-ttu-id="f1748-1747">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="f1748-1747">General availability of `Az` module</span></span>
* <span data-ttu-id="f1748-1748">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f1748-1748">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f1748-1749">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f1748-1749">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f1748-1750">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1750">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f1748-1751">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1751">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f1748-1752">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1752">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f1748-1753">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1753">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1748-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1748-1754">Az.Automation</span></span>
* <span data-ttu-id="f1748-1755">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="f1748-1755">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="f1748-1756">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="f1748-1756">Dynamic grouping</span></span>
    * <span data-ttu-id="f1748-1757">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="f1748-1757">Pre-Post script</span></span>
    * <span data-ttu-id="f1748-1758">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="f1748-1758">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-1759">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-1759">Az.Compute</span></span>
* <span data-ttu-id="f1748-1760">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1760">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="f1748-1761">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="f1748-1761">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1748-1762">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1748-1762">Az.KeyVault</span></span>
* <span data-ttu-id="f1748-1763">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1763">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-1764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-1764">Az.Network</span></span>
* <span data-ttu-id="f1748-1765">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1765">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="f1748-1766">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-1766">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-1767">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1767">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-1768">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="f1748-1768">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="f1748-1769">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1769">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-1770">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-1770">Az.Resources</span></span>
* <span data-ttu-id="f1748-1771">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1771">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="f1748-1772">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1772">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-1773">Az.Sql</span></span>
* <span data-ttu-id="f1748-1774">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="f1748-1774">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-1775">Az.Storage</span></span>
* <span data-ttu-id="f1748-1776">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="f1748-1776">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="f1748-1777">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f1748-1777">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f1748-1778">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f1748-1778">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f1748-1779">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f1748-1779">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f1748-1780">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="f1748-1780">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="f1748-1781">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="f1748-1781">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="f1748-1782">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f1748-1782">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-1783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-1783">Az.Websites</span></span>
* <span data-ttu-id="f1748-1784">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="f1748-1784">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="f1748-1785">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="f1748-1785">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1748-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-1786">Az.Accounts</span></span>
* <span data-ttu-id="f1748-1787">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="f1748-1787">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="f1748-1788">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1788">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1748-1789">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1748-1789">Az.Automation</span></span>
* <span data-ttu-id="f1748-1790">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1790">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="f1748-1791">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="f1748-1791">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="f1748-1792">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="f1748-1792">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f1748-1793">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1748-1793">Az.Cdn</span></span>
* <span data-ttu-id="f1748-1794">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="f1748-1794">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-1795">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-1795">Az.Compute</span></span>
* <span data-ttu-id="f1748-1796">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1796">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1748-1797">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1748-1797">Az.DataFactory</span></span>
* <span data-ttu-id="f1748-1798">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="f1748-1798">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f1748-1799">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f1748-1799">Az.LogicApp</span></span>
* <span data-ttu-id="f1748-1800">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="f1748-1800">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-1801">Az.Network</span></span>
* <span data-ttu-id="f1748-1802">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1802">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-1803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1803">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-1804">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f1748-1804">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="f1748-1805">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="f1748-1805">SDK Update</span></span>
* <span data-ttu-id="f1748-1806">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="f1748-1806">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="f1748-1807">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1807">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-1808">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-1808">Az.Resources</span></span>
* <span data-ttu-id="f1748-1809">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1809">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="f1748-1810">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="f1748-1810">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="f1748-1811">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="f1748-1811">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="f1748-1812">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="f1748-1812">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="f1748-1813">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="f1748-1813">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="f1748-1814">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="f1748-1814">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-1815">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-1815">Az.Sql</span></span>
* <span data-ttu-id="f1748-1816">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="f1748-1816">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="f1748-1817">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="f1748-1817">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-1818">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-1818">Az.Storage</span></span>
* <span data-ttu-id="f1748-1819">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1748-1819">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="f1748-1820">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="f1748-1820">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="f1748-1821">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1821">Az.AnalysisServices</span></span>
* <span data-ttu-id="f1748-1822">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="f1748-1822">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1748-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1748-1823">Az.Automation</span></span>
* <span data-ttu-id="f1748-1824">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1824">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="f1748-1825">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1825">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="f1748-1826">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1826">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1748-1827">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1827">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1748-1828">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-1828">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-1829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-1829">Az.Compute</span></span>
* <span data-ttu-id="f1748-1830">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="f1748-1830">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="f1748-1831">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="f1748-1831">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="f1748-1832">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1832">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="f1748-1833">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="f1748-1833">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1748-1834">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1748-1834">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1748-1835">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="f1748-1835">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f1748-1836">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f1748-1836">Az.EventHub</span></span>
* <span data-ttu-id="f1748-1837">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="f1748-1837">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1748-1838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1748-1838">Az.KeyVault</span></span>
* <span data-ttu-id="f1748-1839">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1839">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f1748-1840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f1748-1840">Az.LogicApp</span></span>
* <span data-ttu-id="f1748-1841">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="f1748-1841">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="f1748-1842">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="f1748-1842">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="f1748-1843">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="f1748-1843">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="f1748-1844">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f1748-1844">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f1748-1845">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f1748-1845">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f1748-1846">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f1748-1846">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f1748-1847">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f1748-1847">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="f1748-1848">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="f1748-1848">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="f1748-1849">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1748-1849">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f1748-1850">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1748-1850">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f1748-1851">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1748-1851">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f1748-1852">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1748-1852">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="f1748-1853">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="f1748-1853">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f1748-1854">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1748-1854">Az.Monitor</span></span>
* <span data-ttu-id="f1748-1855">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1855">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-1856">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-1856">Az.Network</span></span>
* <span data-ttu-id="f1748-1857">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="f1748-1857">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f1748-1858">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1748-1858">Az.OperationalInsights</span></span>
* <span data-ttu-id="f1748-1859">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-1859">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="f1748-1860">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f1748-1860">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="f1748-1861">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="f1748-1861">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-1862">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-1862">Az.Resources</span></span>
* <span data-ttu-id="f1748-1863">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f1748-1863">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f1748-1864">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f1748-1864">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="f1748-1865">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="f1748-1865">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="f1748-1866">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="f1748-1866">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-1867">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-1867">Az.Sql</span></span>
* <span data-ttu-id="f1748-1868">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-1868">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="f1748-1869">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="f1748-1869">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-1870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-1870">Az.Websites</span></span>
* <span data-ttu-id="f1748-1871">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="f1748-1871">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="f1748-1872">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="f1748-1872">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1748-1873">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-1873">Az.Accounts</span></span>
* <span data-ttu-id="f1748-1874">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="f1748-1874">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f1748-1875">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1875">Az.AnalysisServices</span></span>
<span data-ttu-id="f1748-1876">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="f1748-1876">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-1877">Az.Compute</span></span>
* <span data-ttu-id="f1748-1878">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="f1748-1878">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="f1748-1879">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="f1748-1879">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="f1748-1880">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="f1748-1880">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-1881">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1881">Az.RecoveryServices</span></span>
<span data-ttu-id="f1748-1882">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="f1748-1882">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-1883">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-1883">Az.Resources</span></span>
* <span data-ttu-id="f1748-1884">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-1884">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="f1748-1885">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f1748-1885">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f1748-1886">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="f1748-1886">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="f1748-1887">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f1748-1887">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-1888">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-1888">Az.Sql</span></span>
* <span data-ttu-id="f1748-1889">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-1889">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="f1748-1890">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="f1748-1890">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="f1748-1891">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="f1748-1891">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="f1748-1892">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="f1748-1892">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1748-1893">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-1893">Az.Accounts</span></span>
* <span data-ttu-id="f1748-1894">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="f1748-1894">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f1748-1895">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1895">Az.AnalysisServices</span></span>
* <span data-ttu-id="f1748-1896">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="f1748-1896">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-1897">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-1897">Az.RecoveryServices</span></span>
* <span data-ttu-id="f1748-1898">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="f1748-1898">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="f1748-1899">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="f1748-1899">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1748-1900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-1900">Az.Accounts</span></span>
* <span data-ttu-id="f1748-1901">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1901">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f1748-1902">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f1748-1902">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f1748-1903">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="f1748-1903">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="f1748-1904">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f1748-1904">Az.Aks</span></span>
* <span data-ttu-id="f1748-1905">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f1748-1905">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f1748-1906">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1748-1906">Az.Automation</span></span>
* <span data-ttu-id="f1748-1907">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="f1748-1907">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="f1748-1908">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f1748-1908">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f1748-1909">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f1748-1909">Az.Cdn</span></span>
* <span data-ttu-id="f1748-1910">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f1748-1910">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-1911">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-1911">Az.Compute</span></span>
* <span data-ttu-id="f1748-1912">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="f1748-1912">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="f1748-1913">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-1913">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="f1748-1914">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-1914">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f1748-1915">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f1748-1915">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f1748-1916">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f1748-1916">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f1748-1917">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f1748-1917">Az.DataFactory</span></span>
* <span data-ttu-id="f1748-1918">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="f1748-1918">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1748-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1748-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1748-1920">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="f1748-1920">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="f1748-1921">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="f1748-1921">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="f1748-1922">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f1748-1922">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1748-1923">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1748-1923">Az.IotHub</span></span>
* <span data-ttu-id="f1748-1924">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-1924">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f1748-1925">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1748-1925">Az.KeyVault</span></span>
* <span data-ttu-id="f1748-1926">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f1748-1926">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-1927">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-1927">Az.Network</span></span>
* <span data-ttu-id="f1748-1928">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f1748-1928">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-1929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-1929">Az.Resources</span></span>
* <span data-ttu-id="f1748-1930">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="f1748-1930">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="f1748-1931">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="f1748-1931">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="f1748-1932">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-1932">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="f1748-1933">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="f1748-1933">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="f1748-1934">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="f1748-1934">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="f1748-1935">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="f1748-1935">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="f1748-1936">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="f1748-1936">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1748-1937">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1748-1937">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1748-1938">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="f1748-1938">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="f1748-1939">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-1939">Fix some error messages.</span></span>
* <span data-ttu-id="f1748-1940">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="f1748-1940">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="f1748-1941">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="f1748-1941">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f1748-1942">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f1748-1942">Az.SignalR</span></span>
* <span data-ttu-id="f1748-1943">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f1748-1943">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-1944">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-1944">Az.Sql</span></span>
* <span data-ttu-id="f1748-1945">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f1748-1945">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f1748-1946">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="f1748-1946">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="f1748-1947">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="f1748-1947">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="f1748-1948">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="f1748-1948">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-1949">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-1949">Az.Storage</span></span>
* <span data-ttu-id="f1748-1950">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f1748-1950">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f1748-1951">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="f1748-1951">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="f1748-1952">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f1748-1952">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="f1748-1953">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f1748-1953">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f1748-1954">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f1748-1954">Az.TrafficManager</span></span>
* <span data-ttu-id="f1748-1955">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f1748-1955">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-1956">Az.Websites</span></span>
* <span data-ttu-id="f1748-1957">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f1748-1957">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f1748-1958">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="f1748-1958">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="f1748-1959">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="f1748-1959">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="f1748-1960">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="f1748-1960">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f1748-1961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-1961">Az.Accounts</span></span>
* <span data-ttu-id="f1748-1962">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="f1748-1962">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-1963">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-1963">Az.Compute</span></span>
* <span data-ttu-id="f1748-1964">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="f1748-1964">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="f1748-1965">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="f1748-1965">Updated the description of ID in help files</span></span>
* <span data-ttu-id="f1748-1966">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="f1748-1966">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1748-1967">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1748-1967">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1748-1968">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="f1748-1968">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="f1748-1969">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="f1748-1969">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f1748-1970">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f1748-1970">Az.EventGrid</span></span>
* <span data-ttu-id="f1748-1971">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="f1748-1971">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="f1748-1972">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="f1748-1972">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="f1748-1973">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="f1748-1973">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f1748-1974">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="f1748-1974">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f1748-1975">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="f1748-1975">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f1748-1976">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="f1748-1976">Dead letter endpoint.</span></span>
    - <span data-ttu-id="f1748-1977">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="f1748-1977">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f1748-1978">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="f1748-1978">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f1748-1979">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="f1748-1979">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f1748-1980">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="f1748-1980">Dead letter endpoint.</span></span>
* <span data-ttu-id="f1748-1981">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="f1748-1981">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="f1748-1982">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="f1748-1982">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f1748-1983">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f1748-1983">Az.IotHub</span></span>
* <span data-ttu-id="f1748-1984">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="f1748-1984">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f1748-1985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f1748-1985">Az.LogicApp</span></span>
* <span data-ttu-id="f1748-1986">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="f1748-1986">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-1987">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-1987">Az.Resources</span></span>
* <span data-ttu-id="f1748-1988">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="f1748-1988">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="f1748-1989">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="f1748-1989">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="f1748-1990">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="f1748-1990">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f1748-1991">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="f1748-1991">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="f1748-1992">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="f1748-1992">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="f1748-1993">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="f1748-1993">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f1748-1994">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f1748-1994">Az.SignalR</span></span>
* <span data-ttu-id="f1748-1995">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="f1748-1995">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-1996">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-1996">Az.Sql</span></span>
* <span data-ttu-id="f1748-1997">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="f1748-1997">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f1748-1998">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-1998">Az.Storage</span></span>
* <span data-ttu-id="f1748-1999">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="f1748-1999">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="f1748-2000">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f1748-2000">New-AzStorageContext</span></span>
* <span data-ttu-id="f1748-2001">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="f1748-2001">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="f1748-2002">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f1748-2002">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-2003">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-2003">Az.Websites</span></span>
* <span data-ttu-id="f1748-2004">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f1748-2004">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f1748-2005">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="f1748-2005">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="f1748-2006">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="f1748-2006">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f1748-2007">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f1748-2007">General</span></span>

- <span data-ttu-id="f1748-2008">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="f1748-2008">General Availability of Az Module</span></span>
- <span data-ttu-id="f1748-2009">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-2009">Online help for each module</span></span>
- <span data-ttu-id="f1748-2010">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="f1748-2010">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f1748-2011">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f1748-2011">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f1748-2012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-2012">Az.Accounts</span></span>
- <span data-ttu-id="f1748-2013">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="f1748-2013">Changed from Az.Profile</span></span>
- <span data-ttu-id="f1748-2014">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-2014">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f1748-2015">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1748-2015">Az.ApiManagement</span></span>
- <span data-ttu-id="f1748-2016">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="f1748-2016">Fixes for #7002</span></span>
- <span data-ttu-id="f1748-2017">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f1748-2017">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f1748-2018">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f1748-2018">Az.Batch</span></span>
- <span data-ttu-id="f1748-2019">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="f1748-2019">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f1748-2020">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="f1748-2020">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f1748-2021">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f1748-2021">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f1748-2022">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f1748-2022">Az.Billing</span></span>
- <span data-ttu-id="f1748-2023">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="f1748-2023">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f1748-2024">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f1748-2024">Az.CognitivServices</span></span>
- <span data-ttu-id="f1748-2025">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="f1748-2025">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f1748-2026">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="f1748-2026">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f1748-2027">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f1748-2027">Az.ContainerInstance</span></span>
- <span data-ttu-id="f1748-2028">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="f1748-2028">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f1748-2029">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f1748-2029">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f1748-2030">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f1748-2030">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f1748-2031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1748-2031">Az.DataLakeStore</span></span>
- <span data-ttu-id="f1748-2032">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f1748-2032">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f1748-2033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f1748-2033">Az.Monitor</span></span>
- <span data-ttu-id="f1748-2034">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f1748-2034">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f1748-2035">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f1748-2035">Az.KeyVault</span></span>
- <span data-ttu-id="f1748-2036">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-2036">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f1748-2037">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f1748-2037">Az.MachineLearning</span></span>
- <span data-ttu-id="f1748-2038">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="f1748-2038">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f1748-2039">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f1748-2039">Az.Media</span></span>
- <span data-ttu-id="f1748-2040">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="f1748-2040">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f1748-2041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-2041">Az.Network</span></span>
<span data-ttu-id="f1748-2042">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f1748-2042">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f1748-2043">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f1748-2043">New cmdlets added:</span></span>
        - <span data-ttu-id="f1748-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1748-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f1748-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1748-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f1748-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1748-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f1748-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1748-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f1748-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1748-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f1748-2049">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f1748-2049">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f1748-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f1748-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f1748-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1748-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f1748-2052">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1748-2052">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f1748-2053">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1748-2053">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f1748-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f1748-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f1748-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f1748-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f1748-2056">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-2056">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f1748-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f1748-2058">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="f1748-2058">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f1748-2059">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f1748-2059">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f1748-2060">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f1748-2060">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f1748-2061">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f1748-2061">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f1748-2062">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f1748-2062">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f1748-2063">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="f1748-2063">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f1748-2064">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f1748-2064">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f1748-2065">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f1748-2065">Az.OperationalInsights</span></span>
- <span data-ttu-id="f1748-2066">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f1748-2066">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f1748-2067">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f1748-2067">Az.Profile</span></span>
- <span data-ttu-id="f1748-2068">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f1748-2068">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-2069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-2069">Az.RecoveryServices</span></span>
- <span data-ttu-id="f1748-2070">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f1748-2070">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f1748-2071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-2071">Az.Resources</span></span>
- <span data-ttu-id="f1748-2072">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f1748-2072">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f1748-2073">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1748-2073">Az.ServiceFabric</span></span>
- <span data-ttu-id="f1748-2074">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="f1748-2074">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f1748-2075">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f1748-2075">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f1748-2076">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f1748-2076">Az.SIgnalR</span></span>
- <span data-ttu-id="f1748-2077">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="f1748-2077">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f1748-2078">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-2078">Az.Sql</span></span>
- <span data-ttu-id="f1748-2079">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="f1748-2079">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f1748-2080">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="f1748-2080">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f1748-2081">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f1748-2081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f1748-2082">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-2082">Az.Storage</span></span>
- <span data-ttu-id="f1748-2083">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f1748-2083">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f1748-2084">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-2084">Az.Websites</span></span>
- <span data-ttu-id="f1748-2085">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f1748-2085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f1748-2086">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="f1748-2086">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f1748-2087">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f1748-2087">General</span></span>

* <span data-ttu-id="f1748-2088">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-2088">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f1748-2089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-2089">Az.Compute</span></span>

* <span data-ttu-id="f1748-2090">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="f1748-2090">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f1748-2091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1748-2091">Az.DataLakeStore</span></span>

* <span data-ttu-id="f1748-2092">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="f1748-2092">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f1748-2093">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f1748-2093">Az.FrontDoor</span></span>

* <span data-ttu-id="f1748-2094">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="f1748-2094">Fixed some broken links</span></span>
    - <span data-ttu-id="f1748-2095">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="f1748-2095">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f1748-2096">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="f1748-2096">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f1748-2097">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f1748-2097">Az.RecoveryServices</span></span>

* <span data-ttu-id="f1748-2098">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="f1748-2098">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f1748-2099">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="f1748-2099">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f1748-2100">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-2100">Az.Resources</span></span>

* <span data-ttu-id="f1748-2101">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="f1748-2101">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f1748-2102">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="f1748-2102">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f1748-2103">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-2103">Az.Sql</span></span>

* <span data-ttu-id="f1748-2104">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="f1748-2104">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f1748-2105">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="f1748-2105">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f1748-2106">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="f1748-2106">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f1748-2107">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-2107">Az.Storage</span></span>

* <span data-ttu-id="f1748-2108">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-2108">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f1748-2109">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="f1748-2109">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f1748-2110">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f1748-2110">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f1748-2111">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="f1748-2111">Support Static Website configuration</span></span>
    - <span data-ttu-id="f1748-2112">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f1748-2112">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f1748-2113">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f1748-2113">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f1748-2114">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-2114">Az.Websites</span></span>

* <span data-ttu-id="f1748-2115">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f1748-2115">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="f1748-2116">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="f1748-2116">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f1748-2117">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="f1748-2117">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f1748-2118">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="f1748-2118">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f1748-2119">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f1748-2119">Az.ApiManagement</span></span>
* <span data-ttu-id="f1748-2120">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="f1748-2120">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f1748-2121">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f1748-2121">Az.Automation</span></span>
* <span data-ttu-id="f1748-2122">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="f1748-2122">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f1748-2123">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f1748-2123">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f1748-2124">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f1748-2124">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f1748-2125">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="f1748-2125">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f1748-2126">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="f1748-2126">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f1748-2127">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-2127">Az.Compute</span></span>
* <span data-ttu-id="f1748-2128">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="f1748-2128">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f1748-2129">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="f1748-2129">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f1748-2130">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f1748-2130">Az.ContainerInstance</span></span>
* <span data-ttu-id="f1748-2131">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="f1748-2131">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f1748-2132">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f1748-2132">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f1748-2133">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="f1748-2133">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f1748-2134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-2134">Az.Network</span></span>
* <span data-ttu-id="f1748-2135">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="f1748-2135">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f1748-2136">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="f1748-2136">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f1748-2137">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="f1748-2137">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="f1748-2138">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="f1748-2138">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f1748-2139">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f1748-2139">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f1748-2140">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="f1748-2140">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f1748-2141">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="f1748-2141">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f1748-2142">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f1748-2142">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f1748-2143">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="f1748-2143">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f1748-2144">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="f1748-2144">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f1748-2145">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f1748-2145">Az.Relay</span></span>
* <span data-ttu-id="f1748-2146">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="f1748-2146">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f1748-2147">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-2147">Az.Resources</span></span>
* <span data-ttu-id="f1748-2148">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="f1748-2148">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f1748-2149">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="f1748-2149">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f1748-2150">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="f1748-2150">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f1748-2151">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1748-2151">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1748-2152">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-2152">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f1748-2153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-2153">Az.Sql</span></span>
* <span data-ttu-id="f1748-2154">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="f1748-2154">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f1748-2155">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f1748-2155">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f1748-2156">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f1748-2156">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f1748-2157">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f1748-2157">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f1748-2158">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f1748-2158">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f1748-2159">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f1748-2159">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f1748-2160">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f1748-2160">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f1748-2161">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f1748-2161">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f1748-2162">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f1748-2162">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f1748-2163">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="f1748-2163">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f1748-2164">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="f1748-2164">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f1748-2165">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="f1748-2165">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f1748-2166">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f1748-2166">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f1748-2167">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f1748-2167">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f1748-2168">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f1748-2168">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f1748-2169">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f1748-2169">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f1748-2170">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="f1748-2170">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f1748-2171">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="f1748-2171">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f1748-2172">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f1748-2172">General</span></span>
* <span data-ttu-id="f1748-2173">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="f1748-2173">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f1748-2174">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f1748-2174">Az.Profile</span></span>
* <span data-ttu-id="f1748-2175">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="f1748-2175">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f1748-2176">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="f1748-2176">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f1748-2177">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="f1748-2177">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f1748-2178">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="f1748-2178">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f1748-2179">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="f1748-2179">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f1748-2180">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="f1748-2180">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f1748-2181">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="f1748-2181">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1748-2182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1748-2182">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1748-2183">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="f1748-2183">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-2184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-2184">Az.Compute</span></span>
* <span data-ttu-id="f1748-2185">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="f1748-2185">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f1748-2186">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="f1748-2186">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f1748-2187">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="f1748-2187">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1748-2188">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1748-2188">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1748-2189">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="f1748-2189">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f1748-2190">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="f1748-2190">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f1748-2191">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f1748-2191">Az.Insights</span></span>
* <span data-ttu-id="f1748-2192">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="f1748-2192">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f1748-2193">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="f1748-2193">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f1748-2194">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="f1748-2194">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f1748-2195">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="f1748-2195">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-2196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-2196">Az.Network</span></span>
* <span data-ttu-id="f1748-2197">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="f1748-2197">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f1748-2198">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1748-2198">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f1748-2199">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f1748-2199">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f1748-2200">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f1748-2200">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f1748-2201">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f1748-2201">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f1748-2202">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f1748-2202">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f1748-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f1748-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f1748-2204">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f1748-2204">Az.PolicyInsights</span></span>
* <span data-ttu-id="f1748-2205">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-2205">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-2206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-2206">Az.Resources</span></span>
* <span data-ttu-id="f1748-2207">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="f1748-2207">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f1748-2208">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="f1748-2208">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f1748-2209">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f1748-2209">Az.ServiceBus</span></span>
* <span data-ttu-id="f1748-2210">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="f1748-2210">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f1748-2211">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f1748-2211">Az.ServiceFabric</span></span>
* <span data-ttu-id="f1748-2212">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="f1748-2212">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f1748-2213">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="f1748-2213">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f1748-2214">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="f1748-2214">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f1748-2215">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="f1748-2215">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f1748-2216">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="f1748-2216">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f1748-2217">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="f1748-2217">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f1748-2218">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f1748-2218">Az.Profile</span></span>
* <span data-ttu-id="f1748-2219">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="f1748-2219">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f1748-2220">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="f1748-2220">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-2221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-2221">Az.Compute</span></span>
* <span data-ttu-id="f1748-2222">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="f1748-2222">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f1748-2223">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="f1748-2223">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f1748-2224">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f1748-2224">Az.DataLakeStore</span></span>
* <span data-ttu-id="f1748-2225">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="f1748-2225">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f1748-2226">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="f1748-2226">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f1748-2227">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f1748-2227">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f1748-2228">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="f1748-2228">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f1748-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="f1748-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-2230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-2230">Az.Network</span></span>
* <span data-ttu-id="f1748-2231">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="f1748-2231">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f1748-2232">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="f1748-2232">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-2233">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-2233">Az.Resources</span></span>
* <span data-ttu-id="f1748-2234">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="f1748-2234">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f1748-2235">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="f1748-2235">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f1748-2236">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="f1748-2236">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f1748-2237">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f1748-2237">Azure.Storage</span></span>
* <span data-ttu-id="f1748-2238">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="f1748-2238">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f1748-2239">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f1748-2239">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f1748-2240">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f1748-2240">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f1748-2241">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="f1748-2241">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f1748-2242">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f1748-2242">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f1748-2243">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f1748-2243">Az.CognitiveServices</span></span>
* <span data-ttu-id="f1748-2244">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="f1748-2244">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f1748-2245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f1748-2245">Az.Compute</span></span>
* <span data-ttu-id="f1748-2246">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="f1748-2246">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f1748-2247">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="f1748-2247">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f1748-2248">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="f1748-2248">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f1748-2249">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f1748-2249">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f1748-2250">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="f1748-2250">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f1748-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f1748-2251">Az.Network</span></span>
* <span data-ttu-id="f1748-2252">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="f1748-2252">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f1748-2253">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f1748-2253">new cmdlets added</span></span>
    - <span data-ttu-id="f1748-2254">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f1748-2254">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f1748-2255">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f1748-2255">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f1748-2256">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f1748-2256">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f1748-2257">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f1748-2257">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f1748-2258">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-2258">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f1748-2259">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f1748-2259">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f1748-2260">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="f1748-2260">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f1748-2261">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="f1748-2261">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f1748-2262">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="f1748-2262">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f1748-2263">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f1748-2263">Az.RedisCache</span></span>
* <span data-ttu-id="f1748-2264">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="f1748-2264">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f1748-2265">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="f1748-2265">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f1748-2266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f1748-2266">Az.Resources</span></span>
* <span data-ttu-id="f1748-2267">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f1748-2267">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f1748-2268">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="f1748-2268">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f1748-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f1748-2269">Az.Sql</span></span>
* <span data-ttu-id="f1748-2270">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="f1748-2270">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f1748-2271">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f1748-2271">Az.Websites</span></span>
* <span data-ttu-id="f1748-2272">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="f1748-2272">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f1748-2273">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="f1748-2273">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f1748-2274">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="f1748-2274">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f1748-2275">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="f1748-2275">Initial Release</span></span>