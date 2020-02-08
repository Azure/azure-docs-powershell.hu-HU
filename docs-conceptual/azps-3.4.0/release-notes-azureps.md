---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 694439934afb41b465a89188d59bc964db3c0032
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002673"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="fe2d3-103">Az Azure PowerShell kibocsátási megjegyzései</span><span class="sxs-lookup"><span data-stu-id="fe2d3-103">Azure PowerShell release notes</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="fe2d3-104">3.4.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="fe2d3-104">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fe2d3-105">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-105">Highlights since the last major release</span></span>
* <span data-ttu-id="fe2d3-106">Megjelent az Az.CosmosDB 0.1.0-s kezdeti verziója</span><span class="sxs-lookup"><span data-stu-id="fe2d3-106">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="fe2d3-107">Az.Network ConnectionMonitor V2 támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-107">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-108">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-109">A környezet automatikus mentésének letiltása, ha az AzureRmContext.json nem érhető el</span><span class="sxs-lookup"><span data-stu-id="fe2d3-109">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="fe2d3-110">Az Azure Powershell Common referenciájának frissítése 1.3.5-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="fe2d3-110">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="fe2d3-111">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe2d3-111">Az.ApiManagement</span></span>
* <span data-ttu-id="fe2d3-112">**Get-AzApiManagementApiSchema** Az API-val társított Open-API séma kijavítása   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="fe2d3-112">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="fe2d3-113">**New-AzApiManagementProduct**\* és **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="fe2d3-113">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="fe2d3-114">https://github.com/Azure/azure-powershell/issues/10472 dokumentációja kijavítva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-114">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="fe2d3-115">**Set-AzApiManagementApi** A ServiceUrl parancsmaggal való frissítését bemutató példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-115">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-116">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-117">A virtuális gép állapotának korlátozása 100 értékre, hogy ne legyen szabályozás, ha a Get-AzVM -Status a virtuális gép neve nélkül lett végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-117">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="fe2d3-118">Update-AzDiskEncryptionSet parancsmagok hozzáadása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-118">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="fe2d3-119">Az EncryptionType és a DiskEncryptionSetId paraméterek hozzáadása a következő parancsmagokhoz:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-119">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="fe2d3-120">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-120">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="fe2d3-121">A ColocationStatus paraméter hozzáadva a Get-AzProximityPlacementGroup parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-121">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fe2d3-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe2d3-122">Az.DataFactory</span></span>
* <span data-ttu-id="fe2d3-123">Az ADF .Net SDK frissítve lett a 4.7.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="fe2d3-123">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="fe2d3-124">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="fe2d3-124">Az.DeploymentManager</span></span>
* <span data-ttu-id="fe2d3-125">LIST műveletek hozzáadása az erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-125">Adds LIST operations for resources</span></span>
* <span data-ttu-id="fe2d3-126">Műveletek végrehajtásának lehetősége az állapotellenőrzés lépésein</span><span class="sxs-lookup"><span data-stu-id="fe2d3-126">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="fe2d3-127">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fe2d3-127">Az.HDInsight</span></span>
* <span data-ttu-id="fe2d3-128">A New-AzHDInsightCluster dokumentációs hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-128">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fe2d3-129">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fe2d3-129">Az.KeyVault</span></span>
* <span data-ttu-id="fe2d3-130">Name alias hozzáadása a VaultName attribútumhoz, hogy a Remove-AzureKeyVault konzisztens legyen a New-AzureKeyVault paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-130">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-131">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-131">Az.Network</span></span>
* <span data-ttu-id="fe2d3-132">Új példa hozzáadva a Set-AzNetworkWatcherConfigFlowLog.md fájlhoz a Traffic Analytics-letiltási forgatókönyv szemléltetésére.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-132">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="fe2d3-133">Felügyeleti IP-konfiguráció támogatás hozzáadva az Azure Firewallhoz – egy dedikált alhálózat és nyilvános IP-cím, amelyet a tűzfal a forgalom felügyeléséhez használni fog</span><span class="sxs-lookup"><span data-stu-id="fe2d3-133">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="fe2d3-134">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-134">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="fe2d3-135">Hozzá lett adva a (nem kötelező) -PublicIpAddress-ManagementPublicIpAddress paraméter, amely egy nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="fe2d3-135">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="fe2d3-136">Hozzá lett adva a SetManagementIpConfiguration metódus a tűzfalobjektumok esetében – nyilvános IP-cím-objektumokat fogad el bemeneti adatként – az alhálózat nevének AzureFirewallManagementSubnet értéknek kell lennie</span><span class="sxs-lookup"><span data-stu-id="fe2d3-136">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="fe2d3-137">A Get-AzNetworkSecurityGroup példái javítva, hogy hálózati biztonsági csoportok példáit tartalmazzák hálózati adapterek helyett.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-137">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="fe2d3-138">Javítottunk egy elírást a New-AzVpnSite parancsban, amely megakadályozta, hogy az erőforrásazonosító-kiegészítő kiegészítsen egy paramétert.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-138">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="fe2d3-139">Az Application Gateway szabály-újraírási műveletkészletének URL-konfigurálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-139">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="fe2d3-140">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-140">New cmdlets added:</span></span>
        - <span data-ttu-id="fe2d3-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe2d3-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="fe2d3-142">A parancsmagok frissültek a nem kötelező UrlConfiguration paraméterrel</span><span class="sxs-lookup"><span data-stu-id="fe2d3-142">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="fe2d3-143">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="fe2d3-143">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="fe2d3-144">A Network Watcher Connection Monitor 2-es verziójú erőforrások támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-144">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fe2d3-145">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fe2d3-145">Az.PolicyInsights</span></span>
* <span data-ttu-id="fe2d3-146">A javítandó erőforrások azonosítása előtti megfelelőségértékelés támogatása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-146">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="fe2d3-147">-ResourceDiscoverMode paraméter hozzáadása a Start-AzPolicyRemediation parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-147">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="fe2d3-148">A szabályzatok metaadat-erőforrásainak elérésére szolgáló Get-AzPolicyMetadata parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-148">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="fe2d3-149">A Get-AzPolicyState és a Get-AzPolicyStateSummary frissült a 2019-10-01 API-verzióhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-149">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-150">Az.RecoveryServices</span></span>
* <span data-ttu-id="fe2d3-151">Azure Site Recovery-támogatás a replikált lemezek eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-151">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="fe2d3-152">Hozzáadott Azure Backup-támogatás a helyreállítási tárak létrehozása közbeni címkehozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-152">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-153">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-153">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-154">A -Scope választható a \*-AzPolicyAssignment parancsmagokban; az alapértelmezett érték a környezeti előfizetés</span><span class="sxs-lookup"><span data-stu-id="fe2d3-154">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="fe2d3-155">Az ADServicePrincipal jelszó és kulcs típusú hitelesítő adatokkal való létrehozását szemléltető példák hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-155">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-156">Az.Sql</span></span>
<span data-ttu-id="fe2d3-157">A New-AzSqlDatabaseSecondary parancsmag javítva, hogy a PartnerDatabaseName létezését ellenőrizze a DatabaseName létezése helyett.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-157">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-158">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-159">A Table/Queue Encryption Keytype készlet beállításának támogatása Storage-fiók létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-159">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="fe2d3-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe2d3-160">New-AzStorageAccount</span></span>
* <span data-ttu-id="fe2d3-161">RequestId megjelenítése, ha a StorageException nem rendelkezik ExtendedErrorInformation paraméterrel</span><span class="sxs-lookup"><span data-stu-id="fe2d3-161">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="fe2d3-162">A Start-AzStorageBlobCopy parancsmag 6. példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-162">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fe2d3-163">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-163">Az.Websites</span></span>
* <span data-ttu-id="fe2d3-164">A Set-AzWebapp és a Set-AzWebappSlot támogatja az AlwaysOn, a MinTls és a FtpsState tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="fe2d3-164">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="fe2d3-165">Javítva a hiba, amely miatt a HttpsOnly és az AppservicePlan Set-AzWebApp paranccsal történő egyidejű módosításakor a HttpsOnly paraméter alaphelyzetbe állt.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-165">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="fe2d3-166">3.3.0 – 2020. január</span><span class="sxs-lookup"><span data-stu-id="fe2d3-166">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-167">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-167">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-168">Frissítve lettek az Add-AzEnvironment és Set-AzEnvironment parancsmagok, amelyek mostantól elfogadják az AzureAttestationServiceEndpointResourceId és AzureAttestationServiceEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="fe2d3-168">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fe2d3-169">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fe2d3-169">Az.Cdn</span></span>
* <span data-ttu-id="fe2d3-170">A hibaválasz részleteinek láthatóvá tétele a New-AzCdnEndpoint parancsmagban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-170">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-171">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-172">Javítva lett a Set-AzVMCustomScriptExtension parancsmag az olyan virtuális gépek esetében, amelyek felügyelt operációsrendszer-lemeze nem rendelkezik operációsrendszer-profillal.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-172">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="fe2d3-173">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fe2d3-173">Az.ContainerInstance</span></span>
* <span data-ttu-id="fe2d3-174">Javítva lettek a New-AzContainerGroup parancsmagpélda által használt paraméternevek</span><span class="sxs-lookup"><span data-stu-id="fe2d3-174">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="fe2d3-175">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="fe2d3-175">Az.DataBoxEdge</span></span>
* <span data-ttu-id="fe2d3-176">Hozzá lett adva a Get-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="fe2d3-176">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="fe2d3-177">Az Edge Storage-tároló lekérése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-177">Get the Edge Storage Container</span></span>
* <span data-ttu-id="fe2d3-178">Hozzá lett adva a New-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="fe2d3-178">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="fe2d3-179">Új Edge Storage-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-179">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="fe2d3-180">Hozzá lett adva a Remove-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="fe2d3-180">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="fe2d3-181">Az Edge Storage-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-181">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="fe2d3-182">Hozzá lett adva az Invoke-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="fe2d3-182">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="fe2d3-183">Meghívási művelet az Edge Storage-tárolóban lévő adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-183">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="fe2d3-184">Hozzá lett adva a Get-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="fe2d3-184">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="fe2d3-185">Az Edge Storage-fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-185">Get the Edge Storage Account</span></span>
* <span data-ttu-id="fe2d3-186">Hozzá lett adva a New-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="fe2d3-186">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="fe2d3-187">Új Edge Storage-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-187">Create new Edge Storage Account</span></span>
* <span data-ttu-id="fe2d3-188">Hozzá lett adva a Remove-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="fe2d3-188">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="fe2d3-189">Az Edge Storage-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-189">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="fe2d3-190">Hozzá lett adva az Invoke-AzDataBoxEdgeShare parancsmag</span><span class="sxs-lookup"><span data-stu-id="fe2d3-190">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="fe2d3-191">Meghívási művelet a megosztott adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-191">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="fe2d3-192">Hozzá lett adva a Set-AzDataBoxEdgeStorageAccountCredential parancsmag</span><span class="sxs-lookup"><span data-stu-id="fe2d3-192">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="fe2d3-193">Az Az.DataBoxEdge tárfiók hitelesítő adatainak beállítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-193">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fe2d3-194">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe2d3-194">Az.DataFactory</span></span>
* <span data-ttu-id="fe2d3-195">Hozzá lettek adva az AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId és VersionStatus tulajdonságok a Get-AzDataFactoryV2IntegrationRuntime parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-195">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="fe2d3-196">Az ADF .Net SDK frissítve lett a 4.6.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="fe2d3-196">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="fe2d3-197">A PublicIPs paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz statikus nyilvános IP-címekkel rendelkező Azure-SSIS IR létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-197">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="fe2d3-198">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="fe2d3-198">Az.DevTestLabs</span></span>
* <span data-ttu-id="fe2d3-199">A hibás hivatkozás el lett távolítva a Get-AzDtlAllowedVMSizesPolicy.md parancsmagból</span><span class="sxs-lookup"><span data-stu-id="fe2d3-199">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fe2d3-200">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fe2d3-200">Az.EventHub</span></span>
* <span data-ttu-id="fe2d3-201">A 10634-es hiba javítása: Ki lett javítva a nullértékű objektumhivatkozás a remove eventhubnamespace esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-201">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="fe2d3-202">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fe2d3-202">Az.HDInsight</span></span>
* <span data-ttu-id="fe2d3-203">Ki lett javítva az Invoke-AzHDInsightHiveJob.md hibája.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-203">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="fe2d3-204">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="fe2d3-204">Az.MachineLearning</span></span>
* <span data-ttu-id="fe2d3-205">El lettek távolítva az alábbi parancsmagok, mivel a MachineLearningCompute már nem érhető el</span><span class="sxs-lookup"><span data-stu-id="fe2d3-205">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="fe2d3-206">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="fe2d3-206">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="fe2d3-207">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="fe2d3-207">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="fe2d3-208">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="fe2d3-208">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="fe2d3-209">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="fe2d3-209">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="fe2d3-210">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="fe2d3-210">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="fe2d3-211">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="fe2d3-211">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="fe2d3-212">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="fe2d3-212">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-213">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-213">Az.Network</span></span>
* <span data-ttu-id="fe2d3-214">Frissítve lett a Microsoft.Azure.Management.Sql függősége: 1.36-preview helyett 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="fe2d3-214">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-215">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-215">Az.RecoveryServices</span></span>
* <span data-ttu-id="fe2d3-216">Módosított Azure Site Recovery-támogatás azon felügyelt lemezeken található, inaktív állapotban titkosított virtuális gépeknél, amelyekhez felhasználó által kezelt kulcsok tartoznak a következő esetében: Azure – Azure-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-216">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="fe2d3-217">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a védelem engedélyezése során a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-217">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="fe2d3-218">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a lemez szintjén a védelem engedélyezéséhez a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-218">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="fe2d3-219">Azure Site Recovery-támogatás a Replikációval védett, lemeztitkosítási csoportleképezéssel ellátott elemek frissítéséhez a következő esetében: HyperV – Azure.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-219">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-220">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-221">Javítva lett egy hiba a Remove-AzTag súgódokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-221">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-222">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-222">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-223">Javítva lett a sebezhetőségi felmérés csoportszintű alapkonfigurációs parancsmagjainak működése: az Azure-adatbázis főadatbázisában használható, a felügyelt példányok rendszeradatbázisaiban korlátozott.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-223">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="fe2d3-224">Ki lett javítva egy hiba az SQL-példányok feladatátvételi csoportjainak létrehozása esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-224">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="fe2d3-225">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fe2d3-225">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="fe2d3-226">Hozzá lett adva a DR, mint új érvényes licenctípus</span><span class="sxs-lookup"><span data-stu-id="fe2d3-226">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-227">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-227">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-228">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet a DefaultAction értékének módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-228">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="fe2d3-229">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe2d3-229">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="fe2d3-230">Támogatott a tárfiók legutóbbi szinkronizálási időpontjának lekérése a get-AzureRMStorageAccount parancsmag -IncludeGeoReplicationStats paraméterrel való futtatásával</span><span class="sxs-lookup"><span data-stu-id="fe2d3-230">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="fe2d3-231">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe2d3-231">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="fe2d3-232">3.2.0 – 2019. december</span><span class="sxs-lookup"><span data-stu-id="fe2d3-232">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="fe2d3-233">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="fe2d3-233">General</span></span>
* <span data-ttu-id="fe2d3-234">A .psd1 hivatkozásai frissítve, hogy minden modulhoz a relatív elérési utat használják</span><span class="sxs-lookup"><span data-stu-id="fe2d3-234">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-235">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-236">A megfelelő felhasználói ügynök beállítva az ügyféloldali telemetriához az Az 4.0 előzetes verziójában</span><span class="sxs-lookup"><span data-stu-id="fe2d3-236">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="fe2d3-237">Felhasználóbarát hibaüzenet megjelenítése, ha az Az 4.0 előzetes verziójában a környezet null értékű</span><span class="sxs-lookup"><span data-stu-id="fe2d3-237">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="fe2d3-238">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fe2d3-238">Az.Batch</span></span>
* <span data-ttu-id="fe2d3-239">Ki lett javítva a [10602-es](https://github.com/Azure/azure-powershell/issues/10602) számú hiba, amely miatt a **New-AzBatchPool** nem megfelelően küldte el a „VirtualMachineConfiguration.ContainerConfiguration” és a „VirtualMachineConfiguration.DataDisks” paramétereket a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-239">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fe2d3-240">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe2d3-240">Az.DataFactory</span></span>
* <span data-ttu-id="fe2d3-241">Az ADF .Net SDK a 4.5.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="fe2d3-241">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="fe2d3-242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-242">Az.FrontDoor</span></span>
* <span data-ttu-id="fe2d3-243">A WAF felügyeleti szabályok kizárása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="fe2d3-243">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="fe2d3-244">Hozzá lett adva a SocketAddr automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-244">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="fe2d3-245">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="fe2d3-245">Az.HealthcareApis</span></span>
* <span data-ttu-id="fe2d3-246">Kivételkezelés</span><span class="sxs-lookup"><span data-stu-id="fe2d3-246">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fe2d3-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fe2d3-247">Az.KeyVault</span></span>
* <span data-ttu-id="fe2d3-248">Ki lett javítva az esetleg nem beállított értékek hozzáférésével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="fe2d3-248">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="fe2d3-249">Az elliptikus görbéjű titkosítási tanúsítványok kezelése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-249">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="fe2d3-250">A görbe tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-250">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fe2d3-251">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-251">Az.Monitor</span></span>
* <span data-ttu-id="fe2d3-252">Opcionális argumentum hozzáadva a Diagnosztikai beállítások hozzáadása parancshoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-252">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="fe2d3-253">Ez egy kapcsoló argumentum, amely megléte esetén azt jelzi, hogy a Log Analyticsbe történő exportálást egy rögzített séma (más néven</span><span class="sxs-lookup"><span data-stu-id="fe2d3-253">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="fe2d3-254">dedikált adattípus) szerint kell végrehajtani</span><span class="sxs-lookup"><span data-stu-id="fe2d3-254">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-255">Az.Network</span></span>
* <span data-ttu-id="fe2d3-256">Támogatás az Ip-csoportok számára az AzureFirewall alkalmazás, valamint a Nat- és a hálózati szabályok esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-256">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-257">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-258">Ki lett javítva az a hiba, amely miatt a sablonalapú üzembe helyezés során a sablonparamétert nem lehet olvasni, ha a sablonparaméter és egy beépített paraméter neve között névütközés áll fenn.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-258">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="fe2d3-259">Frissültek a szabályzat parancsmagjai a 2019. 09. 01. dátumú új API-verzió használatára, amely bevezeti a szabályzatkészlet-definíciókon belüli csoportos támogatást.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-259">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-260">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-261">Frissítve lett a sebezhetőségi felmérés automatikus engedélyezéséhez szükséges tárterület létrehozása a Storagev2-ben</span><span class="sxs-lookup"><span data-stu-id="fe2d3-261">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-262">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-262">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-263">A blob-/tárolóidentitás-alapú SAS-token Oauth-hitelesítésen alapuló Storage-környezettel való létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-263">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="fe2d3-264">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="fe2d3-264">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="fe2d3-265">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="fe2d3-265">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="fe2d3-266">Támogatott lett a tárfiókhoz tartozó felhasználódelegálási kulcsok visszavonása, így minden identitásalapú SAS-token visszavonható</span><span class="sxs-lookup"><span data-stu-id="fe2d3-266">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="fe2d3-267">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="fe2d3-267">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="fe2d3-268">Frissítés a Microsoft.Azure.Management.Storage 14.2.0-s verziójára az új API-verzió (2019. 06. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-268">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="fe2d3-269">A QuotaGiB (gigabájtban megadott megosztási kvóta) esetében támogatottak az 5120-nál nagyobb értékek a fájlmegosztási parancsmagok felügyeleti síkján, és hozzá lett adva a Quota paraméteralias a QuotaGiB paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-269">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="fe2d3-270">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fe2d3-270">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="fe2d3-271">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fe2d3-271">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="fe2d3-272">A „QuotaGiB” paraméteralias hozzáadva a „kvóta” paraméterhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-272">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="fe2d3-273">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="fe2d3-273">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="fe2d3-274">Ki lett javítva az a hiba, amely miatt a Set-AzStorageContainerAcl parancsmag el tudta távolítani a tárolt hozzáférési szabályzatot</span><span class="sxs-lookup"><span data-stu-id="fe2d3-274">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="fe2d3-275">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="fe2d3-275">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="fe2d3-276">3.1.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="fe2d3-276">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fe2d3-277">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-277">Highlights since the last major release</span></span>
* <span data-ttu-id="fe2d3-278">Az.DataBoxEdge 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-278">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="fe2d3-279">Az.SqlVirtualMachine 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-279">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-280">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-281">A virtuális gépek Reapply funkciója</span><span class="sxs-lookup"><span data-stu-id="fe2d3-281">VM Reapply feature</span></span>
    - <span data-ttu-id="fe2d3-282">A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-282">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="fe2d3-283">A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-283">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="fe2d3-284">Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fe2d3-284">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="fe2d3-285">Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-285">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="fe2d3-286">A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-286">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="fe2d3-287">A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-287">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="fe2d3-288">A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező</span><span class="sxs-lookup"><span data-stu-id="fe2d3-288">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="fe2d3-289">A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="fe2d3-289">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="fe2d3-290">A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-290">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="fe2d3-291">A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-291">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="fe2d3-292">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="fe2d3-292">Az.DataBoxEdge</span></span>
* <span data-ttu-id="fe2d3-293">A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-293">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="fe2d3-294">Megrendelés lekérése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-294">Get the Order</span></span>
* <span data-ttu-id="fe2d3-295">A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-295">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="fe2d3-296">Új megrendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-296">Create new Order</span></span>
* <span data-ttu-id="fe2d3-297">A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-297">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="fe2d3-298">Megrendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-298">Remove the Order</span></span>
* <span data-ttu-id="fe2d3-299">`New-AzDataBoxEdgeShare` parancsmag módosítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-299">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="fe2d3-300">Mostantól helyi megosztást hoz létre</span><span class="sxs-lookup"><span data-stu-id="fe2d3-300">Now creates Local Share</span></span>
* <span data-ttu-id="fe2d3-301">A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-301">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="fe2d3-302">Mostantól az IotRole leképezhető a Share-re</span><span class="sxs-lookup"><span data-stu-id="fe2d3-302">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="fe2d3-303">A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-303">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="fe2d3-304">Frissítések keresésének, letöltésének, telepítésének indítása az eszközön</span><span class="sxs-lookup"><span data-stu-id="fe2d3-304">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="fe2d3-305">A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-305">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="fe2d3-306">Triggerek információinak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-306">Gets the information about Triggers</span></span>
* <span data-ttu-id="fe2d3-307">A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-307">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="fe2d3-308">Új triggerek létrehozása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-308">Create new Triggers</span></span>
* <span data-ttu-id="fe2d3-309">A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-309">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="fe2d3-310">Triggerek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-310">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fe2d3-311">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe2d3-311">Az.DataFactory</span></span>
* <span data-ttu-id="fe2d3-312">Az ADF .Net SDK a 4.4.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="fe2d3-312">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="fe2d3-313">Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-313">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fe2d3-314">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe2d3-314">Az.DataLakeStore</span></span>
* <span data-ttu-id="fe2d3-315">Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fe2d3-315">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fe2d3-316">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fe2d3-316">Az.EventHub</span></span>
* <span data-ttu-id="fe2d3-317">A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-317">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="fe2d3-318">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-318">Az.FrontDoor</span></span>
* <span data-ttu-id="fe2d3-319">Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="fe2d3-319">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="fe2d3-320">A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="fe2d3-320">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="fe2d3-321">Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-321">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="fe2d3-322">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="fe2d3-322">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-323">Az.Network</span></span>
* <span data-ttu-id="fe2d3-324">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-324">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="fe2d3-325">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="fe2d3-325">Az.PrivateDns</span></span>
* <span data-ttu-id="fe2d3-326">A PrivateDns .net sdk frissült az 1.0.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="fe2d3-326">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-327">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-327">Az.RecoveryServices</span></span>
* <span data-ttu-id="fe2d3-328">Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-328">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="fe2d3-329">Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-329">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="fe2d3-330">SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-330">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="fe2d3-331">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fe2d3-331">Az.RedisCache</span></span>
* <span data-ttu-id="fe2d3-332">A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-332">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="fe2d3-333">Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-333">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="fe2d3-334">Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-334">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-335">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-335">Az.Resources</span></span>
- <span data-ttu-id="fe2d3-336">Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-336">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="fe2d3-337">Frissült a létrehozási szabályzat definíciójának súgóbeli példája</span><span class="sxs-lookup"><span data-stu-id="fe2d3-337">Updated create policy definition help example</span></span>
- <span data-ttu-id="fe2d3-338">Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-338">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="fe2d3-339">Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-339">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="fe2d3-340">A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-340">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-341">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-341">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-342">Az adatbázisbeli ReadReplicaCount mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-342">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="fe2d3-343">A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén</span><span class="sxs-lookup"><span data-stu-id="fe2d3-343">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="fe2d3-344">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="fe2d3-344">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="fe2d3-345">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="fe2d3-345">General</span></span>
* <span data-ttu-id="fe2d3-346">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="fe2d3-346">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-347">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-348">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-348">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="fe2d3-349">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-349">Az.Advisor</span></span>
* <span data-ttu-id="fe2d3-350">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-350">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="fe2d3-351">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fe2d3-351">Az.Batch</span></span>
* <span data-ttu-id="fe2d3-352">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-352">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="fe2d3-353">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-353">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="fe2d3-354">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-354">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="fe2d3-355">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-355">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="fe2d3-356">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-356">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="fe2d3-357">Ezek az **New-AzBatchTask**`-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-357">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="fe2d3-358">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-358">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="fe2d3-359">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-359">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="fe2d3-360">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-360">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="fe2d3-361">A `PSApplication`**Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-361">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="fe2d3-362">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-362">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="fe2d3-363">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-363">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="fe2d3-364">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-364">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="fe2d3-365">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-365">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="fe2d3-366">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-366">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="fe2d3-367">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-367">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="fe2d3-368">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-368">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="fe2d3-369">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-369">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="fe2d3-370">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-370">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="fe2d3-371">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-371">This operation is no longer supported.</span></span>
* <span data-ttu-id="fe2d3-372">`PSCloudServiceConfiguration``TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-372">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="fe2d3-373">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-373">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="fe2d3-374">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-374">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="fe2d3-375">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-375">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="fe2d3-376">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-376">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="fe2d3-377">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-377">New non-verified images are also now returned.</span></span> <span data-ttu-id="fe2d3-378">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-378">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="fe2d3-379">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-379">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="fe2d3-380">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-380">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="fe2d3-381">Ez a `PSNetworkSecurityGroupRule``SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-381">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="fe2d3-382">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-382">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="fe2d3-383">Ezt a `PSTaskContainerSettings``WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-383">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="fe2d3-384">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-384">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="fe2d3-385">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-385">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="fe2d3-386">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-386">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="fe2d3-387">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-387">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fe2d3-388">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fe2d3-388">Az.Cdn</span></span>
* <span data-ttu-id="fe2d3-389">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-389">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="fe2d3-390">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-390">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-391">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-391">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-392">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="fe2d3-392">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="fe2d3-393">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="fe2d3-393">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="fe2d3-394">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="fe2d3-394">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="fe2d3-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fe2d3-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="fe2d3-396">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-396">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="fe2d3-397">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-397">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="fe2d3-398">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="fe2d3-398">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="fe2d3-399">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-399">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="fe2d3-400">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="fe2d3-400">Breaking changes</span></span>
    - <span data-ttu-id="fe2d3-401">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="fe2d3-401">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="fe2d3-402">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-402">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fe2d3-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe2d3-403">Az.DataFactory</span></span>
* <span data-ttu-id="fe2d3-404">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="fe2d3-404">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fe2d3-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe2d3-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="fe2d3-406">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="fe2d3-406">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="fe2d3-407">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-407">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="fe2d3-408">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-408">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="fe2d3-409">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-409">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="fe2d3-410">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-410">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="fe2d3-411">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-411">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="fe2d3-412">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-412">Az.FrontDoor</span></span>
* <span data-ttu-id="fe2d3-413">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-413">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="fe2d3-414">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fe2d3-414">Az.HDInsight</span></span>
* <span data-ttu-id="fe2d3-415">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-415">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="fe2d3-416">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-416">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="fe2d3-417">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="fe2d3-417">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="fe2d3-418">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-418">Removed five cmdlets:</span></span>
    - <span data-ttu-id="fe2d3-419">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="fe2d3-419">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="fe2d3-420">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="fe2d3-420">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="fe2d3-421">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="fe2d3-421">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="fe2d3-422">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="fe2d3-422">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="fe2d3-423">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="fe2d3-423">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="fe2d3-424">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-424">Added three cmdlets:</span></span>
    - <span data-ttu-id="fe2d3-425">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-425">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="fe2d3-426">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-426">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="fe2d3-427">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-427">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="fe2d3-428">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-428">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="fe2d3-429">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-429">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="fe2d3-430">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-430">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="fe2d3-431">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-431">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="fe2d3-432">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-432">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="fe2d3-433">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-433">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="fe2d3-434">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-434">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="fe2d3-435">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-435">Added some scenario test cases.</span></span>
* <span data-ttu-id="fe2d3-436">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-436">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fe2d3-437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fe2d3-437">Az.IotHub</span></span>
* <span data-ttu-id="fe2d3-438">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-438">Breaking changes:</span></span>
    - <span data-ttu-id="fe2d3-439">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-439">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="fe2d3-440">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-440">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="fe2d3-441">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-441">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="fe2d3-442">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-442">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="fe2d3-443">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-443">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="fe2d3-444">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-444">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="fe2d3-445">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-445">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="fe2d3-446">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-446">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="fe2d3-447">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-447">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="fe2d3-448">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-448">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="fe2d3-449">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-449">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="fe2d3-450">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-450">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-451">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-451">Az.RecoveryServices</span></span>
* <span data-ttu-id="fe2d3-452">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-452">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="fe2d3-453">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-453">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="fe2d3-454">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-454">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="fe2d3-455">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-455">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="fe2d3-456">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-456">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="fe2d3-457">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-457">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="fe2d3-458">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-458">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="fe2d3-459">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-459">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="fe2d3-460">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="fe2d3-460">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-461">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-462">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="fe2d3-462">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-463">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-463">Az.Network</span></span>
* <span data-ttu-id="fe2d3-464">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-464">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="fe2d3-465">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-465">Updated cmdlet:</span></span>
        - <span data-ttu-id="fe2d3-466">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-466">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fe2d3-467">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-467">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fe2d3-468">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-468">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fe2d3-469">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-469">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fe2d3-470">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-470">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="fe2d3-471">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-471">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="fe2d3-472">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-472">New cmdlet:</span></span>
        - <span data-ttu-id="fe2d3-473">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="fe2d3-473">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="fe2d3-474">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-474">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="fe2d3-475">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-475">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="fe2d3-476">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-476">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="fe2d3-477">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-477">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="fe2d3-478">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="fe2d3-478">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="fe2d3-479">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-479">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="fe2d3-480">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-480">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="fe2d3-481">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-481">New cmdlets added:</span></span>
        - <span data-ttu-id="fe2d3-482">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-482">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="fe2d3-483">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fe2d3-483">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="fe2d3-484">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fe2d3-484">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="fe2d3-485">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fe2d3-485">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="fe2d3-486">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="fe2d3-486">Set-AzVirtualHub</span></span>
* <span data-ttu-id="fe2d3-487">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-487">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="fe2d3-488">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-488">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="fe2d3-489">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-489">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="fe2d3-490">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-490">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="fe2d3-491">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-491">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="fe2d3-492">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-492">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="fe2d3-493">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-493">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="fe2d3-494">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-494">New cmdlets added:</span></span>
        - <span data-ttu-id="fe2d3-495">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-495">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="fe2d3-496">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-496">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="fe2d3-497">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-497">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="fe2d3-498">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-498">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="fe2d3-499">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-499">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="fe2d3-500">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-500">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="fe2d3-501">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-501">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="fe2d3-502">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-502">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="fe2d3-503">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-503">New cmdlets added:</span></span>
        - <span data-ttu-id="fe2d3-504">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="fe2d3-504">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="fe2d3-505">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="fe2d3-505">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="fe2d3-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="fe2d3-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="fe2d3-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="fe2d3-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="fe2d3-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="fe2d3-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="fe2d3-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe2d3-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="fe2d3-510">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-510">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="fe2d3-511">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-511">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="fe2d3-512">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-512">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="fe2d3-513">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-513">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="fe2d3-514">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-514">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="fe2d3-515">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-515">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="fe2d3-516">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-516">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="fe2d3-517">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-517">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="fe2d3-518">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="fe2d3-518">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="fe2d3-519">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-519">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="fe2d3-520">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-520">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="fe2d3-521">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-521">New cmdlets added:</span></span>
        - <span data-ttu-id="fe2d3-522">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="fe2d3-522">New-AzIpGroup</span></span>
        - <span data-ttu-id="fe2d3-523">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="fe2d3-523">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="fe2d3-524">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="fe2d3-524">Get-AzIpGroup</span></span>
        - <span data-ttu-id="fe2d3-525">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="fe2d3-525">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fe2d3-526">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fe2d3-526">Az.ServiceFabric</span></span>
* <span data-ttu-id="fe2d3-527">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-527">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-528">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-529">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-529">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="fe2d3-530">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-530">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="fe2d3-531">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-531">Removed deprecated aliases:</span></span>
* <span data-ttu-id="fe2d3-532">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="fe2d3-532">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="fe2d3-533">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="fe2d3-533">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="fe2d3-534">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-534">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="fe2d3-535">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-535">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="fe2d3-536">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="fe2d3-536">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="fe2d3-537">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-537">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-538">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-539">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="fe2d3-539">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="fe2d3-540">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe2d3-540">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="fe2d3-541">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe2d3-541">Set-AzStorageAccount</span></span>
* <span data-ttu-id="fe2d3-542">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="fe2d3-542">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="fe2d3-543">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="fe2d3-543">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="fe2d3-544">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="fe2d3-544">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="fe2d3-545">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="fe2d3-545">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="fe2d3-546">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="fe2d3-546">General</span></span>
* <span data-ttu-id="fe2d3-547">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="fe2d3-547">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-548">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-548">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-549">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-549">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="fe2d3-550">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe2d3-550">Az.ApiManagement</span></span>
* <span data-ttu-id="fe2d3-551">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="fe2d3-551">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="fe2d3-552">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="fe2d3-552">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fe2d3-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fe2d3-553">Az.Automation</span></span>
* <span data-ttu-id="fe2d3-554">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-554">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="fe2d3-555">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fe2d3-555">Az.Batch</span></span>
* <span data-ttu-id="fe2d3-556">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-556">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-557">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-558">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-558">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="fe2d3-559">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-559">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="fe2d3-560">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-560">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="fe2d3-561">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-561">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fe2d3-562">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe2d3-562">Az.DataFactory</span></span>
* <span data-ttu-id="fe2d3-563">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-563">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="fe2d3-564">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-564">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="fe2d3-565">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="fe2d3-565">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fe2d3-566">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe2d3-566">Az.DataLakeStore</span></span>
* <span data-ttu-id="fe2d3-567">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="fe2d3-567">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="fe2d3-568">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="fe2d3-568">Az.HealthcareApis</span></span>
* <span data-ttu-id="fe2d3-569">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="fe2d3-569">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="fe2d3-570">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="fe2d3-570">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="fe2d3-571">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-571">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="fe2d3-572">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-572">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fe2d3-573">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fe2d3-573">Az.IotHub</span></span>
* <span data-ttu-id="fe2d3-574">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="fe2d3-574">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="fe2d3-575">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe2d3-575">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="fe2d3-576">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-576">Az.Monitor</span></span>
* <span data-ttu-id="fe2d3-577">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="fe2d3-577">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="fe2d3-578">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-578">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="fe2d3-579">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-579">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="fe2d3-580">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-580">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-581">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-581">Az.Network</span></span>
* <span data-ttu-id="fe2d3-582">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-582">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="fe2d3-583">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-583">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="fe2d3-584">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-584">New cmdlets added:</span></span>
        - <span data-ttu-id="fe2d3-585">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="fe2d3-585">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="fe2d3-586">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-586">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="fe2d3-587">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-587">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="fe2d3-588">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-588">Updated cmdlets:</span></span>
        - <span data-ttu-id="fe2d3-589">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-589">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="fe2d3-590">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-590">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="fe2d3-591">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-591">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="fe2d3-592">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-592">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="fe2d3-593">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="fe2d3-593">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="fe2d3-594">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-594">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="fe2d3-595">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-595">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="fe2d3-596">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fe2d3-596">Az.RedisCache</span></span>
* <span data-ttu-id="fe2d3-597">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-597">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-598">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-599">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-599">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-600">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-601">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-601">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="fe2d3-602">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="fe2d3-602">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="fe2d3-603">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fe2d3-603">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="fe2d3-604">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="fe2d3-604">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="fe2d3-605">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe2d3-605">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="fe2d3-606">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="fe2d3-606">Az.StorageSync</span></span>
* <span data-ttu-id="fe2d3-607">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-607">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fe2d3-608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-608">Az.Websites</span></span>
* <span data-ttu-id="fe2d3-609">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="fe2d3-609">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="fe2d3-610">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="fe2d3-610">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="fe2d3-611">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe2d3-611">Az.ApiManagement</span></span>
* <span data-ttu-id="fe2d3-612">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="fe2d3-612">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="fe2d3-613">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-613">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="fe2d3-614">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-614">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fe2d3-615">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fe2d3-615">Az.Automation</span></span>
* <span data-ttu-id="fe2d3-616">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="fe2d3-616">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="fe2d3-617">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-617">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="fe2d3-618">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-618">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-619">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-619">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-620">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-620">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="fe2d3-621">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-621">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="fe2d3-622">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-622">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="fe2d3-623">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-623">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="fe2d3-624">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-624">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="fe2d3-625">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-625">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="fe2d3-626">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-626">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="fe2d3-627">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-627">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="fe2d3-628">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-628">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fe2d3-629">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe2d3-629">Az.DataFactory</span></span>
* <span data-ttu-id="fe2d3-630">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-630">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="fe2d3-631">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="fe2d3-631">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="fe2d3-632">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fe2d3-632">Az.HDInsight</span></span>
* <span data-ttu-id="fe2d3-633">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-633">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fe2d3-634">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fe2d3-634">Az.IotHub</span></span>
* <span data-ttu-id="fe2d3-635">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-635">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="fe2d3-636">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-636">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="fe2d3-637">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-637">New cmdlets are:</span></span>
    - <span data-ttu-id="fe2d3-638">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="fe2d3-638">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="fe2d3-639">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="fe2d3-639">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="fe2d3-640">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="fe2d3-640">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="fe2d3-641">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="fe2d3-641">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fe2d3-642">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-642">Az.Monitor</span></span>
* <span data-ttu-id="fe2d3-643">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="fe2d3-643">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="fe2d3-644">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-644">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="fe2d3-645">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-645">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="fe2d3-646">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-646">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="fe2d3-647">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-647">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="fe2d3-648">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-648">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="fe2d3-649">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-649">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="fe2d3-650">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-650">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="fe2d3-651">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-651">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="fe2d3-652">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-652">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="fe2d3-653">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-653">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="fe2d3-654">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-654">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="fe2d3-655">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-655">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="fe2d3-656">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="fe2d3-656">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="fe2d3-657">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="fe2d3-657">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="fe2d3-658">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="fe2d3-658">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="fe2d3-659">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="fe2d3-659">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="fe2d3-660">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-660">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="fe2d3-661">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-661">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="fe2d3-662">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-662">Overall improved help files</span></span>
* <span data-ttu-id="fe2d3-663">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="fe2d3-663">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-664">Az.Network</span></span>
* <span data-ttu-id="fe2d3-665">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="fe2d3-665">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="fe2d3-666">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="fe2d3-666">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="fe2d3-667">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-667">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="fe2d3-668">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-668">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="fe2d3-669">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-669">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="fe2d3-670">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-670">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="fe2d3-671">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-671">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="fe2d3-672">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-672">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="fe2d3-673">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-673">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="fe2d3-674">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="fe2d3-674">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="fe2d3-675">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-675">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="fe2d3-676">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="fe2d3-676">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="fe2d3-677">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-677">New cmdlets</span></span>
        - <span data-ttu-id="fe2d3-678">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="fe2d3-678">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="fe2d3-679">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-679">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="fe2d3-680">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-680">Updated cmdlet:</span></span>
        - <span data-ttu-id="fe2d3-681">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="fe2d3-681">New-VpnSite</span></span>
        - <span data-ttu-id="fe2d3-682">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="fe2d3-682">Update-VpnSite</span></span>
        - <span data-ttu-id="fe2d3-683">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-683">New-VpnConnection</span></span>
        - <span data-ttu-id="fe2d3-684">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-684">Update-VpnConnection</span></span>
* <span data-ttu-id="fe2d3-685">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="fe2d3-685">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-686">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-686">Az.RecoveryServices</span></span>
* <span data-ttu-id="fe2d3-687">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="fe2d3-687">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="fe2d3-688">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-688">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-689">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-690">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-690">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fe2d3-691">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fe2d3-691">Az.ServiceFabric</span></span>
* <span data-ttu-id="fe2d3-692">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="fe2d3-692">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="fe2d3-693">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-693">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="fe2d3-694">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fe2d3-694">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="fe2d3-695">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="fe2d3-695">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="fe2d3-696">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fe2d3-696">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="fe2d3-697">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="fe2d3-697">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="fe2d3-698">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fe2d3-698">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="fe2d3-699">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fe2d3-699">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="fe2d3-700">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="fe2d3-700">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="fe2d3-701">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fe2d3-701">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="fe2d3-702">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="fe2d3-702">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="fe2d3-703">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fe2d3-703">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="fe2d3-704">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="fe2d3-704">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="fe2d3-705">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fe2d3-705">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="fe2d3-706">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="fe2d3-706">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="fe2d3-707">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-707">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="fe2d3-708">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="fe2d3-708">Az.SignalR</span></span>
* <span data-ttu-id="fe2d3-709">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-709">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-710">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-711">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="fe2d3-711">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="fe2d3-712">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-712">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="fe2d3-713">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-713">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="fe2d3-714">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-714">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="fe2d3-715">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-715">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-716">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-716">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-717">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="fe2d3-717">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="fe2d3-718">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-718">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="fe2d3-719">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fe2d3-719">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="fe2d3-720">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fe2d3-720">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="fe2d3-721">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-721">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="fe2d3-722">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fe2d3-722">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="fe2d3-723">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-723">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="fe2d3-724">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fe2d3-724">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="fe2d3-725">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fe2d3-725">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="fe2d3-726">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fe2d3-726">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="fe2d3-727">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fe2d3-727">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fe2d3-728">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-728">Az.Websites</span></span>
* <span data-ttu-id="fe2d3-729">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-729">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="fe2d3-730">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-730">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="fe2d3-731">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="fe2d3-731">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="fe2d3-732">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="fe2d3-732">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="fe2d3-733">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="fe2d3-733">General</span></span>
* <span data-ttu-id="fe2d3-734">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-734">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-735">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-735">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-736">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="fe2d3-736">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="fe2d3-737">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="fe2d3-737">Az.Aks</span></span>
* <span data-ttu-id="fe2d3-738">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-738">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="fe2d3-739">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="fe2d3-739">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="fe2d3-740">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe2d3-740">Az.ApiManagement</span></span>
* <span data-ttu-id="fe2d3-741">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="fe2d3-741">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="fe2d3-742">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="fe2d3-742">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="fe2d3-743">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-743">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="fe2d3-744">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="fe2d3-744">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="fe2d3-745">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="fe2d3-745">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="fe2d3-746">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fe2d3-746">Az.Batch</span></span>
* <span data-ttu-id="fe2d3-747">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="fe2d3-747">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fe2d3-748">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fe2d3-748">Az.Cdn</span></span>
* <span data-ttu-id="fe2d3-749">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="fe2d3-749">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-750">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-751">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-751">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="fe2d3-752">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-752">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="fe2d3-753">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-753">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="fe2d3-754">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="fe2d3-754">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="fe2d3-755">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="fe2d3-755">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="fe2d3-756">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-756">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="fe2d3-757">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="fe2d3-757">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="fe2d3-758">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="fe2d3-758">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fe2d3-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe2d3-759">Az.DataFactory</span></span>
* <span data-ttu-id="fe2d3-760">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-760">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="fe2d3-761">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="fe2d3-761">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="fe2d3-762">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="fe2d3-762">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="fe2d3-763">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="fe2d3-763">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fe2d3-764">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe2d3-764">Az.DataLakeStore</span></span>
* <span data-ttu-id="fe2d3-765">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-765">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fe2d3-766">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fe2d3-766">Az.EventHub</span></span>
* <span data-ttu-id="fe2d3-767">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-767">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="fe2d3-768">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="fe2d3-768">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="fe2d3-769">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-769">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="fe2d3-770">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="fe2d3-770">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="fe2d3-771">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="fe2d3-771">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="fe2d3-772">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="fe2d3-772">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fe2d3-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-773">Az.Monitor</span></span>
* <span data-ttu-id="fe2d3-774">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-774">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-775">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-775">Az.Network</span></span>
* <span data-ttu-id="fe2d3-776">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-776">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="fe2d3-777">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-777">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="fe2d3-778">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-778">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="fe2d3-779">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="fe2d3-779">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="fe2d3-780">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-780">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="fe2d3-781">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-781">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="fe2d3-782">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-782">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fe2d3-783">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fe2d3-783">Az.OperationalInsights</span></span>
* <span data-ttu-id="fe2d3-784">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fe2d3-784">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="fe2d3-785">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-785">Added example</span></span>
    - <span data-ttu-id="fe2d3-786">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="fe2d3-786">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="fe2d3-787">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-787">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="fe2d3-788">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-788">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-789">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-789">Az.RecoveryServices</span></span>
* <span data-ttu-id="fe2d3-790">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="fe2d3-790">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-791">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-792">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="fe2d3-792">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="fe2d3-793">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-793">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="fe2d3-794">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="fe2d3-794">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="fe2d3-795">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-795">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fe2d3-796">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fe2d3-796">Az.ServiceBus</span></span>
* <span data-ttu-id="fe2d3-797">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-797">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="fe2d3-798">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="fe2d3-798">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="fe2d3-799">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="fe2d3-799">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="fe2d3-800">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fe2d3-800">Az.ServiceFabric</span></span>
* <span data-ttu-id="fe2d3-801">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-801">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="fe2d3-802">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-802">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="fe2d3-803">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="fe2d3-803">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="fe2d3-804">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-804">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="fe2d3-805">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="fe2d3-805">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="fe2d3-806">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="fe2d3-806">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-807">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-807">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-808">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-808">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-809">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-810">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="fe2d3-810">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="fe2d3-811">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-811">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="fe2d3-812">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fe2d3-812">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="fe2d3-813">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fe2d3-813">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="fe2d3-814">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-814">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="fe2d3-815">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fe2d3-815">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fe2d3-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-816">Az.Websites</span></span>
* <span data-ttu-id="fe2d3-817">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-817">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="fe2d3-818">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="fe2d3-818">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-819">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-819">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-820">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-820">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="fe2d3-821">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fe2d3-821">Az.ApplicationInsights</span></span>
* <span data-ttu-id="fe2d3-822">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-822">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="fe2d3-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fe2d3-823">Az.Automation</span></span>
* <span data-ttu-id="fe2d3-824">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-824">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="fe2d3-825">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-825">Az.CognitiveServices</span></span>
* <span data-ttu-id="fe2d3-826">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-826">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-827">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-827">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-828">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-828">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="fe2d3-829">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe2d3-829">Az.ContainerRegistry</span></span>
* <span data-ttu-id="fe2d3-830">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-830">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="fe2d3-831">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="fe2d3-831">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fe2d3-832">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe2d3-832">Az.DataFactory</span></span>
* <span data-ttu-id="fe2d3-833">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="fe2d3-833">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="fe2d3-834">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-834">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fe2d3-835">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fe2d3-835">Az.EventHub</span></span>
* <span data-ttu-id="fe2d3-836">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="fe2d3-836">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="fe2d3-837">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="fe2d3-837">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fe2d3-838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fe2d3-838">Az.KeyVault</span></span>
* <span data-ttu-id="fe2d3-839">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-839">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fe2d3-840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fe2d3-840">Az.LogicApp</span></span>
* <span data-ttu-id="fe2d3-841">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="fe2d3-841">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="fe2d3-842">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-842">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="fe2d3-843">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-843">Az.ManagedServices</span></span>
* <span data-ttu-id="fe2d3-844">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-844">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-845">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-845">Az.Network</span></span>
* <span data-ttu-id="fe2d3-846">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-846">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="fe2d3-847">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-847">New cmdlets</span></span>
        - <span data-ttu-id="fe2d3-848">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe2d3-848">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="fe2d3-849">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fe2d3-849">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="fe2d3-850">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-850">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fe2d3-851">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-851">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fe2d3-852">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-852">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fe2d3-853">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-853">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fe2d3-854">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="fe2d3-854">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="fe2d3-855">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fe2d3-855">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="fe2d3-856">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-856">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="fe2d3-857">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="fe2d3-857">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="fe2d3-858">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-858">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="fe2d3-859">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-859">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="fe2d3-860">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-860">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="fe2d3-861">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-861">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="fe2d3-862">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-862">Updated cmdlets</span></span>
        - <span data-ttu-id="fe2d3-863">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-863">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="fe2d3-864">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-864">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="fe2d3-865">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-865">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="fe2d3-866">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="fe2d3-866">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="fe2d3-867">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-867">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="fe2d3-868">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-868">Updated cmdlet:</span></span>
        - <span data-ttu-id="fe2d3-869">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-869">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="fe2d3-870">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-870">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="fe2d3-871">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-871">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="fe2d3-872">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-872">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="fe2d3-873">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-873">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="fe2d3-874">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-874">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fe2d3-875">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fe2d3-875">Az.OperationalInsights</span></span>
* <span data-ttu-id="fe2d3-876">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-876">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="fe2d3-877">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-877">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-878">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-878">Az.RecoveryServices</span></span>
* <span data-ttu-id="fe2d3-879">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-879">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="fe2d3-880">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-880">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="fe2d3-881">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-881">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="fe2d3-882">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-882">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="fe2d3-883">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-883">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="fe2d3-884">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-884">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="fe2d3-885">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-885">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="fe2d3-886">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-886">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="fe2d3-887">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-887">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="fe2d3-888">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-888">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-889">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-889">Az.Resources</span></span>
- <span data-ttu-id="fe2d3-890">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-890">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="fe2d3-891">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="fe2d3-891">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fe2d3-892">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fe2d3-892">Az.ServiceBus</span></span>
* <span data-ttu-id="fe2d3-893">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="fe2d3-893">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="fe2d3-894">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="fe2d3-894">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-895">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-895">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-896">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-896">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="fe2d3-897">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-897">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="fe2d3-898">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-898">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-899">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-900">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="fe2d3-900">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="fe2d3-901">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="fe2d3-901">Az.StorageSync</span></span>
* <span data-ttu-id="fe2d3-902">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-902">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="fe2d3-903">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-903">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fe2d3-904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-904">Az.Websites</span></span>
* <span data-ttu-id="fe2d3-905">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="fe2d3-905">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="fe2d3-906">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-906">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="fe2d3-907">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-907">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="fe2d3-908">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="fe2d3-908">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-909">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-909">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-910">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-910">Add support for profile cmdlets</span></span>
* <span data-ttu-id="fe2d3-911">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-911">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="fe2d3-912">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="fe2d3-912">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="fe2d3-913">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-913">Az.Advisor</span></span>
* <span data-ttu-id="fe2d3-914">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-914">GA release of Az.Advisor</span></span>
* <span data-ttu-id="fe2d3-915">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="fe2d3-915">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="fe2d3-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe2d3-916">Az.ApiManagement</span></span>
* <span data-ttu-id="fe2d3-917">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="fe2d3-917">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="fe2d3-918">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="fe2d3-918">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="fe2d3-919">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-919">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="fe2d3-920">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-920">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="fe2d3-921">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="fe2d3-921">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="fe2d3-922">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="fe2d3-922">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="fe2d3-923">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-923">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fe2d3-924">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fe2d3-924">Az.Automation</span></span>
* <span data-ttu-id="fe2d3-925">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-925">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-926">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-926">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-927">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-927">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fe2d3-928">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe2d3-928">Az.DataFactory</span></span>
* <span data-ttu-id="fe2d3-929">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-929">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="fe2d3-930">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fe2d3-930">Az.EventGrid</span></span>
* <span data-ttu-id="fe2d3-931">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="fe2d3-931">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fe2d3-932">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fe2d3-932">Az.IotHub</span></span>
* <span data-ttu-id="fe2d3-933">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-933">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-934">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-934">Az.Network</span></span>
* <span data-ttu-id="fe2d3-935">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-935">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="fe2d3-936">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-936">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fe2d3-937">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fe2d3-937">Az.PolicyInsights</span></span>
* <span data-ttu-id="fe2d3-938">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-938">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="fe2d3-939">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="fe2d3-939">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fe2d3-940">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fe2d3-940">Az.OperationalInsights</span></span>
* <span data-ttu-id="fe2d3-941">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="fe2d3-941">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-942">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-942">Az.RecoveryServices</span></span>
* <span data-ttu-id="fe2d3-943">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-943">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-944">Az.Resources</span></span>
    - <span data-ttu-id="fe2d3-945">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-945">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="fe2d3-946">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-946">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="fe2d3-947">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-947">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="fe2d3-948">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-948">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fe2d3-949">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fe2d3-949">Az.ServiceBus</span></span>
* <span data-ttu-id="fe2d3-950">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-950">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-951">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-952">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-952">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="fe2d3-953">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-953">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="fe2d3-954">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="fe2d3-954">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="fe2d3-955">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="fe2d3-955">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="fe2d3-956">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="fe2d3-956">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="fe2d3-957">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="fe2d3-957">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="fe2d3-958">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="fe2d3-958">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="fe2d3-959">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="fe2d3-959">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="fe2d3-960">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="fe2d3-960">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-961">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-962">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-962">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="fe2d3-963">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="fe2d3-963">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="fe2d3-964">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="fe2d3-964">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="fe2d3-965">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="fe2d3-965">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="fe2d3-966">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="fe2d3-966">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="fe2d3-967">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe2d3-967">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="fe2d3-968">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe2d3-968">Set-AzStorageAccount</span></span>
* <span data-ttu-id="fe2d3-969">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-969">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="fe2d3-970">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="fe2d3-970">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="fe2d3-971">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="fe2d3-971">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="fe2d3-972">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="fe2d3-972">Az.StorageSync</span></span>
* <span data-ttu-id="fe2d3-973">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="fe2d3-973">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="fe2d3-974">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="fe2d3-974">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-975">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-975">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-976">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-976">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="fe2d3-977">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="fe2d3-977">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="fe2d3-978">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-978">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="fe2d3-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fe2d3-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="fe2d3-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="fe2d3-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-981">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-982">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-982">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="fe2d3-983">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="fe2d3-983">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="fe2d3-984">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="fe2d3-984">Az.Dns</span></span>
* <span data-ttu-id="fe2d3-985">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-985">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="fe2d3-986">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fe2d3-986">Az.EventGrid</span></span>
* <span data-ttu-id="fe2d3-987">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-987">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="fe2d3-988">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-988">New cmdlets:</span></span>
    - <span data-ttu-id="fe2d3-989">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="fe2d3-989">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="fe2d3-990">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-990">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="fe2d3-991">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="fe2d3-991">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="fe2d3-992">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-992">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="fe2d3-993">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="fe2d3-993">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="fe2d3-994">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-994">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="fe2d3-995">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="fe2d3-995">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="fe2d3-996">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-996">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="fe2d3-997">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="fe2d3-997">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="fe2d3-998">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-998">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="fe2d3-999">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-999">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="fe2d3-1000">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1000">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="fe2d3-1001">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1001">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="fe2d3-1002">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1002">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="fe2d3-1003">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1003">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="fe2d3-1004">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1004">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="fe2d3-1005">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1005">Updated cmdlets:</span></span>
    - <span data-ttu-id="fe2d3-1006">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1006">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="fe2d3-1007">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1007">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="fe2d3-1008">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1008">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="fe2d3-1009">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1009">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="fe2d3-1010">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1010">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="fe2d3-1011">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1011">Event subscription expiration date,</span></span>
            - <span data-ttu-id="fe2d3-1012">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1012">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="fe2d3-1013">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1013">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="fe2d3-1014">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1014">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="fe2d3-1015">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1015">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="fe2d3-1016">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1016">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="fe2d3-1017">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1017">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="fe2d3-1018">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1018">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="fe2d3-1019">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1019">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="fe2d3-1020">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1020">Az.FrontDoor</span></span>
* <span data-ttu-id="fe2d3-1021">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1021">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="fe2d3-1022">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1022">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="fe2d3-1023">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1023">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="fe2d3-1024">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1024">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1025">Az.Network</span></span>
* <span data-ttu-id="fe2d3-1026">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1026">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="fe2d3-1027">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1027">New cmdlets</span></span>
        - <span data-ttu-id="fe2d3-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="fe2d3-1029">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1029">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="fe2d3-1030">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1030">New cmdlets</span></span> 
        - <span data-ttu-id="fe2d3-1031">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1031">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="fe2d3-1032">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1032">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="fe2d3-1033">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1033">New cmdlets</span></span> 
        - <span data-ttu-id="fe2d3-1034">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1034">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="fe2d3-1035">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1035">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="fe2d3-1036">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1036">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="fe2d3-1037">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1037">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="fe2d3-1038">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1038">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="fe2d3-1039">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1039">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="fe2d3-1040">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1040">New cmdlets</span></span>
        - <span data-ttu-id="fe2d3-1041">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1041">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="fe2d3-1042">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1042">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="fe2d3-1043">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1043">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="fe2d3-1044">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1044">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="fe2d3-1045">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1045">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="fe2d3-1046">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1046">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="fe2d3-1047">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1047">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="fe2d3-1048">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1048">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="fe2d3-1049">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1049">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="fe2d3-1050">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1050">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="fe2d3-1051">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1051">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="fe2d3-1052">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1052">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="fe2d3-1053">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1053">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="fe2d3-1054">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1054">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="fe2d3-1055">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1055">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="fe2d3-1056">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1056">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="fe2d3-1057">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1057">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="fe2d3-1058">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1058">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="fe2d3-1059">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1059">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="fe2d3-1060">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1060">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="fe2d3-1061">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1061">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="fe2d3-1062">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1062">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="fe2d3-1063">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1063">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="fe2d3-1064">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1064">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="fe2d3-1065">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1065">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="fe2d3-1066">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1066">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="fe2d3-1067">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1067">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fe2d3-1068">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1068">Az.OperationalInsights</span></span>
* <span data-ttu-id="fe2d3-1069">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1069">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-1070">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1070">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-1071">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1071">Support for additional Template Export options</span></span>
    - <span data-ttu-id="fe2d3-1072">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1072">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="fe2d3-1073">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1073">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="fe2d3-1074">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1074">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fe2d3-1075">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1075">Az.ServiceFabric</span></span>
* <span data-ttu-id="fe2d3-1076">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1076">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-1077">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1077">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-1078">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1078">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="fe2d3-1079">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1079">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="fe2d3-1080">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1080">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="fe2d3-1081">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1081">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="fe2d3-1082">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1082">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="fe2d3-1083">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1083">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="fe2d3-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="fe2d3-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-1086">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1086">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-1087">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1087">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="fe2d3-1088">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1088">New-AzStorageAccount</span></span>
* <span data-ttu-id="fe2d3-1089">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1089">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="fe2d3-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fe2d3-1091">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1091">Az.Websites</span></span>
* <span data-ttu-id="fe2d3-1092">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1092">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="fe2d3-1093">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1093">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="fe2d3-1094">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1094">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="fe2d3-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1095">Az.Cdn</span></span>
* <span data-ttu-id="fe2d3-1096">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1096">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1097">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-1098">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1098">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="fe2d3-1099">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1099">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fe2d3-1100">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1100">Az.EventHub</span></span>
* <span data-ttu-id="fe2d3-1101">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1101">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="fe2d3-1102">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1102">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-1103">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1103">Az.Network</span></span>
* <span data-ttu-id="fe2d3-1104">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1104">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="fe2d3-1105">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1105">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fe2d3-1106">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1106">Az.PolicyInsights</span></span>
* <span data-ttu-id="fe2d3-1107">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1107">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-1108">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1108">Az.RecoveryServices</span></span>
* <span data-ttu-id="fe2d3-1109">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1109">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fe2d3-1110">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1110">Az.ServiceBus</span></span>
* <span data-ttu-id="fe2d3-1111">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1111">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fe2d3-1112">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1112">Az.ServiceFabric</span></span>
* <span data-ttu-id="fe2d3-1113">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1113">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="fe2d3-1114">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1114">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-1115">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1115">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-1116">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1116">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="fe2d3-1117">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1117">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="fe2d3-1118">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1118">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="fe2d3-1119">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1119">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fe2d3-1120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1120">Az.Websites</span></span>
* <span data-ttu-id="fe2d3-1121">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1121">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="fe2d3-1122">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1122">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="fe2d3-1123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1123">Az.ApiManagement</span></span>
* <span data-ttu-id="fe2d3-1124">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1124">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="fe2d3-1125">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1125">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="fe2d3-1126">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1126">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="fe2d3-1127">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1127">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="fe2d3-1128">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1128">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="fe2d3-1129">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1129">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="fe2d3-1130">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1130">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="fe2d3-1131">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1131">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="fe2d3-1132">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1132">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="fe2d3-1133">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1133">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="fe2d3-1134">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1134">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="fe2d3-1135">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1135">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="fe2d3-1136">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1136">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="fe2d3-1137">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1137">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="fe2d3-1138">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1138">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="fe2d3-1139">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1139">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="fe2d3-1140">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1140">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="fe2d3-1141">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1141">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="fe2d3-1142">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1142">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="fe2d3-1143">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1143">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="fe2d3-1144">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1144">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="fe2d3-1145">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1145">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="fe2d3-1146">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1146">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="fe2d3-1147">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1147">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="fe2d3-1148">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1148">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="fe2d3-1149">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1149">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="fe2d3-1150">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1150">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="fe2d3-1151">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1151">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="fe2d3-1152">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1152">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="fe2d3-1153">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1153">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="fe2d3-1154">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1154">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="fe2d3-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="fe2d3-1156">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1156">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="fe2d3-1157">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1157">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="fe2d3-1158">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1158">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="fe2d3-1159">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1159">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="fe2d3-1160">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1160">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="fe2d3-1161">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1161">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="fe2d3-1162">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1162">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="fe2d3-1163">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1163">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="fe2d3-1164">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1164">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="fe2d3-1165">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1165">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="fe2d3-1166">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1166">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="fe2d3-1167">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1167">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="fe2d3-1168">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1168">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="fe2d3-1169">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1169">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="fe2d3-1170">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1170">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="fe2d3-1171">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1171">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="fe2d3-1172">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1172">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="fe2d3-1173">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1173">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="fe2d3-1174">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1174">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="fe2d3-1175">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1175">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="fe2d3-1176">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1176">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="fe2d3-1177">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1177">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="fe2d3-1178">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1178">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="fe2d3-1179">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1179">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="fe2d3-1180">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1180">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="fe2d3-1181">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1181">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="fe2d3-1182">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1182">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="fe2d3-1183">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1183">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="fe2d3-1184">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1184">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="fe2d3-1185">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1185">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="fe2d3-1186">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1186">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="fe2d3-1187">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1187">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="fe2d3-1188">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1188">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="fe2d3-1189">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1189">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="fe2d3-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="fe2d3-1191">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1191">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="fe2d3-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="fe2d3-1193">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1193">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="fe2d3-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="fe2d3-1195">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1195">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="fe2d3-1196">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1196">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="fe2d3-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="fe2d3-1198">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1198">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="fe2d3-1199">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1199">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="fe2d3-1200">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1200">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fe2d3-1201">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1201">Az.Automation</span></span>
* <span data-ttu-id="fe2d3-1202">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1202">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="fe2d3-1203">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1203">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="fe2d3-1204">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="fe2d3-1205">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1205">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="fe2d3-1206">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1206">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="fe2d3-1207">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1207">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="fe2d3-1208">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1208">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1209">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-1210">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1210">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="fe2d3-1211">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1211">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fe2d3-1212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1212">Az.DataLakeStore</span></span>
* <span data-ttu-id="fe2d3-1213">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1213">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fe2d3-1214">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1214">Az.Monitor</span></span>
* <span data-ttu-id="fe2d3-1215">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1215">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-1216">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1216">Az.Network</span></span>
* <span data-ttu-id="fe2d3-1217">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1217">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="fe2d3-1218">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1218">Updated cmdlet:</span></span>
        - <span data-ttu-id="fe2d3-1219">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1219">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="fe2d3-1220">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1220">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-1221">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1221">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-1222">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1222">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-1223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1223">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-1224">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1224">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="fe2d3-1225">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1225">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-1226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1226">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-1227">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1227">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fe2d3-1228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1228">Az.CognitiveServices</span></span>
* <span data-ttu-id="fe2d3-1229">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1229">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="fe2d3-1230">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1230">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1231">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-1232">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1232">Proximity placement group feature.</span></span>
    - <span data-ttu-id="fe2d3-1233">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1233">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="fe2d3-1234">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1234">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="fe2d3-1235">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1235">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="fe2d3-1236">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1236">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="fe2d3-1237">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1237">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="fe2d3-1238">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1238">Breaking changes</span></span>
    - <span data-ttu-id="fe2d3-1239">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1239">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="fe2d3-1240">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1240">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="fe2d3-1241">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1241">Az.DeploymentManager</span></span>
* <span data-ttu-id="fe2d3-1242">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1242">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="fe2d3-1243">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1243">Az.Dns</span></span>
* <span data-ttu-id="fe2d3-1244">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1244">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="fe2d3-1245">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1245">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="fe2d3-1246">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1246">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="fe2d3-1247">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1247">Az.FrontDoor</span></span>
* <span data-ttu-id="fe2d3-1248">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1248">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="fe2d3-1249">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1249">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="fe2d3-1250">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1250">Az.HDInsight</span></span>
* <span data-ttu-id="fe2d3-1251">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1251">Removed two cmdlets:</span></span>
    - <span data-ttu-id="fe2d3-1252">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1252">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="fe2d3-1253">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1253">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="fe2d3-1254">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1254">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="fe2d3-1255">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1255">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="fe2d3-1256">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1256">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="fe2d3-1257">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1257">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fe2d3-1258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1258">Az.Monitor</span></span>
* <span data-ttu-id="fe2d3-1259">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1259">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="fe2d3-1260">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1260">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="fe2d3-1261">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1261">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="fe2d3-1262">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1262">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="fe2d3-1263">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1263">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="fe2d3-1264">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1264">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="fe2d3-1265">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1265">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="fe2d3-1266">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1266">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="fe2d3-1267">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1267">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="fe2d3-1268">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1268">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="fe2d3-1269">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1269">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="fe2d3-1270">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1270">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="fe2d3-1271">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1271">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="fe2d3-1272">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1272">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-1273">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1273">Az.Network</span></span>
* <span data-ttu-id="fe2d3-1274">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1274">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="fe2d3-1275">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1275">New cmdlets</span></span>
        - <span data-ttu-id="fe2d3-1276">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1276">New-AzNatGateway</span></span>
        - <span data-ttu-id="fe2d3-1277">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1277">Get-AzNatGateway</span></span>
        - <span data-ttu-id="fe2d3-1278">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1278">Set-AzNatGateway</span></span>
        - <span data-ttu-id="fe2d3-1279">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1279">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="fe2d3-1280">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1280">Updated cmdlets</span></span>
        - <span data-ttu-id="fe2d3-1281">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1281">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="fe2d3-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="fe2d3-1283">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1283">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="fe2d3-1284">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1284">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="fe2d3-1285">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1285">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fe2d3-1286">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1286">Az.PolicyInsights</span></span>
* <span data-ttu-id="fe2d3-1287">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1287">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="fe2d3-1288">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1288">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="fe2d3-1289">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1289">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-1290">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1290">Az.RecoveryServices</span></span>
* <span data-ttu-id="fe2d3-1291">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1291">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="fe2d3-1292">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1292">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="fe2d3-1293">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1293">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="fe2d3-1294">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1294">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="fe2d3-1295">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1295">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="fe2d3-1296">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1296">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="fe2d3-1297">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1297">Az.Relay</span></span>
* <span data-ttu-id="fe2d3-1298">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1298">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fe2d3-1299">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1299">Az.ServiceBus</span></span>
* <span data-ttu-id="fe2d3-1300">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1300">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-1301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1301">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-1302">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1302">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="fe2d3-1303">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1303">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="fe2d3-1304">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1304">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="fe2d3-1305">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1305">New-AzStorageAccount</span></span>
* <span data-ttu-id="fe2d3-1306">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1306">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="fe2d3-1307">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1307">New-AzStorageAccount</span></span>
    - <span data-ttu-id="fe2d3-1308">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1308">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="fe2d3-1309">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1309">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fe2d3-1310">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1310">Az.Websites</span></span>
* <span data-ttu-id="fe2d3-1311">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1311">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="fe2d3-1312">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1312">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="fe2d3-1313">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1313">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fe2d3-1314">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1314">Highlights since the last major release</span></span>
* <span data-ttu-id="fe2d3-1315">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1315">General availability of `Az` module</span></span>
* <span data-ttu-id="fe2d3-1316">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1316">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="fe2d3-1317">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1317">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="fe2d3-1318">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1318">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="fe2d3-1319">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1319">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="fe2d3-1320">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1320">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="fe2d3-1321">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1321">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-1322">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1322">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-1323">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1323">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="fe2d3-1324">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1324">Az.Batch</span></span>
* <span data-ttu-id="fe2d3-1325">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1325">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fe2d3-1326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1326">Az.Cdn</span></span>
* <span data-ttu-id="fe2d3-1327">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fe2d3-1328">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1328">Az.CognitiveServices</span></span>
* <span data-ttu-id="fe2d3-1329">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1329">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-1330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1330">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-1331">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1331">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="fe2d3-1332">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fe2d3-1333">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1333">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fe2d3-1334">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1334">Az.DataFactory</span></span>
* <span data-ttu-id="fe2d3-1335">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1335">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fe2d3-1336">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1336">Az.DataLakeStore</span></span>
* <span data-ttu-id="fe2d3-1337">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1337">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="fe2d3-1338">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1338">Az.EventGrid</span></span>
* <span data-ttu-id="fe2d3-1339">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1339">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fe2d3-1340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1340">Az.EventHub</span></span>
* <span data-ttu-id="fe2d3-1341">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1341">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="fe2d3-1342">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1342">Az.HDInsight</span></span>
* <span data-ttu-id="fe2d3-1343">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1343">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fe2d3-1344">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1344">Az.IotHub</span></span>
* <span data-ttu-id="fe2d3-1345">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1345">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fe2d3-1346">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1346">Az.KeyVault</span></span>
* <span data-ttu-id="fe2d3-1347">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1347">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fe2d3-1348">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1348">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="fe2d3-1349">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1349">Az.MachineLearning</span></span>
* <span data-ttu-id="fe2d3-1350">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="fe2d3-1351">Az.Media</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1351">Az.Media</span></span>
* <span data-ttu-id="fe2d3-1352">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fe2d3-1353">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1353">Az.Monitor</span></span>
  * <span data-ttu-id="fe2d3-1354">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1354">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="fe2d3-1355">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1355">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="fe2d3-1356">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1356">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="fe2d3-1357">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1357">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="fe2d3-1358">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1358">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="fe2d3-1359">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1359">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="fe2d3-1360">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1360">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-1361">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1361">Az.Network</span></span>
* <span data-ttu-id="fe2d3-1362">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1362">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fe2d3-1363">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1363">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="fe2d3-1364">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1364">Az.NotificationHubs</span></span>
* <span data-ttu-id="fe2d3-1365">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1365">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fe2d3-1366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1366">Az.OperationalInsights</span></span>
* <span data-ttu-id="fe2d3-1367">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1367">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="fe2d3-1368">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1368">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="fe2d3-1369">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-1370">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1370">Az.RecoveryServices</span></span>
* <span data-ttu-id="fe2d3-1371">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1371">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fe2d3-1372">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1372">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="fe2d3-1373">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1373">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="fe2d3-1374">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1374">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="fe2d3-1375">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1375">Az.RedisCache</span></span>
* <span data-ttu-id="fe2d3-1376">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-1377">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1377">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-1378">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1378">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-1379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1379">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-1380">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1380">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="fe2d3-1381">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1381">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fe2d3-1382">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1382">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="fe2d3-1383">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1383">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="fe2d3-1384">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1384">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="fe2d3-1385">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1385">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="fe2d3-1386">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1386">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fe2d3-1387">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1387">Az.Websites</span></span>
* <span data-ttu-id="fe2d3-1388">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1388">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="fe2d3-1389">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1389">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fe2d3-1390">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1390">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="fe2d3-1391">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1391">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="fe2d3-1392">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1392">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fe2d3-1393">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1393">Highlights since the last major release</span></span>
* <span data-ttu-id="fe2d3-1394">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1394">General availability of `Az` module</span></span>
* <span data-ttu-id="fe2d3-1395">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1395">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="fe2d3-1396">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1396">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="fe2d3-1397">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1397">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="fe2d3-1398">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1398">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="fe2d3-1399">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1399">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="fe2d3-1400">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1400">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-1401">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1401">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-1402">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1402">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="fe2d3-1403">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1403">Az.AnalysisServices</span></span>
* <span data-ttu-id="fe2d3-1404">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1404">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="fe2d3-1405">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1405">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fe2d3-1406">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1406">Az.Automation</span></span>
* <span data-ttu-id="fe2d3-1407">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1407">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="fe2d3-1408">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1408">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="fe2d3-1409">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1409">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-1410">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1410">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-1411">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1411">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="fe2d3-1412">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1412">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="fe2d3-1413">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1413">Az.ContainerInstance</span></span>
* <span data-ttu-id="fe2d3-1414">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1414">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fe2d3-1415">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1415">Az.DataFactory</span></span>
* <span data-ttu-id="fe2d3-1416">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1416">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="fe2d3-1417">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1417">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-1418">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1418">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-1419">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1419">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="fe2d3-1420">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1420">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="fe2d3-1421">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1421">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="fe2d3-1422">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1422">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="fe2d3-1423">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1423">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="fe2d3-1424">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1424">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-1425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1425">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-1426">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1426">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-1427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1427">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-1428">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1428">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="fe2d3-1429">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1429">New-AzStorageContext</span></span>
* <span data-ttu-id="fe2d3-1430">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1430">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="fe2d3-1431">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1431">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="fe2d3-1432">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1432">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="fe2d3-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="fe2d3-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="fe2d3-1435">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1435">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="fe2d3-1436">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1436">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="fe2d3-1437">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1437">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="fe2d3-1438">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1438">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="fe2d3-1439">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1439">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="fe2d3-1440">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1440">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fe2d3-1441">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1441">Highlights since the last major release</span></span>
* <span data-ttu-id="fe2d3-1442">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1442">General availability of `Az` module</span></span>
* <span data-ttu-id="fe2d3-1443">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1443">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="fe2d3-1444">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1444">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="fe2d3-1445">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1445">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="fe2d3-1446">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1446">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="fe2d3-1447">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1447">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="fe2d3-1448">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1448">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fe2d3-1449">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1449">Az.Automation</span></span>
* <span data-ttu-id="fe2d3-1450">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1450">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="fe2d3-1451">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1451">Dynamic grouping</span></span>
    * <span data-ttu-id="fe2d3-1452">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1452">Pre-Post script</span></span>
    * <span data-ttu-id="fe2d3-1453">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1453">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-1454">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1454">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-1455">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1455">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="fe2d3-1456">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1456">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fe2d3-1457">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1457">Az.KeyVault</span></span>
* <span data-ttu-id="fe2d3-1458">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1458">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-1459">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1459">Az.Network</span></span>
* <span data-ttu-id="fe2d3-1460">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1460">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="fe2d3-1461">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1461">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-1462">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1462">Az.RecoveryServices</span></span>
* <span data-ttu-id="fe2d3-1463">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1463">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="fe2d3-1464">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1464">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1465">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-1466">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1466">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="fe2d3-1467">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1467">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-1468">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1468">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-1469">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1469">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-1470">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1470">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-1471">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1471">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="fe2d3-1472">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1472">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="fe2d3-1473">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1473">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="fe2d3-1474">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1474">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="fe2d3-1475">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1475">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="fe2d3-1476">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1476">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="fe2d3-1477">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1477">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fe2d3-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1478">Az.Websites</span></span>
* <span data-ttu-id="fe2d3-1479">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1479">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="fe2d3-1480">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1480">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-1481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1481">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-1482">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1482">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="fe2d3-1483">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1483">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fe2d3-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1484">Az.Automation</span></span>
* <span data-ttu-id="fe2d3-1485">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1485">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="fe2d3-1486">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1486">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="fe2d3-1487">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1487">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fe2d3-1488">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1488">Az.Cdn</span></span>
* <span data-ttu-id="fe2d3-1489">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1489">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-1490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1490">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-1491">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1491">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fe2d3-1492">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1492">Az.DataFactory</span></span>
* <span data-ttu-id="fe2d3-1493">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1493">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fe2d3-1494">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1494">Az.LogicApp</span></span>
* <span data-ttu-id="fe2d3-1495">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1495">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-1496">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1496">Az.Network</span></span>
* <span data-ttu-id="fe2d3-1497">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1497">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-1498">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1498">Az.RecoveryServices</span></span>
* <span data-ttu-id="fe2d3-1499">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1499">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="fe2d3-1500">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1500">SDK Update</span></span>
* <span data-ttu-id="fe2d3-1501">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1501">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="fe2d3-1502">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1502">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-1503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1503">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-1504">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1504">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="fe2d3-1505">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1505">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="fe2d3-1506">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1506">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="fe2d3-1507">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1507">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="fe2d3-1508">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1508">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="fe2d3-1509">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1509">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1510">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-1511">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1511">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="fe2d3-1512">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1512">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-1513">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1513">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-1514">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1514">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="fe2d3-1515">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1515">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="fe2d3-1516">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1516">Az.AnalysisServices</span></span>
* <span data-ttu-id="fe2d3-1517">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1517">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fe2d3-1518">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1518">Az.Automation</span></span>
* <span data-ttu-id="fe2d3-1519">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1519">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="fe2d3-1520">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1520">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="fe2d3-1521">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1521">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fe2d3-1522">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1522">Az.CognitiveServices</span></span>
* <span data-ttu-id="fe2d3-1523">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1523">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-1524">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1524">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-1525">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1525">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="fe2d3-1526">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1526">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="fe2d3-1527">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1527">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="fe2d3-1528">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1528">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fe2d3-1529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1529">Az.DataLakeStore</span></span>
* <span data-ttu-id="fe2d3-1530">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1530">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fe2d3-1531">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1531">Az.EventHub</span></span>
* <span data-ttu-id="fe2d3-1532">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1532">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="fe2d3-1533">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1533">Az.KeyVault</span></span>
* <span data-ttu-id="fe2d3-1534">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1534">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fe2d3-1535">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1535">Az.LogicApp</span></span>
* <span data-ttu-id="fe2d3-1536">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1536">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="fe2d3-1537">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1537">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="fe2d3-1538">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1538">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="fe2d3-1539">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1539">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="fe2d3-1540">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1540">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="fe2d3-1541">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1541">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="fe2d3-1542">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1542">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="fe2d3-1543">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1543">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="fe2d3-1544">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1544">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="fe2d3-1545">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1545">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="fe2d3-1546">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1546">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="fe2d3-1547">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1547">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="fe2d3-1548">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1548">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fe2d3-1549">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1549">Az.Monitor</span></span>
* <span data-ttu-id="fe2d3-1550">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1550">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1551">Az.Network</span></span>
* <span data-ttu-id="fe2d3-1552">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1552">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fe2d3-1553">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1553">Az.OperationalInsights</span></span>
* <span data-ttu-id="fe2d3-1554">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1554">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="fe2d3-1555">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1555">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="fe2d3-1556">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1556">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="fe2d3-1557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1557">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-1558">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1558">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="fe2d3-1559">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1559">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="fe2d3-1560">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1560">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="fe2d3-1561">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1561">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-1562">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1562">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-1563">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1563">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="fe2d3-1564">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1564">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fe2d3-1565">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1565">Az.Websites</span></span>
* <span data-ttu-id="fe2d3-1566">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1566">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="fe2d3-1567">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1567">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-1568">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1568">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-1569">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1569">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="fe2d3-1570">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1570">Az.AnalysisServices</span></span>
<span data-ttu-id="fe2d3-1571">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1571">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-1572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1572">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-1573">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1573">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="fe2d3-1574">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1574">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="fe2d3-1575">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1575">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-1576">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1576">Az.RecoveryServices</span></span>
<span data-ttu-id="fe2d3-1577">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1577">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-1578">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1578">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-1579">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1579">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="fe2d3-1580">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1580">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="fe2d3-1581">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1581">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="fe2d3-1582">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1582">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-1583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1583">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-1584">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1584">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="fe2d3-1585">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1585">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="fe2d3-1586">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1586">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="fe2d3-1587">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1587">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1588">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-1589">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1589">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="fe2d3-1590">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1590">Az.AnalysisServices</span></span>
* <span data-ttu-id="fe2d3-1591">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1591">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="fe2d3-1593">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1593">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="fe2d3-1594">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1594">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-1595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1595">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-1596">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1596">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="fe2d3-1597">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1597">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fe2d3-1598">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1598">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="fe2d3-1599">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1599">Az.Aks</span></span>
* <span data-ttu-id="fe2d3-1600">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1600">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fe2d3-1601">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1601">Az.Automation</span></span>
* <span data-ttu-id="fe2d3-1602">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1602">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="fe2d3-1603">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1603">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fe2d3-1604">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1604">Az.Cdn</span></span>
* <span data-ttu-id="fe2d3-1605">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1605">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-1606">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1606">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-1607">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1607">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="fe2d3-1608">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1608">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="fe2d3-1609">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1609">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="fe2d3-1610">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1610">Az.ContainerRegistry</span></span>
* <span data-ttu-id="fe2d3-1611">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1611">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fe2d3-1612">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1612">Az.DataFactory</span></span>
* <span data-ttu-id="fe2d3-1613">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1613">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fe2d3-1614">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1614">Az.DataLakeStore</span></span>
* <span data-ttu-id="fe2d3-1615">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1615">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="fe2d3-1616">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1616">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="fe2d3-1617">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1617">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fe2d3-1618">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1618">Az.IotHub</span></span>
* <span data-ttu-id="fe2d3-1619">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1619">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fe2d3-1620">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1620">Az.KeyVault</span></span>
* <span data-ttu-id="fe2d3-1621">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1621">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-1622">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1622">Az.Network</span></span>
* <span data-ttu-id="fe2d3-1623">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1623">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-1624">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1624">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-1625">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1625">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="fe2d3-1626">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1626">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="fe2d3-1627">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1627">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="fe2d3-1628">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1628">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="fe2d3-1629">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1629">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="fe2d3-1630">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1630">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="fe2d3-1631">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1631">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fe2d3-1632">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1632">Az.ServiceFabric</span></span>
* <span data-ttu-id="fe2d3-1633">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1633">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="fe2d3-1634">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1634">Fix some error messages.</span></span>
* <span data-ttu-id="fe2d3-1635">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1635">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="fe2d3-1636">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1636">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="fe2d3-1637">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1637">Az.SignalR</span></span>
* <span data-ttu-id="fe2d3-1638">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1638">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-1639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1639">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-1640">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1640">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fe2d3-1641">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1641">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="fe2d3-1642">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1642">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="fe2d3-1643">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1643">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-1644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1644">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-1645">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1645">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fe2d3-1646">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1646">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="fe2d3-1647">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1647">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="fe2d3-1648">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1648">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="fe2d3-1649">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1649">Az.TrafficManager</span></span>
* <span data-ttu-id="fe2d3-1650">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1650">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fe2d3-1651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1651">Az.Websites</span></span>
* <span data-ttu-id="fe2d3-1652">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fe2d3-1653">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1653">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="fe2d3-1654">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1654">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="fe2d3-1655">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1655">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fe2d3-1656">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1656">Az.Accounts</span></span>
* <span data-ttu-id="fe2d3-1657">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1657">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-1658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1658">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-1659">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1659">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="fe2d3-1660">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1660">Updated the description of ID in help files</span></span>
* <span data-ttu-id="fe2d3-1661">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1661">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fe2d3-1662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1662">Az.DataLakeStore</span></span>
* <span data-ttu-id="fe2d3-1663">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1663">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="fe2d3-1664">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1664">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="fe2d3-1665">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1665">Az.EventGrid</span></span>
* <span data-ttu-id="fe2d3-1666">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1666">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="fe2d3-1667">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1667">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="fe2d3-1668">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1668">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="fe2d3-1669">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1669">Event Time-To-Live,</span></span>
        - <span data-ttu-id="fe2d3-1670">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1670">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="fe2d3-1671">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1671">Dead letter endpoint.</span></span>
    - <span data-ttu-id="fe2d3-1672">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1672">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="fe2d3-1673">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1673">Event Time-To-Live,</span></span>
        - <span data-ttu-id="fe2d3-1674">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1674">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="fe2d3-1675">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1675">Dead letter endpoint.</span></span>
* <span data-ttu-id="fe2d3-1676">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1676">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="fe2d3-1677">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1677">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fe2d3-1678">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1678">Az.IotHub</span></span>
* <span data-ttu-id="fe2d3-1679">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1679">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fe2d3-1680">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1680">Az.LogicApp</span></span>
* <span data-ttu-id="fe2d3-1681">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1681">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1682">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-1683">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1683">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="fe2d3-1684">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1684">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="fe2d3-1685">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1685">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="fe2d3-1686">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1686">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="fe2d3-1687">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1687">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="fe2d3-1688">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1688">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="fe2d3-1689">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1689">Az.SignalR</span></span>
* <span data-ttu-id="fe2d3-1690">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1690">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-1691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1691">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-1692">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1692">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fe2d3-1693">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1693">Az.Storage</span></span>
* <span data-ttu-id="fe2d3-1694">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1694">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="fe2d3-1695">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1695">New-AzStorageContext</span></span>
* <span data-ttu-id="fe2d3-1696">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1696">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="fe2d3-1697">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1697">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fe2d3-1698">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1698">Az.Websites</span></span>
* <span data-ttu-id="fe2d3-1699">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1699">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="fe2d3-1700">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1700">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="fe2d3-1701">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1701">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="fe2d3-1702">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1702">General</span></span>

- <span data-ttu-id="fe2d3-1703">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1703">General Availability of Az Module</span></span>
- <span data-ttu-id="fe2d3-1704">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1704">Online help for each module</span></span>
- <span data-ttu-id="fe2d3-1705">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1705">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="fe2d3-1706">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1706">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="fe2d3-1707">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1707">Az.Accounts</span></span>
- <span data-ttu-id="fe2d3-1708">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1708">Changed from Az.Profile</span></span>
- <span data-ttu-id="fe2d3-1709">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1709">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="fe2d3-1710">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1710">Az.ApiManagement</span></span>
- <span data-ttu-id="fe2d3-1711">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1711">Fixes for #7002</span></span>
- <span data-ttu-id="fe2d3-1712">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1712">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="fe2d3-1713">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1713">Az.Batch</span></span>
- <span data-ttu-id="fe2d3-1714">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1714">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="fe2d3-1715">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1715">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="fe2d3-1716">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="fe2d3-1717">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1717">Az.Billing</span></span>
- <span data-ttu-id="fe2d3-1718">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1718">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="fe2d3-1719">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1719">Az.CognitivServices</span></span>
- <span data-ttu-id="fe2d3-1720">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1720">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="fe2d3-1721">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1721">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="fe2d3-1722">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1722">Az.ContainerInstance</span></span>
- <span data-ttu-id="fe2d3-1723">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1723">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="fe2d3-1724">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1724">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="fe2d3-1725">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1725">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="fe2d3-1726">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1726">Az.DataLakeStore</span></span>
- <span data-ttu-id="fe2d3-1727">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1727">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="fe2d3-1728">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1728">Az.Monitor</span></span>
- <span data-ttu-id="fe2d3-1729">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1729">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="fe2d3-1730">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1730">Az.KeyVault</span></span>
- <span data-ttu-id="fe2d3-1731">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1731">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="fe2d3-1732">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1732">Az.MachineLearning</span></span>
- <span data-ttu-id="fe2d3-1733">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1733">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="fe2d3-1734">Az.Media</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1734">Az.Media</span></span>
- <span data-ttu-id="fe2d3-1735">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1735">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="fe2d3-1736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1736">Az.Network</span></span>
<span data-ttu-id="fe2d3-1737">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1737">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="fe2d3-1738">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1738">New cmdlets added:</span></span>
        - <span data-ttu-id="fe2d3-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fe2d3-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fe2d3-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fe2d3-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fe2d3-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fe2d3-1744">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1744">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="fe2d3-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="fe2d3-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="fe2d3-1747">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1747">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="fe2d3-1748">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1748">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="fe2d3-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="fe2d3-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="fe2d3-1751">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1751">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="fe2d3-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="fe2d3-1753">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1753">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="fe2d3-1754">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1754">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="fe2d3-1755">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1755">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="fe2d3-1756">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1756">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="fe2d3-1757">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1757">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="fe2d3-1758">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1758">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="fe2d3-1759">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1759">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="fe2d3-1760">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1760">Az.OperationalInsights</span></span>
- <span data-ttu-id="fe2d3-1761">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1761">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="fe2d3-1762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1762">Az.Profile</span></span>
- <span data-ttu-id="fe2d3-1763">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1763">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-1764">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1764">Az.RecoveryServices</span></span>
- <span data-ttu-id="fe2d3-1765">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1765">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="fe2d3-1766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1766">Az.Resources</span></span>
- <span data-ttu-id="fe2d3-1767">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="fe2d3-1768">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1768">Az.ServiceFabric</span></span>
- <span data-ttu-id="fe2d3-1769">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1769">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="fe2d3-1770">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1770">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="fe2d3-1771">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1771">Az.SIgnalR</span></span>
- <span data-ttu-id="fe2d3-1772">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1772">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="fe2d3-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1773">Az.Sql</span></span>
- <span data-ttu-id="fe2d3-1774">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1774">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="fe2d3-1775">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1775">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="fe2d3-1776">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1776">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="fe2d3-1777">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1777">Az.Storage</span></span>
- <span data-ttu-id="fe2d3-1778">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1778">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="fe2d3-1779">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1779">Az.Websites</span></span>
- <span data-ttu-id="fe2d3-1780">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="fe2d3-1781">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1781">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="fe2d3-1782">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1782">General</span></span>

* <span data-ttu-id="fe2d3-1783">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1783">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="fe2d3-1784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1784">Az.Compute</span></span>

* <span data-ttu-id="fe2d3-1785">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1785">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="fe2d3-1786">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1786">Az.DataLakeStore</span></span>

* <span data-ttu-id="fe2d3-1787">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1787">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="fe2d3-1788">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1788">Az.FrontDoor</span></span>

* <span data-ttu-id="fe2d3-1789">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1789">Fixed some broken links</span></span>
    - <span data-ttu-id="fe2d3-1790">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1790">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="fe2d3-1791">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1791">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="fe2d3-1792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1792">Az.RecoveryServices</span></span>

* <span data-ttu-id="fe2d3-1793">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1793">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="fe2d3-1794">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1794">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="fe2d3-1795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1795">Az.Resources</span></span>

* <span data-ttu-id="fe2d3-1796">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1796">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="fe2d3-1797">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1797">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="fe2d3-1798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1798">Az.Sql</span></span>

* <span data-ttu-id="fe2d3-1799">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1799">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="fe2d3-1800">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1800">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="fe2d3-1801">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1801">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="fe2d3-1802">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1802">Az.Storage</span></span>

* <span data-ttu-id="fe2d3-1803">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1803">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="fe2d3-1804">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1804">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="fe2d3-1805">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1805">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="fe2d3-1806">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1806">Support Static Website configuration</span></span>
    - <span data-ttu-id="fe2d3-1807">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1807">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="fe2d3-1808">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1808">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="fe2d3-1809">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1809">Az.Websites</span></span>

* <span data-ttu-id="fe2d3-1810">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1810">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="fe2d3-1811">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1811">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="fe2d3-1812">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1812">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="fe2d3-1813">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1813">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="fe2d3-1814">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1814">Az.ApiManagement</span></span>
* <span data-ttu-id="fe2d3-1815">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1815">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="fe2d3-1816">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1816">Az.Automation</span></span>
* <span data-ttu-id="fe2d3-1817">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1817">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="fe2d3-1818">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1818">Added Update Management cmdlets</span></span>
* <span data-ttu-id="fe2d3-1819">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1819">Added Source Control cmdlets</span></span>
* <span data-ttu-id="fe2d3-1820">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1820">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="fe2d3-1821">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1821">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="fe2d3-1822">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1822">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-1823">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1823">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="fe2d3-1824">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1824">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="fe2d3-1825">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1825">Az.ContainerInstance</span></span>
* <span data-ttu-id="fe2d3-1826">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1826">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="fe2d3-1827">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1827">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="fe2d3-1828">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1828">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="fe2d3-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1829">Az.Network</span></span>
* <span data-ttu-id="fe2d3-1830">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1830">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="fe2d3-1831">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1831">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="fe2d3-1832">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1832">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="fe2d3-1833">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1833">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="fe2d3-1834">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1834">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fe2d3-1835">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1835">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="fe2d3-1836">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1836">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="fe2d3-1837">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1837">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="fe2d3-1838">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1838">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="fe2d3-1839">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1839">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="fe2d3-1840">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1840">Az.Relay</span></span>
* <span data-ttu-id="fe2d3-1841">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1841">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="fe2d3-1842">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1842">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-1843">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1843">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="fe2d3-1844">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1844">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="fe2d3-1845">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1845">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="fe2d3-1846">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1846">Az.ServiceFabric</span></span>
* <span data-ttu-id="fe2d3-1847">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1847">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="fe2d3-1848">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1848">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-1849">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1849">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="fe2d3-1850">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1850">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fe2d3-1851">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1851">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fe2d3-1852">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1852">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fe2d3-1853">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1853">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fe2d3-1854">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1854">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fe2d3-1855">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1855">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fe2d3-1856">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1856">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fe2d3-1857">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1857">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="fe2d3-1858">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1858">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="fe2d3-1859">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1859">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="fe2d3-1860">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1860">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="fe2d3-1861">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1861">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="fe2d3-1862">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1862">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="fe2d3-1863">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1863">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="fe2d3-1864">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1864">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="fe2d3-1865">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1865">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="fe2d3-1866">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1866">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fe2d3-1867">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1867">General</span></span>
* <span data-ttu-id="fe2d3-1868">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1868">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="fe2d3-1869">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1869">Az.Profile</span></span>
* <span data-ttu-id="fe2d3-1870">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1870">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="fe2d3-1871">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1871">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="fe2d3-1872">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1872">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="fe2d3-1873">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1873">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="fe2d3-1874">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1874">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="fe2d3-1875">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1875">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="fe2d3-1876">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1876">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="fe2d3-1877">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1877">Az.CognitiveServices</span></span>
* <span data-ttu-id="fe2d3-1878">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1878">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-1879">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1879">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-1880">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1880">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="fe2d3-1881">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1881">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="fe2d3-1882">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1882">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fe2d3-1883">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1883">Az.DataLakeStore</span></span>
* <span data-ttu-id="fe2d3-1884">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1884">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="fe2d3-1885">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1885">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="fe2d3-1886">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1886">Az.Insights</span></span>
* <span data-ttu-id="fe2d3-1887">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1887">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="fe2d3-1888">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1888">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="fe2d3-1889">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1889">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="fe2d3-1890">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1890">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-1891">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1891">Az.Network</span></span>
* <span data-ttu-id="fe2d3-1892">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1892">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="fe2d3-1893">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1893">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="fe2d3-1894">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1894">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="fe2d3-1895">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1895">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="fe2d3-1896">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1896">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="fe2d3-1897">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1897">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="fe2d3-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fe2d3-1899">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1899">Az.PolicyInsights</span></span>
* <span data-ttu-id="fe2d3-1900">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1900">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-1901">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1901">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-1902">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1902">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="fe2d3-1903">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1903">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fe2d3-1904">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1904">Az.ServiceBus</span></span>
* <span data-ttu-id="fe2d3-1905">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1905">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fe2d3-1906">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1906">Az.ServiceFabric</span></span>
* <span data-ttu-id="fe2d3-1907">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1907">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="fe2d3-1908">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1908">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="fe2d3-1909">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1909">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="fe2d3-1910">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1910">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="fe2d3-1911">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1911">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="fe2d3-1912">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1912">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="fe2d3-1913">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1913">Az.Profile</span></span>
* <span data-ttu-id="fe2d3-1914">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1914">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="fe2d3-1915">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1915">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-1916">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1916">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-1917">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1917">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="fe2d3-1918">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1918">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fe2d3-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="fe2d3-1920">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1920">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="fe2d3-1921">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1921">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="fe2d3-1922">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1922">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="fe2d3-1923">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1923">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="fe2d3-1924">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1924">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1925">Az.Network</span></span>
* <span data-ttu-id="fe2d3-1926">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1926">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="fe2d3-1927">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1927">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-1928">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1928">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-1929">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1929">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="fe2d3-1930">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1930">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="fe2d3-1931">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1931">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="fe2d3-1932">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1932">Azure.Storage</span></span>
* <span data-ttu-id="fe2d3-1933">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1933">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="fe2d3-1934">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1934">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="fe2d3-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="fe2d3-1936">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1936">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="fe2d3-1937">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1937">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="fe2d3-1938">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1938">Az.CognitiveServices</span></span>
* <span data-ttu-id="fe2d3-1939">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1939">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fe2d3-1940">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1940">Az.Compute</span></span>
* <span data-ttu-id="fe2d3-1941">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1941">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="fe2d3-1942">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1942">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="fe2d3-1943">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1943">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="fe2d3-1944">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1944">Az.DataFactoryV2</span></span>
* <span data-ttu-id="fe2d3-1945">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1945">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fe2d3-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1946">Az.Network</span></span>
* <span data-ttu-id="fe2d3-1947">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1947">Added NetworkProfile functionality.</span></span> <span data-ttu-id="fe2d3-1948">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1948">new cmdlets added</span></span>
    - <span data-ttu-id="fe2d3-1949">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1949">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="fe2d3-1950">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1950">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="fe2d3-1951">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1951">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="fe2d3-1952">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1952">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="fe2d3-1953">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1953">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="fe2d3-1954">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1954">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="fe2d3-1955">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1955">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="fe2d3-1956">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1956">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="fe2d3-1957">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1957">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="fe2d3-1958">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1958">Az.RedisCache</span></span>
* <span data-ttu-id="fe2d3-1959">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1959">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="fe2d3-1960">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1960">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="fe2d3-1961">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1961">Az.Resources</span></span>
* <span data-ttu-id="fe2d3-1962">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1962">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="fe2d3-1963">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1963">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="fe2d3-1964">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1964">Az.Sql</span></span>
* <span data-ttu-id="fe2d3-1965">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1965">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fe2d3-1966">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1966">Az.Websites</span></span>
* <span data-ttu-id="fe2d3-1967">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1967">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="fe2d3-1968">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1968">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="fe2d3-1969">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1969">0.2.0 - September 2018</span></span>
 <span data-ttu-id="fe2d3-1970">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="fe2d3-1970">Initial Release</span></span>
