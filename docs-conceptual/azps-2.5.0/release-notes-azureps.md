---
ms.openlocfilehash: 77cb28e47d8dddcf3936edff23f794de3b78442b
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861191"
---
## <a name="250---july-2019"></a><span data-ttu-id="aa7df-101">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="aa7df-101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aa7df-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aa7df-102">Az.Accounts</span></span>
* <span data-ttu-id="aa7df-103">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="aa7df-103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="aa7df-104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="aa7df-104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="aa7df-105">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="aa7df-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aa7df-106">Az.Automation</span></span>
* <span data-ttu-id="aa7df-107">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-107">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="aa7df-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="aa7df-109">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="aa7df-109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-110">Az.Compute</span></span>
* <span data-ttu-id="aa7df-111">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="aa7df-111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="aa7df-112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aa7df-112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="aa7df-113">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="aa7df-114">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="aa7df-114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aa7df-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aa7df-115">Az.DataFactory</span></span>
* <span data-ttu-id="aa7df-116">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="aa7df-116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="aa7df-117">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="aa7df-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="aa7df-118">Az.EventHub</span></span>
* <span data-ttu-id="aa7df-119">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="aa7df-119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="aa7df-120">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="aa7df-120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="aa7df-121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aa7df-121">Az.KeyVault</span></span>
* <span data-ttu-id="aa7df-122">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="aa7df-122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="aa7df-123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="aa7df-123">Az.LogicApp</span></span>
* <span data-ttu-id="aa7df-124">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="aa7df-124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="aa7df-125">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="aa7df-125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="aa7df-126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-126">Az.ManagedServices</span></span>
* <span data-ttu-id="aa7df-127">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="aa7df-127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aa7df-128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-128">Az.Network</span></span>
* <span data-ttu-id="aa7df-129">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="aa7df-129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="aa7df-130">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="aa7df-130">New cmdlets</span></span>
        - <span data-ttu-id="aa7df-131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa7df-131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="aa7df-132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="aa7df-132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="aa7df-133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="aa7df-133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="aa7df-134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="aa7df-134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="aa7df-135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="aa7df-135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="aa7df-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="aa7df-136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="aa7df-137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="aa7df-137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="aa7df-138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="aa7df-138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="aa7df-139">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="aa7df-139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="aa7df-140">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="aa7df-140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="aa7df-141">-PrivateEndpointNetworkPoliciesFlag opcionális paraméter hozzáadva, amely azt jelzi, hogy az alhálózaton be vagy ki van-e kapcsolva a hálózati szabályok alkalmazása a privát végpontra.</span><span class="sxs-lookup"><span data-stu-id="aa7df-141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="aa7df-142">-PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter hozzáadva, amely azt jelzi, hogy az alhálózaton be vagy ki van-e kapcsolva a hálózati szabályok alkalmazása a privát kapcsolatszolgáltatásra.</span><span class="sxs-lookup"><span data-stu-id="aa7df-142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="aa7df-143">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="aa7df-143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="aa7df-144">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="aa7df-145">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="aa7df-145">Updated cmdlets</span></span>
        - <span data-ttu-id="aa7df-146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aa7df-146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="aa7df-147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aa7df-147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="aa7df-148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aa7df-148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="aa7df-149">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="aa7df-149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="aa7df-150">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="aa7df-150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="aa7df-151">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="aa7df-151">Updated cmdlet:</span></span>
        - <span data-ttu-id="aa7df-152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aa7df-152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="aa7df-153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aa7df-153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="aa7df-154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="aa7df-154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="aa7df-155">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="aa7df-155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="aa7df-156">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="aa7df-156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="aa7df-157">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="aa7df-157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="aa7df-158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aa7df-158">Az.OperationalInsights</span></span>
* <span data-ttu-id="aa7df-159">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="aa7df-159">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="aa7df-160">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="aa7df-160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aa7df-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="aa7df-162">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="aa7df-163">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="aa7df-164">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="aa7df-165">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="aa7df-166">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="aa7df-167">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="aa7df-168">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="aa7df-169">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="aa7df-170">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="aa7df-171">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="aa7df-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-172">Az.Resources</span></span>
- <span data-ttu-id="aa7df-173">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="aa7df-174">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="aa7df-174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="aa7df-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aa7df-175">Az.ServiceBus</span></span>
* <span data-ttu-id="aa7df-176">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="aa7df-176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="aa7df-177">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="aa7df-177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="aa7df-178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-178">Az.Sql</span></span>
* <span data-ttu-id="aa7df-179">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="aa7df-180">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="aa7df-181">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="aa7df-181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aa7df-182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aa7df-182">Az.Storage</span></span>
* <span data-ttu-id="aa7df-183">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="aa7df-183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="aa7df-184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="aa7df-184">Az.StorageSync</span></span>
* <span data-ttu-id="aa7df-185">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="aa7df-185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="aa7df-186">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="aa7df-186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aa7df-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aa7df-187">Az.Websites</span></span>
* <span data-ttu-id="aa7df-188">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="aa7df-188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="aa7df-189">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="aa7df-190">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="aa7df-191">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="aa7df-191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aa7df-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aa7df-192">Az.Accounts</span></span>
* <span data-ttu-id="aa7df-193">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="aa7df-193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="aa7df-194">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="aa7df-194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="aa7df-195">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="aa7df-195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="aa7df-196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="aa7df-196">Az.Advisor</span></span>
* <span data-ttu-id="aa7df-197">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="aa7df-197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="aa7df-198">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="aa7df-198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="aa7df-199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="aa7df-199">Az.ApiManagement</span></span>
* <span data-ttu-id="aa7df-200">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="aa7df-200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="aa7df-201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="aa7df-201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="aa7df-202">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="aa7df-202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="aa7df-203">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="aa7df-203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="aa7df-204">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="aa7df-204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="aa7df-205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="aa7df-205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="aa7df-206">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="aa7df-206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aa7df-207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aa7df-207">Az.Automation</span></span>
* <span data-ttu-id="aa7df-208">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="aa7df-208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-209">Az.Compute</span></span>
* <span data-ttu-id="aa7df-210">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aa7df-211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aa7df-211">Az.DataFactory</span></span>
* <span data-ttu-id="aa7df-212">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="aa7df-212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="aa7df-213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="aa7df-213">Az.EventGrid</span></span>
* <span data-ttu-id="aa7df-214">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="aa7df-214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="aa7df-215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="aa7df-215">Az.IotHub</span></span>
* <span data-ttu-id="aa7df-216">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="aa7df-216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aa7df-217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-217">Az.Network</span></span>
* <span data-ttu-id="aa7df-218">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="aa7df-219">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="aa7df-219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="aa7df-220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="aa7df-220">Az.PolicyInsights</span></span>
* <span data-ttu-id="aa7df-221">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="aa7df-221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="aa7df-222">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="aa7df-222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="aa7df-223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aa7df-223">Az.OperationalInsights</span></span>
* <span data-ttu-id="aa7df-224">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="aa7df-224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aa7df-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="aa7df-226">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="aa7df-227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-227">Az.Resources</span></span>
    - <span data-ttu-id="aa7df-228">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="aa7df-229">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="aa7df-230">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="aa7df-231">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="aa7df-232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aa7df-232">Az.ServiceBus</span></span>
* <span data-ttu-id="aa7df-233">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="aa7df-233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="aa7df-234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-234">Az.Sql</span></span>
* <span data-ttu-id="aa7df-235">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="aa7df-236">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="aa7df-236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="aa7df-237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="aa7df-237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="aa7df-238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="aa7df-238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="aa7df-239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="aa7df-239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="aa7df-240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="aa7df-240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="aa7df-241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="aa7df-241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="aa7df-242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="aa7df-242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="aa7df-243">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="aa7df-243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aa7df-244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aa7df-244">Az.Storage</span></span>
* <span data-ttu-id="aa7df-245">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="aa7df-245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="aa7df-246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="aa7df-246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="aa7df-247">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="aa7df-247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="aa7df-248">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="aa7df-248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="aa7df-249">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="aa7df-249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="aa7df-250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa7df-250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="aa7df-251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa7df-251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="aa7df-252">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="aa7df-252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="aa7df-253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="aa7df-253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="aa7df-254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="aa7df-254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="aa7df-255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="aa7df-255">Az.StorageSync</span></span>
* <span data-ttu-id="aa7df-256">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="aa7df-256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="aa7df-257">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="aa7df-257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aa7df-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aa7df-258">Az.Accounts</span></span>
* <span data-ttu-id="aa7df-259">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="aa7df-260">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="aa7df-260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="aa7df-261">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="aa7df-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="aa7df-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="aa7df-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="aa7df-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-264">Az.Compute</span></span>
* <span data-ttu-id="aa7df-265">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="aa7df-265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="aa7df-266">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="aa7df-266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="aa7df-267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="aa7df-267">Az.Dns</span></span>
* <span data-ttu-id="aa7df-268">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="aa7df-268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="aa7df-269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="aa7df-269">Az.EventGrid</span></span>
* <span data-ttu-id="aa7df-270">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="aa7df-270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="aa7df-271">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="aa7df-271">New cmdlets:</span></span>
    - <span data-ttu-id="aa7df-272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="aa7df-272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="aa7df-273">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="aa7df-273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="aa7df-274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="aa7df-274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="aa7df-275">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="aa7df-275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="aa7df-276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="aa7df-276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="aa7df-277">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="aa7df-277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="aa7df-278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="aa7df-278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="aa7df-279">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="aa7df-279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="aa7df-280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="aa7df-280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="aa7df-281">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="aa7df-281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="aa7df-282">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="aa7df-282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="aa7df-283">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="aa7df-283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="aa7df-284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="aa7df-284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="aa7df-285">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="aa7df-285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="aa7df-286">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="aa7df-286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="aa7df-287">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="aa7df-287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="aa7df-288">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="aa7df-288">Updated cmdlets:</span></span>
    - <span data-ttu-id="aa7df-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="aa7df-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="aa7df-290">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="aa7df-290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="aa7df-291">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="aa7df-291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="aa7df-292">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="aa7df-292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="aa7df-293">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="aa7df-293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="aa7df-294">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="aa7df-294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="aa7df-295">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="aa7df-295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="aa7df-296">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="aa7df-296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="aa7df-297">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="aa7df-297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="aa7df-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="aa7df-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="aa7df-299">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="aa7df-299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="aa7df-300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="aa7df-300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="aa7df-301">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="aa7df-301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="aa7df-302">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="aa7df-302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="aa7df-303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="aa7df-303">Az.FrontDoor</span></span>
* <span data-ttu-id="aa7df-304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="aa7df-304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="aa7df-305">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="aa7df-305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="aa7df-306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="aa7df-306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="aa7df-307">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="aa7df-307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aa7df-308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-308">Az.Network</span></span>
* <span data-ttu-id="aa7df-309">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="aa7df-309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="aa7df-310">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="aa7df-310">New cmdlets</span></span>
        - <span data-ttu-id="aa7df-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="aa7df-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="aa7df-312">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="aa7df-312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="aa7df-313">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="aa7df-313">New cmdlets</span></span> 
        - <span data-ttu-id="aa7df-314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="aa7df-314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="aa7df-315">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="aa7df-315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="aa7df-316">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="aa7df-316">New cmdlets</span></span> 
        - <span data-ttu-id="aa7df-317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="aa7df-317">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="aa7df-318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="aa7df-318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="aa7df-319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="aa7df-319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="aa7df-320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="aa7df-320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="aa7df-321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="aa7df-321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="aa7df-322">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="aa7df-322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="aa7df-323">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="aa7df-323">New cmdlets</span></span>
        - <span data-ttu-id="aa7df-324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa7df-324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="aa7df-325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa7df-325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="aa7df-326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa7df-326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="aa7df-327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="aa7df-327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="aa7df-328">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="aa7df-328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="aa7df-329">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="aa7df-329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="aa7df-330">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="aa7df-330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="aa7df-331">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="aa7df-331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="aa7df-332">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="aa7df-332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="aa7df-333">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="aa7df-333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="aa7df-334">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="aa7df-334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="aa7df-335">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="aa7df-335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="aa7df-336">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="aa7df-337">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="aa7df-337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="aa7df-338">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="aa7df-339">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="aa7df-340">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="aa7df-340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="aa7df-341">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="aa7df-342">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="aa7df-342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="aa7df-343">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="aa7df-343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="aa7df-344">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="aa7df-344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="aa7df-345">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="aa7df-345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="aa7df-346">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="aa7df-346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="aa7df-347">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="aa7df-347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="aa7df-348">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="aa7df-348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="aa7df-349">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="aa7df-349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="aa7df-350">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="aa7df-350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="aa7df-351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aa7df-351">Az.OperationalInsights</span></span>
* <span data-ttu-id="aa7df-352">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="aa7df-353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-353">Az.Resources</span></span>
* <span data-ttu-id="aa7df-354">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="aa7df-354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="aa7df-355">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="aa7df-356">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="aa7df-357">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="aa7df-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aa7df-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="aa7df-359">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="aa7df-359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="aa7df-360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-360">Az.Sql</span></span>
* <span data-ttu-id="aa7df-361">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="aa7df-361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="aa7df-362">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="aa7df-362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="aa7df-363">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="aa7df-364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="aa7df-364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="aa7df-365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="aa7df-365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="aa7df-366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="aa7df-366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="aa7df-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="aa7df-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="aa7df-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="aa7df-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aa7df-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aa7df-369">Az.Storage</span></span>
* <span data-ttu-id="aa7df-370">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="aa7df-370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="aa7df-371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa7df-371">New-AzStorageAccount</span></span>
* <span data-ttu-id="aa7df-372">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="aa7df-372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="aa7df-373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="aa7df-373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aa7df-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aa7df-374">Az.Websites</span></span>
* <span data-ttu-id="aa7df-375">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="aa7df-375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="aa7df-376">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="aa7df-377">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="aa7df-377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="aa7df-378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="aa7df-378">Az.Cdn</span></span>
* <span data-ttu-id="aa7df-379">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="aa7df-379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-380">Az.Compute</span></span>
* <span data-ttu-id="aa7df-381">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="aa7df-381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="aa7df-382">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="aa7df-382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="aa7df-383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="aa7df-383">Az.EventHub</span></span>
* <span data-ttu-id="aa7df-384">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="aa7df-384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="aa7df-385">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="aa7df-385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aa7df-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-386">Az.Network</span></span>
* <span data-ttu-id="aa7df-387">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="aa7df-387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="aa7df-388">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="aa7df-388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="aa7df-389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="aa7df-389">Az.PolicyInsights</span></span>
* <span data-ttu-id="aa7df-390">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="aa7df-390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aa7df-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="aa7df-392">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="aa7df-392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="aa7df-393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aa7df-393">Az.ServiceBus</span></span>
* <span data-ttu-id="aa7df-394">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="aa7df-394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="aa7df-395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aa7df-395">Az.ServiceFabric</span></span>
* <span data-ttu-id="aa7df-396">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="aa7df-397">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="aa7df-397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="aa7df-398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-398">Az.Sql</span></span>
* <span data-ttu-id="aa7df-399">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="aa7df-399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="aa7df-400">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="aa7df-400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="aa7df-401">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="aa7df-401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="aa7df-402">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="aa7df-402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aa7df-403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aa7df-403">Az.Websites</span></span>
* <span data-ttu-id="aa7df-404">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="aa7df-404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="aa7df-405">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="aa7df-405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="aa7df-406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="aa7df-406">Az.ApiManagement</span></span>
* <span data-ttu-id="aa7df-407">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="aa7df-407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="aa7df-408">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="aa7df-408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="aa7df-409">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="aa7df-409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="aa7df-410">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="aa7df-410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="aa7df-411">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="aa7df-411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="aa7df-412">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="aa7df-413">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="aa7df-413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="aa7df-414">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="aa7df-414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="aa7df-415">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="aa7df-416">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="aa7df-416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="aa7df-417">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="aa7df-417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="aa7df-418">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="aa7df-419">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="aa7df-420">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="aa7df-421">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="aa7df-422">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="aa7df-422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="aa7df-423">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="aa7df-424">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="aa7df-425">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="aa7df-425">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="aa7df-426">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="aa7df-426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="aa7df-427">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="aa7df-428">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="aa7df-428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="aa7df-429">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="aa7df-429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="aa7df-430">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="aa7df-431">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="aa7df-431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="aa7df-432">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="aa7df-432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="aa7df-433">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="aa7df-433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="aa7df-434">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="aa7df-434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="aa7df-435">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="aa7df-435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="aa7df-436">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="aa7df-436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="aa7df-437">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-437">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="aa7df-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="aa7df-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="aa7df-439">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="aa7df-439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="aa7df-440">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="aa7df-441">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="aa7df-441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="aa7df-442">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="aa7df-442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="aa7df-443">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="aa7df-443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="aa7df-444">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="aa7df-444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="aa7df-445">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="aa7df-445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="aa7df-446">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-446">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="aa7df-447">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="aa7df-447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="aa7df-448">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="aa7df-448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="aa7df-449">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="aa7df-449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="aa7df-450">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="aa7df-450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="aa7df-451">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="aa7df-452">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="aa7df-452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="aa7df-453">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="aa7df-453">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="aa7df-454">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="aa7df-454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="aa7df-455">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="aa7df-456">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="aa7df-456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="aa7df-457">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="aa7df-457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="aa7df-458">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="aa7df-459">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="aa7df-459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="aa7df-460">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="aa7df-461">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="aa7df-461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="aa7df-462">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="aa7df-463">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="aa7df-464">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="aa7df-465">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="aa7df-466">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="aa7df-467">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="aa7df-468">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="aa7df-469">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="aa7df-470">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="aa7df-471">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="aa7df-471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="aa7df-472">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aa7df-472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="aa7df-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="aa7df-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="aa7df-474">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aa7df-474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="aa7df-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="aa7df-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="aa7df-476">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="aa7df-476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="aa7df-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="aa7df-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="aa7df-478">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="aa7df-478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="aa7df-479">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aa7df-479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="aa7df-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="aa7df-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="aa7df-481">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="aa7df-481">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="aa7df-482">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="aa7df-482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="aa7df-483">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="aa7df-483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aa7df-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aa7df-484">Az.Automation</span></span>
* <span data-ttu-id="aa7df-485">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="aa7df-486">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="aa7df-486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="aa7df-487">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="aa7df-487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="aa7df-488">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="aa7df-488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="aa7df-489">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="aa7df-489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="aa7df-490">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="aa7df-490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="aa7df-491">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="aa7df-491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-492">Az.Compute</span></span>
* <span data-ttu-id="aa7df-493">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="aa7df-494">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="aa7df-494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aa7df-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aa7df-495">Az.DataLakeStore</span></span>
* <span data-ttu-id="aa7df-496">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="aa7df-496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="aa7df-497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="aa7df-497">Az.Monitor</span></span>
* <span data-ttu-id="aa7df-498">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="aa7df-498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aa7df-499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-499">Az.Network</span></span>
* <span data-ttu-id="aa7df-500">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="aa7df-501">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="aa7df-501">Updated cmdlet:</span></span>
        - <span data-ttu-id="aa7df-502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="aa7df-502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="aa7df-503">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="aa7df-503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="aa7df-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-504">Az.Resources</span></span>
* <span data-ttu-id="aa7df-505">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="aa7df-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-506">Az.Sql</span></span>
* <span data-ttu-id="aa7df-507">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="aa7df-507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="aa7df-508">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="aa7df-508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aa7df-509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aa7df-509">Az.Accounts</span></span>
* <span data-ttu-id="aa7df-510">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="aa7df-510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="aa7df-511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-511">Az.CognitiveServices</span></span>
* <span data-ttu-id="aa7df-512">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="aa7df-512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="aa7df-513">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="aa7df-513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-514">Az.Compute</span></span>
* <span data-ttu-id="aa7df-515">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="aa7df-515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="aa7df-516">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="aa7df-516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="aa7df-517">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="aa7df-517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="aa7df-518">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="aa7df-518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="aa7df-519">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="aa7df-519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="aa7df-520">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="aa7df-521">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="aa7df-521">Breaking changes</span></span>
    - <span data-ttu-id="aa7df-522">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="aa7df-522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="aa7df-523">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="aa7df-523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="aa7df-524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="aa7df-524">Az.DeploymentManager</span></span>
* <span data-ttu-id="aa7df-525">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="aa7df-525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="aa7df-526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="aa7df-526">Az.Dns</span></span>
* <span data-ttu-id="aa7df-527">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="aa7df-527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="aa7df-528">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="aa7df-529">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="aa7df-529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="aa7df-530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="aa7df-530">Az.FrontDoor</span></span>
* <span data-ttu-id="aa7df-531">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="aa7df-531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="aa7df-532">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="aa7df-532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="aa7df-533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="aa7df-533">Az.HDInsight</span></span>
* <span data-ttu-id="aa7df-534">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="aa7df-534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="aa7df-535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="aa7df-535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="aa7df-536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="aa7df-536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="aa7df-537">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="aa7df-537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="aa7df-538">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="aa7df-538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="aa7df-539">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="aa7df-539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="aa7df-540">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="aa7df-540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="aa7df-541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="aa7df-541">Az.Monitor</span></span>
* <span data-ttu-id="aa7df-542">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="aa7df-542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="aa7df-543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="aa7df-543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="aa7df-544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="aa7df-544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="aa7df-545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="aa7df-545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="aa7df-546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="aa7df-546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="aa7df-547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="aa7df-547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="aa7df-548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="aa7df-548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="aa7df-549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="aa7df-549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="aa7df-550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="aa7df-550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="aa7df-551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="aa7df-551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="aa7df-552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="aa7df-552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="aa7df-553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="aa7df-553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="aa7df-554">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="aa7df-554">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="aa7df-555">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="aa7df-555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aa7df-556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-556">Az.Network</span></span>
* <span data-ttu-id="aa7df-557">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="aa7df-557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="aa7df-558">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="aa7df-558">New cmdlets</span></span>
        - <span data-ttu-id="aa7df-559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="aa7df-559">New-AzNatGateway</span></span>
        - <span data-ttu-id="aa7df-560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="aa7df-560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="aa7df-561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="aa7df-561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="aa7df-562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="aa7df-562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="aa7df-563">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="aa7df-563">Updated cmdlets</span></span>
        - <span data-ttu-id="aa7df-564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="aa7df-564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="aa7df-565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="aa7df-565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="aa7df-566">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="aa7df-566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="aa7df-567">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="aa7df-567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="aa7df-568">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="aa7df-568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="aa7df-569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="aa7df-569">Az.PolicyInsights</span></span>
* <span data-ttu-id="aa7df-570">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="aa7df-570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="aa7df-571">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="aa7df-571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="aa7df-572">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="aa7df-572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aa7df-573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-573">Az.RecoveryServices</span></span>
* <span data-ttu-id="aa7df-574">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="aa7df-574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="aa7df-575">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="aa7df-575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="aa7df-576">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="aa7df-576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="aa7df-577">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="aa7df-577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="aa7df-578">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="aa7df-578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="aa7df-579">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="aa7df-579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="aa7df-580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="aa7df-580">Az.Relay</span></span>
* <span data-ttu-id="aa7df-581">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="aa7df-581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="aa7df-582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aa7df-582">Az.ServiceBus</span></span>
* <span data-ttu-id="aa7df-583">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="aa7df-583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aa7df-584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aa7df-584">Az.Storage</span></span>
* <span data-ttu-id="aa7df-585">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="aa7df-585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="aa7df-586">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="aa7df-586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="aa7df-587">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="aa7df-587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="aa7df-588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa7df-588">New-AzStorageAccount</span></span>
* <span data-ttu-id="aa7df-589">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="aa7df-589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="aa7df-590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa7df-590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="aa7df-591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa7df-591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="aa7df-592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa7df-592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aa7df-593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aa7df-593">Az.Websites</span></span>
* <span data-ttu-id="aa7df-594">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="aa7df-595">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="aa7df-595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="aa7df-596">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="aa7df-596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="aa7df-597">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="aa7df-597">Highlights since the last major release</span></span>
* <span data-ttu-id="aa7df-598">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="aa7df-598">General availability of `Az` module</span></span>
* <span data-ttu-id="aa7df-599">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="aa7df-599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="aa7df-600">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="aa7df-600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="aa7df-601">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="aa7df-602">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="aa7df-603">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="aa7df-604">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="aa7df-605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aa7df-605">Az.Accounts</span></span>
* <span data-ttu-id="aa7df-606">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="aa7df-607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="aa7df-607">Az.Batch</span></span>
* <span data-ttu-id="aa7df-608">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="aa7df-609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="aa7df-609">Az.Cdn</span></span>
* <span data-ttu-id="aa7df-610">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="aa7df-611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-611">Az.CognitiveServices</span></span>
* <span data-ttu-id="aa7df-612">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-613">Az.Compute</span></span>
* <span data-ttu-id="aa7df-614">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="aa7df-614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="aa7df-615">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aa7df-616">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="aa7df-616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aa7df-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aa7df-617">Az.DataFactory</span></span>
* <span data-ttu-id="aa7df-618">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="aa7df-618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aa7df-619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aa7df-619">Az.DataLakeStore</span></span>
* <span data-ttu-id="aa7df-620">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="aa7df-621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="aa7df-621">Az.EventGrid</span></span>
* <span data-ttu-id="aa7df-622">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="aa7df-622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="aa7df-623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="aa7df-623">Az.EventHub</span></span>
* <span data-ttu-id="aa7df-624">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="aa7df-624">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="aa7df-625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="aa7df-625">Az.HDInsight</span></span>
* <span data-ttu-id="aa7df-626">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="aa7df-627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="aa7df-627">Az.IotHub</span></span>
* <span data-ttu-id="aa7df-628">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="aa7df-629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aa7df-629">Az.KeyVault</span></span>
* <span data-ttu-id="aa7df-630">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aa7df-631">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="aa7df-631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="aa7df-632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="aa7df-632">Az.MachineLearning</span></span>
* <span data-ttu-id="aa7df-633">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="aa7df-634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="aa7df-634">Az.Media</span></span>
* <span data-ttu-id="aa7df-635">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="aa7df-636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="aa7df-636">Az.Monitor</span></span>
  * <span data-ttu-id="aa7df-637">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="aa7df-637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="aa7df-638">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="aa7df-638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="aa7df-639">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="aa7df-639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="aa7df-640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="aa7df-640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="aa7df-641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="aa7df-641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="aa7df-642">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="aa7df-642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="aa7df-643">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="aa7df-643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aa7df-644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-644">Az.Network</span></span>
* <span data-ttu-id="aa7df-645">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aa7df-646">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="aa7df-646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="aa7df-647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="aa7df-647">Az.NotificationHubs</span></span>
* <span data-ttu-id="aa7df-648">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="aa7df-649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aa7df-649">Az.OperationalInsights</span></span>
* <span data-ttu-id="aa7df-650">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="aa7df-651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="aa7df-651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="aa7df-652">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aa7df-653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-653">Az.RecoveryServices</span></span>
* <span data-ttu-id="aa7df-654">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aa7df-655">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="aa7df-655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="aa7df-656">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="aa7df-656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="aa7df-657">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="aa7df-657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="aa7df-658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="aa7df-658">Az.RedisCache</span></span>
* <span data-ttu-id="aa7df-659">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="aa7df-660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-660">Az.Resources</span></span>
* <span data-ttu-id="aa7df-661">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="aa7df-661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="aa7df-662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-662">Az.Sql</span></span>
* <span data-ttu-id="aa7df-663">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="aa7df-663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="aa7df-664">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aa7df-665">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="aa7df-665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="aa7df-666">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="aa7df-666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="aa7df-667">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="aa7df-667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="aa7df-668">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="aa7df-668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="aa7df-669">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="aa7df-669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aa7df-670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aa7df-670">Az.Websites</span></span>
* <span data-ttu-id="aa7df-671">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="aa7df-671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="aa7df-672">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="aa7df-673">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="aa7df-673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="aa7df-674">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="aa7df-674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="aa7df-675">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="aa7df-675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="aa7df-676">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="aa7df-676">Highlights since the last major release</span></span>
* <span data-ttu-id="aa7df-677">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="aa7df-677">General availability of `Az` module</span></span>
* <span data-ttu-id="aa7df-678">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="aa7df-678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="aa7df-679">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="aa7df-679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="aa7df-680">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="aa7df-681">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="aa7df-682">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="aa7df-683">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="aa7df-684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aa7df-684">Az.Accounts</span></span>
* <span data-ttu-id="aa7df-685">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="aa7df-685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="aa7df-686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-686">Az.AnalysisServices</span></span>
* <span data-ttu-id="aa7df-687">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="aa7df-688">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aa7df-689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aa7df-689">Az.Automation</span></span>
* <span data-ttu-id="aa7df-690">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="aa7df-690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="aa7df-691">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="aa7df-691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="aa7df-692">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-693">Az.Compute</span></span>
* <span data-ttu-id="aa7df-694">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="aa7df-695">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="aa7df-695">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="aa7df-696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="aa7df-696">Az.ContainerInstance</span></span>
* <span data-ttu-id="aa7df-697">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="aa7df-697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aa7df-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aa7df-698">Az.DataFactory</span></span>
* <span data-ttu-id="aa7df-699">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="aa7df-699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="aa7df-700">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="aa7df-700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="aa7df-701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-701">Az.Resources</span></span>
* <span data-ttu-id="aa7df-702">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="aa7df-702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="aa7df-703">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="aa7df-704">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="aa7df-704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="aa7df-705">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="aa7df-705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="aa7df-706">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="aa7df-707">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="aa7df-707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="aa7df-708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-708">Az.Sql</span></span>
* <span data-ttu-id="aa7df-709">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="aa7df-709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aa7df-710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aa7df-710">Az.Storage</span></span>
* <span data-ttu-id="aa7df-711">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="aa7df-711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="aa7df-712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="aa7df-712">New-AzStorageContext</span></span>
* <span data-ttu-id="aa7df-713">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="aa7df-713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="aa7df-714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="aa7df-714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="aa7df-715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="aa7df-715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="aa7df-716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aa7df-716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="aa7df-717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aa7df-717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="aa7df-718">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="aa7df-719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="aa7df-719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="aa7df-720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="aa7df-720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="aa7df-721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="aa7df-721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="aa7df-722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="aa7df-722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="aa7df-723">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="aa7df-723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="aa7df-724">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="aa7df-724">Highlights since the last major release</span></span>
* <span data-ttu-id="aa7df-725">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="aa7df-725">General availability of `Az` module</span></span>
* <span data-ttu-id="aa7df-726">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="aa7df-726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="aa7df-727">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="aa7df-727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="aa7df-728">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="aa7df-729">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="aa7df-730">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="aa7df-731">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aa7df-732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aa7df-732">Az.Automation</span></span>
* <span data-ttu-id="aa7df-733">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="aa7df-733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="aa7df-734">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="aa7df-734">Dynamic grouping</span></span>
    * <span data-ttu-id="aa7df-735">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="aa7df-735">Pre-Post script</span></span>
    * <span data-ttu-id="aa7df-736">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="aa7df-736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-737">Az.Compute</span></span>
* <span data-ttu-id="aa7df-738">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="aa7df-739">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="aa7df-739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="aa7df-740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aa7df-740">Az.KeyVault</span></span>
* <span data-ttu-id="aa7df-741">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aa7df-742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-742">Az.Network</span></span>
* <span data-ttu-id="aa7df-743">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="aa7df-744">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="aa7df-744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aa7df-745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-745">Az.RecoveryServices</span></span>
* <span data-ttu-id="aa7df-746">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="aa7df-746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="aa7df-747">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="aa7df-748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-748">Az.Resources</span></span>
* <span data-ttu-id="aa7df-749">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="aa7df-750">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="aa7df-751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-751">Az.Sql</span></span>
* <span data-ttu-id="aa7df-752">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="aa7df-752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aa7df-753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aa7df-753">Az.Storage</span></span>
* <span data-ttu-id="aa7df-754">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="aa7df-754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="aa7df-755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="aa7df-755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="aa7df-756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="aa7df-756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="aa7df-757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="aa7df-757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="aa7df-758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="aa7df-758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="aa7df-759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="aa7df-759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="aa7df-760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="aa7df-760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aa7df-761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aa7df-761">Az.Websites</span></span>
* <span data-ttu-id="aa7df-762">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="aa7df-762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="aa7df-763">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="aa7df-763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aa7df-764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aa7df-764">Az.Accounts</span></span>
* <span data-ttu-id="aa7df-765">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="aa7df-765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="aa7df-766">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aa7df-767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aa7df-767">Az.Automation</span></span>
* <span data-ttu-id="aa7df-768">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="aa7df-769">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="aa7df-769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="aa7df-770">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="aa7df-770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="aa7df-771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="aa7df-771">Az.Cdn</span></span>
* <span data-ttu-id="aa7df-772">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="aa7df-772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-773">Az.Compute</span></span>
* <span data-ttu-id="aa7df-774">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aa7df-775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aa7df-775">Az.DataFactory</span></span>
* <span data-ttu-id="aa7df-776">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="aa7df-776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="aa7df-777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="aa7df-777">Az.LogicApp</span></span>
* <span data-ttu-id="aa7df-778">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="aa7df-778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aa7df-779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-779">Az.Network</span></span>
* <span data-ttu-id="aa7df-780">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aa7df-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="aa7df-782">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="aa7df-782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="aa7df-783">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="aa7df-783">SDK Update</span></span>
* <span data-ttu-id="aa7df-784">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="aa7df-784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="aa7df-785">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="aa7df-786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-786">Az.Resources</span></span>
* <span data-ttu-id="aa7df-787">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="aa7df-788">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="aa7df-788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="aa7df-789">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="aa7df-789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="aa7df-790">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="aa7df-790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="aa7df-791">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="aa7df-791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="aa7df-792">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="aa7df-792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="aa7df-793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-793">Az.Sql</span></span>
* <span data-ttu-id="aa7df-794">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="aa7df-794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="aa7df-795">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="aa7df-795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aa7df-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aa7df-796">Az.Storage</span></span>
* <span data-ttu-id="aa7df-797">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa7df-797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="aa7df-798">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="aa7df-798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="aa7df-799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-799">Az.AnalysisServices</span></span>
* <span data-ttu-id="aa7df-800">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="aa7df-800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aa7df-801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aa7df-801">Az.Automation</span></span>
* <span data-ttu-id="aa7df-802">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="aa7df-803">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="aa7df-804">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="aa7df-805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-805">Az.CognitiveServices</span></span>
* <span data-ttu-id="aa7df-806">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="aa7df-806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-807">Az.Compute</span></span>
* <span data-ttu-id="aa7df-808">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="aa7df-808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="aa7df-809">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="aa7df-809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="aa7df-810">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="aa7df-811">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="aa7df-811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aa7df-812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aa7df-812">Az.DataLakeStore</span></span>
* <span data-ttu-id="aa7df-813">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="aa7df-813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="aa7df-814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="aa7df-814">Az.EventHub</span></span>
* <span data-ttu-id="aa7df-815">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="aa7df-815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="aa7df-816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aa7df-816">Az.KeyVault</span></span>
* <span data-ttu-id="aa7df-817">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="aa7df-818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="aa7df-818">Az.LogicApp</span></span>
* <span data-ttu-id="aa7df-819">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="aa7df-819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="aa7df-820">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="aa7df-820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="aa7df-821">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="aa7df-821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="aa7df-822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aa7df-822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="aa7df-823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aa7df-823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="aa7df-824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aa7df-824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="aa7df-825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="aa7df-825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="aa7df-826">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="aa7df-826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="aa7df-827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa7df-827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="aa7df-828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa7df-828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="aa7df-829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa7df-829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="aa7df-830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa7df-830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="aa7df-831">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="aa7df-831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="aa7df-832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="aa7df-832">Az.Monitor</span></span>
* <span data-ttu-id="aa7df-833">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aa7df-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-834">Az.Network</span></span>
* <span data-ttu-id="aa7df-835">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="aa7df-835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="aa7df-836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aa7df-836">Az.OperationalInsights</span></span>
* <span data-ttu-id="aa7df-837">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="aa7df-837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="aa7df-838">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="aa7df-838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="aa7df-839">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="aa7df-839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="aa7df-840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-840">Az.Resources</span></span>
* <span data-ttu-id="aa7df-841">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="aa7df-841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="aa7df-842">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="aa7df-842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="aa7df-843">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="aa7df-843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="aa7df-844">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="aa7df-844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="aa7df-845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-845">Az.Sql</span></span>
* <span data-ttu-id="aa7df-846">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="aa7df-846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="aa7df-847">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="aa7df-847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aa7df-848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aa7df-848">Az.Websites</span></span>
* <span data-ttu-id="aa7df-849">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="aa7df-850">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="aa7df-850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aa7df-851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aa7df-851">Az.Accounts</span></span>
* <span data-ttu-id="aa7df-852">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="aa7df-852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="aa7df-853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-853">Az.AnalysisServices</span></span>
<span data-ttu-id="aa7df-854">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="aa7df-854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-855">Az.Compute</span></span>
* <span data-ttu-id="aa7df-856">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="aa7df-856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="aa7df-857">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="aa7df-857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="aa7df-858">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="aa7df-858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aa7df-859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-859">Az.RecoveryServices</span></span>
<span data-ttu-id="aa7df-860">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="aa7df-860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="aa7df-861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-861">Az.Resources</span></span>
* <span data-ttu-id="aa7df-862">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="aa7df-862">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="aa7df-863">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="aa7df-863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="aa7df-864">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="aa7df-864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="aa7df-865">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="aa7df-865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="aa7df-866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-866">Az.Sql</span></span>
* <span data-ttu-id="aa7df-867">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="aa7df-867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="aa7df-868">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="aa7df-868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="aa7df-869">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="aa7df-869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="aa7df-870">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="aa7df-870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aa7df-871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aa7df-871">Az.Accounts</span></span>
* <span data-ttu-id="aa7df-872">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="aa7df-872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="aa7df-873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-873">Az.AnalysisServices</span></span>
* <span data-ttu-id="aa7df-874">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="aa7df-874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="aa7df-875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-875">Az.RecoveryServices</span></span>
* <span data-ttu-id="aa7df-876">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="aa7df-876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="aa7df-877">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="aa7df-877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aa7df-878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aa7df-878">Az.Accounts</span></span>
* <span data-ttu-id="aa7df-879">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="aa7df-880">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="aa7df-880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aa7df-881">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="aa7df-881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="aa7df-882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="aa7df-882">Az.Aks</span></span>
* <span data-ttu-id="aa7df-883">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="aa7df-883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="aa7df-884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aa7df-884">Az.Automation</span></span>
* <span data-ttu-id="aa7df-885">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="aa7df-885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="aa7df-886">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="aa7df-886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="aa7df-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="aa7df-887">Az.Cdn</span></span>
* <span data-ttu-id="aa7df-888">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="aa7df-888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-889">Az.Compute</span></span>
* <span data-ttu-id="aa7df-890">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="aa7df-890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="aa7df-891">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="aa7df-891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="aa7df-892">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="aa7df-892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="aa7df-893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aa7df-893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="aa7df-894">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="aa7df-894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="aa7df-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aa7df-895">Az.DataFactory</span></span>
* <span data-ttu-id="aa7df-896">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="aa7df-896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aa7df-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aa7df-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="aa7df-898">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="aa7df-898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="aa7df-899">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="aa7df-899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="aa7df-900">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="aa7df-900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="aa7df-901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="aa7df-901">Az.IotHub</span></span>
* <span data-ttu-id="aa7df-902">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="aa7df-902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="aa7df-903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aa7df-903">Az.KeyVault</span></span>
* <span data-ttu-id="aa7df-904">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="aa7df-904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aa7df-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-905">Az.Network</span></span>
* <span data-ttu-id="aa7df-906">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="aa7df-906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="aa7df-907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-907">Az.Resources</span></span>
* <span data-ttu-id="aa7df-908">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="aa7df-908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="aa7df-909">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="aa7df-909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="aa7df-910">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="aa7df-910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="aa7df-911">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="aa7df-911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="aa7df-912">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="aa7df-912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="aa7df-913">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="aa7df-913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="aa7df-914">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="aa7df-914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="aa7df-915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aa7df-915">Az.ServiceFabric</span></span>
* <span data-ttu-id="aa7df-916">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="aa7df-916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="aa7df-917">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="aa7df-917">Fix some error messages.</span></span>
* <span data-ttu-id="aa7df-918">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="aa7df-918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="aa7df-919">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="aa7df-919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="aa7df-920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="aa7df-920">Az.SignalR</span></span>
* <span data-ttu-id="aa7df-921">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="aa7df-921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="aa7df-922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-922">Az.Sql</span></span>
* <span data-ttu-id="aa7df-923">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="aa7df-923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aa7df-924">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="aa7df-924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="aa7df-925">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="aa7df-925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="aa7df-926">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="aa7df-926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aa7df-927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aa7df-927">Az.Storage</span></span>
* <span data-ttu-id="aa7df-928">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="aa7df-928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aa7df-929">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="aa7df-929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="aa7df-930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="aa7df-930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="aa7df-931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="aa7df-931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="aa7df-932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="aa7df-932">Az.TrafficManager</span></span>
* <span data-ttu-id="aa7df-933">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="aa7df-933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aa7df-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aa7df-934">Az.Websites</span></span>
* <span data-ttu-id="aa7df-935">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="aa7df-935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="aa7df-936">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="aa7df-936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="aa7df-937">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="aa7df-937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="aa7df-938">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="aa7df-938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="aa7df-939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aa7df-939">Az.Accounts</span></span>
* <span data-ttu-id="aa7df-940">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-941">Az.Compute</span></span>
* <span data-ttu-id="aa7df-942">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="aa7df-942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="aa7df-943">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="aa7df-943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="aa7df-944">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="aa7df-944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aa7df-945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aa7df-945">Az.DataLakeStore</span></span>
* <span data-ttu-id="aa7df-946">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="aa7df-946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="aa7df-947">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="aa7df-947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="aa7df-948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="aa7df-948">Az.EventGrid</span></span>
* <span data-ttu-id="aa7df-949">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="aa7df-949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="aa7df-950">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="aa7df-950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="aa7df-951">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="aa7df-951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="aa7df-952">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="aa7df-952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="aa7df-953">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="aa7df-953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="aa7df-954">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="aa7df-954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="aa7df-955">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="aa7df-955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="aa7df-956">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="aa7df-956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="aa7df-957">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="aa7df-957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="aa7df-958">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="aa7df-958">Dead letter endpoint.</span></span>
* <span data-ttu-id="aa7df-959">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="aa7df-959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="aa7df-960">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="aa7df-960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="aa7df-961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="aa7df-961">Az.IotHub</span></span>
* <span data-ttu-id="aa7df-962">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="aa7df-962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="aa7df-963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="aa7df-963">Az.LogicApp</span></span>
* <span data-ttu-id="aa7df-964">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="aa7df-964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="aa7df-965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-965">Az.Resources</span></span>
* <span data-ttu-id="aa7df-966">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="aa7df-966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="aa7df-967">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="aa7df-967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="aa7df-968">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="aa7df-968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="aa7df-969">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="aa7df-969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="aa7df-970">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="aa7df-971">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="aa7df-971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="aa7df-972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="aa7df-972">Az.SignalR</span></span>
* <span data-ttu-id="aa7df-973">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="aa7df-973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="aa7df-974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-974">Az.Sql</span></span>
* <span data-ttu-id="aa7df-975">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="aa7df-975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="aa7df-976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aa7df-976">Az.Storage</span></span>
* <span data-ttu-id="aa7df-977">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="aa7df-977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="aa7df-978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="aa7df-978">New-AzStorageContext</span></span>
* <span data-ttu-id="aa7df-979">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="aa7df-979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="aa7df-980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="aa7df-980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aa7df-981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aa7df-981">Az.Websites</span></span>
* <span data-ttu-id="aa7df-982">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="aa7df-982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="aa7df-983">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="aa7df-983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="aa7df-984">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="aa7df-984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="aa7df-985">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="aa7df-985">General</span></span>

- <span data-ttu-id="aa7df-986">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="aa7df-986">General Availability of Az Module</span></span>
- <span data-ttu-id="aa7df-987">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-987">Online help for each module</span></span>
- <span data-ttu-id="aa7df-988">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="aa7df-988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="aa7df-989">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aa7df-989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="aa7df-990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aa7df-990">Az.Accounts</span></span>
- <span data-ttu-id="aa7df-991">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="aa7df-991">Changed from Az.Profile</span></span>
- <span data-ttu-id="aa7df-992">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="aa7df-993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="aa7df-993">Az.ApiManagement</span></span>
- <span data-ttu-id="aa7df-994">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="aa7df-994">Fixes for #7002</span></span>
- <span data-ttu-id="aa7df-995">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aa7df-995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="aa7df-996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="aa7df-996">Az.Batch</span></span>
- <span data-ttu-id="aa7df-997">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="aa7df-997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="aa7df-998">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="aa7df-998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="aa7df-999">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aa7df-999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="aa7df-1000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="aa7df-1000">Az.Billing</span></span>
- <span data-ttu-id="aa7df-1001">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="aa7df-1002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-1002">Az.CognitivServices</span></span>
- <span data-ttu-id="aa7df-1003">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="aa7df-1004">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="aa7df-1005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="aa7df-1005">Az.ContainerInstance</span></span>
- <span data-ttu-id="aa7df-1006">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="aa7df-1006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="aa7df-1007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="aa7df-1007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="aa7df-1008">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aa7df-1008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="aa7df-1009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aa7df-1009">Az.DataLakeStore</span></span>
- <span data-ttu-id="aa7df-1010">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aa7df-1010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="aa7df-1011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="aa7df-1011">Az.Monitor</span></span>
- <span data-ttu-id="aa7df-1012">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aa7df-1012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="aa7df-1013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="aa7df-1013">Az.KeyVault</span></span>
- <span data-ttu-id="aa7df-1014">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="aa7df-1015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="aa7df-1015">Az.MachineLearning</span></span>
- <span data-ttu-id="aa7df-1016">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="aa7df-1016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="aa7df-1017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="aa7df-1017">Az.Media</span></span>
- <span data-ttu-id="aa7df-1018">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="aa7df-1018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="aa7df-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-1019">Az.Network</span></span>
<span data-ttu-id="aa7df-1020">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="aa7df-1021">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="aa7df-1021">New cmdlets added:</span></span>
        - <span data-ttu-id="aa7df-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aa7df-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aa7df-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aa7df-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aa7df-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aa7df-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aa7df-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aa7df-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aa7df-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="aa7df-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="aa7df-1027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="aa7df-1027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="aa7df-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="aa7df-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="aa7df-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa7df-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="aa7df-1030">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="aa7df-1030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="aa7df-1031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aa7df-1031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="aa7df-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="aa7df-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="aa7df-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="aa7df-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="aa7df-1034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aa7df-1034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="aa7df-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="aa7df-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="aa7df-1036">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="aa7df-1037">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="aa7df-1037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="aa7df-1038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aa7df-1038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="aa7df-1039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aa7df-1039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="aa7df-1040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="aa7df-1040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="aa7df-1041">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="aa7df-1041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="aa7df-1042">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aa7df-1042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="aa7df-1043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="aa7df-1043">Az.OperationalInsights</span></span>
- <span data-ttu-id="aa7df-1044">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aa7df-1044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="aa7df-1045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="aa7df-1045">Az.Profile</span></span>
- <span data-ttu-id="aa7df-1046">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aa7df-1046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="aa7df-1047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-1047">Az.RecoveryServices</span></span>
- <span data-ttu-id="aa7df-1048">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aa7df-1048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="aa7df-1049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-1049">Az.Resources</span></span>
- <span data-ttu-id="aa7df-1050">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aa7df-1050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="aa7df-1051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aa7df-1051">Az.ServiceFabric</span></span>
- <span data-ttu-id="aa7df-1052">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="aa7df-1052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="aa7df-1053">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aa7df-1053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="aa7df-1054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="aa7df-1054">Az.SIgnalR</span></span>
- <span data-ttu-id="aa7df-1055">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="aa7df-1055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="aa7df-1056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-1056">Az.Sql</span></span>
- <span data-ttu-id="aa7df-1057">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-1057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="aa7df-1058">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="aa7df-1058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="aa7df-1059">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aa7df-1059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="aa7df-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aa7df-1060">Az.Storage</span></span>
- <span data-ttu-id="aa7df-1061">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aa7df-1061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="aa7df-1062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aa7df-1062">Az.Websites</span></span>
- <span data-ttu-id="aa7df-1063">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="aa7df-1063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="aa7df-1064">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="aa7df-1064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="aa7df-1065">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="aa7df-1065">General</span></span>

* <span data-ttu-id="aa7df-1066">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-1066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="aa7df-1067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-1067">Az.Compute</span></span>

* <span data-ttu-id="aa7df-1068">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="aa7df-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aa7df-1069">Az.DataLakeStore</span></span>

* <span data-ttu-id="aa7df-1070">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="aa7df-1070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="aa7df-1071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="aa7df-1071">Az.FrontDoor</span></span>

* <span data-ttu-id="aa7df-1072">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-1072">Fixed some broken links</span></span>
    - <span data-ttu-id="aa7df-1073">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="aa7df-1074">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="aa7df-1075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-1075">Az.RecoveryServices</span></span>

* <span data-ttu-id="aa7df-1076">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="aa7df-1077">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="aa7df-1078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-1078">Az.Resources</span></span>

* <span data-ttu-id="aa7df-1079">https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-1079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="aa7df-1080">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="aa7df-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-1081">Az.Sql</span></span>

* <span data-ttu-id="aa7df-1082">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-1082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="aa7df-1083">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="aa7df-1083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="aa7df-1084">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="aa7df-1085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aa7df-1085">Az.Storage</span></span>

* <span data-ttu-id="aa7df-1086">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-1086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="aa7df-1087">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="aa7df-1088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="aa7df-1088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="aa7df-1089">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="aa7df-1089">Support Static Website configuration</span></span>
    - <span data-ttu-id="aa7df-1090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="aa7df-1090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="aa7df-1091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="aa7df-1091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="aa7df-1092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aa7df-1092">Az.Websites</span></span>

* <span data-ttu-id="aa7df-1093">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="aa7df-1093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="aa7df-1094">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="aa7df-1095">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="aa7df-1096">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="aa7df-1096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="aa7df-1097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="aa7df-1097">Az.ApiManagement</span></span>
* <span data-ttu-id="aa7df-1098">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="aa7df-1099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="aa7df-1099">Az.Automation</span></span>
* <span data-ttu-id="aa7df-1100">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="aa7df-1101">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="aa7df-1102">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="aa7df-1103">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="aa7df-1104">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="aa7df-1105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-1105">Az.Compute</span></span>
* <span data-ttu-id="aa7df-1106">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="aa7df-1107">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="aa7df-1108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="aa7df-1108">Az.ContainerInstance</span></span>
* <span data-ttu-id="aa7df-1109">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="aa7df-1110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="aa7df-1110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="aa7df-1111">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="aa7df-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-1112">Az.Network</span></span>
* <span data-ttu-id="aa7df-1113">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="aa7df-1114">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="aa7df-1115">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="aa7df-1116">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="aa7df-1117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="aa7df-1117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="aa7df-1118">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="aa7df-1119">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="aa7df-1120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="aa7df-1120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="aa7df-1121">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="aa7df-1122">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="aa7df-1123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="aa7df-1123">Az.Relay</span></span>
* <span data-ttu-id="aa7df-1124">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="aa7df-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-1125">Az.Resources</span></span>
* <span data-ttu-id="aa7df-1126">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="aa7df-1127">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="aa7df-1128">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="aa7df-1129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aa7df-1129">Az.ServiceFabric</span></span>
* <span data-ttu-id="aa7df-1130">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="aa7df-1131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-1131">Az.Sql</span></span>
* <span data-ttu-id="aa7df-1132">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="aa7df-1133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aa7df-1133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aa7df-1134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aa7df-1134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aa7df-1135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aa7df-1135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aa7df-1136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aa7df-1136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="aa7df-1137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aa7df-1137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="aa7df-1138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aa7df-1138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="aa7df-1139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aa7df-1139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="aa7df-1140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="aa7df-1140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="aa7df-1141">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="aa7df-1142">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="aa7df-1143">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="aa7df-1144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="aa7df-1145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="aa7df-1146">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="aa7df-1147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="aa7df-1148">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="aa7df-1149">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="aa7df-1149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="aa7df-1150">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="aa7df-1150">General</span></span>
* <span data-ttu-id="aa7df-1151">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="aa7df-1152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="aa7df-1152">Az.Profile</span></span>
* <span data-ttu-id="aa7df-1153">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="aa7df-1154">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="aa7df-1154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="aa7df-1155">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="aa7df-1155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="aa7df-1156">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="aa7df-1156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="aa7df-1157">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="aa7df-1157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="aa7df-1158">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="aa7df-1158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="aa7df-1159">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="aa7df-1159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="aa7df-1160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-1160">Az.CognitiveServices</span></span>
* <span data-ttu-id="aa7df-1161">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-1162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-1162">Az.Compute</span></span>
* <span data-ttu-id="aa7df-1163">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="aa7df-1163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="aa7df-1164">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="aa7df-1164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="aa7df-1165">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aa7df-1166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aa7df-1166">Az.DataLakeStore</span></span>
* <span data-ttu-id="aa7df-1167">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="aa7df-1168">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="aa7df-1169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="aa7df-1169">Az.Insights</span></span>
* <span data-ttu-id="aa7df-1170">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="aa7df-1170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="aa7df-1171">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="aa7df-1171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="aa7df-1172">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="aa7df-1172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="aa7df-1173">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="aa7df-1173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aa7df-1174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-1174">Az.Network</span></span>
* <span data-ttu-id="aa7df-1175">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="aa7df-1175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="aa7df-1176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="aa7df-1176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="aa7df-1177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="aa7df-1177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="aa7df-1178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="aa7df-1178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="aa7df-1179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="aa7df-1179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="aa7df-1180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="aa7df-1180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="aa7df-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="aa7df-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="aa7df-1182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="aa7df-1182">Az.PolicyInsights</span></span>
* <span data-ttu-id="aa7df-1183">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="aa7df-1183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="aa7df-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-1184">Az.Resources</span></span>
* <span data-ttu-id="aa7df-1185">https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="aa7df-1185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="aa7df-1186">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="aa7df-1186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="aa7df-1187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="aa7df-1187">Az.ServiceBus</span></span>
* <span data-ttu-id="aa7df-1188">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="aa7df-1189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aa7df-1189">Az.ServiceFabric</span></span>
* <span data-ttu-id="aa7df-1190">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="aa7df-1191">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="aa7df-1191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="aa7df-1192">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="aa7df-1192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="aa7df-1193">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="aa7df-1193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="aa7df-1194">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="aa7df-1195">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="aa7df-1195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="aa7df-1196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="aa7df-1196">Az.Profile</span></span>
* <span data-ttu-id="aa7df-1197">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="aa7df-1198">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-1199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-1199">Az.Compute</span></span>
* <span data-ttu-id="aa7df-1200">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="aa7df-1201">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="aa7df-1202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="aa7df-1202">Az.DataLakeStore</span></span>
* <span data-ttu-id="aa7df-1203">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="aa7df-1203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="aa7df-1204">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="aa7df-1205">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="aa7df-1206">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="aa7df-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aa7df-1208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-1208">Az.Network</span></span>
* <span data-ttu-id="aa7df-1209">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="aa7df-1210">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="aa7df-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-1211">Az.Resources</span></span>
* <span data-ttu-id="aa7df-1212">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="aa7df-1212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="aa7df-1213">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="aa7df-1214">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="aa7df-1214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="aa7df-1215">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="aa7df-1215">Azure.Storage</span></span>
* <span data-ttu-id="aa7df-1216">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="aa7df-1216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="aa7df-1217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="aa7df-1217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="aa7df-1218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="aa7df-1218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="aa7df-1219">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="aa7df-1220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="aa7df-1220">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="aa7df-1221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="aa7df-1221">Az.CognitiveServices</span></span>
* <span data-ttu-id="aa7df-1222">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="aa7df-1223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="aa7df-1223">Az.Compute</span></span>
* <span data-ttu-id="aa7df-1224">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="aa7df-1225">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="aa7df-1226">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="aa7df-1226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="aa7df-1227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="aa7df-1227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="aa7df-1228">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="aa7df-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="aa7df-1229">Az.Network</span></span>
* <span data-ttu-id="aa7df-1230">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="aa7df-1231">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="aa7df-1231">new cmdlets added</span></span>
    - <span data-ttu-id="aa7df-1232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aa7df-1232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="aa7df-1233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aa7df-1233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="aa7df-1234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aa7df-1234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="aa7df-1235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="aa7df-1235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="aa7df-1236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="aa7df-1236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="aa7df-1237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="aa7df-1237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="aa7df-1238">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="aa7df-1238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="aa7df-1239">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="aa7df-1239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="aa7df-1240">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="aa7df-1240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="aa7df-1241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="aa7df-1241">Az.RedisCache</span></span>
* <span data-ttu-id="aa7df-1242">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="aa7df-1242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="aa7df-1243">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-1243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="aa7df-1244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aa7df-1244">Az.Resources</span></span>
* <span data-ttu-id="aa7df-1245">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="aa7df-1245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="aa7df-1246">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="aa7df-1246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="aa7df-1247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="aa7df-1247">Az.Sql</span></span>
* <span data-ttu-id="aa7df-1248">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="aa7df-1248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="aa7df-1249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="aa7df-1249">Az.Websites</span></span>
* <span data-ttu-id="aa7df-1250">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="aa7df-1250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="aa7df-1251">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="aa7df-1251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="aa7df-1252">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="aa7df-1252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="aa7df-1253">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="aa7df-1253">Initial Release</span></span>