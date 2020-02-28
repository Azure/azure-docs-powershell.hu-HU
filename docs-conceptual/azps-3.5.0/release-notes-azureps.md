---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 81afcd63e5ca7a776965849de9090b833f49acc7
ms.sourcegitcommit: a321ef9d134c684fa24ababcbd898f86b00d9364
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/20/2020
ms.locfileid: "77477233"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="0a711-103">Az Azure PowerShell kibocsátási megjegyzései</span><span class="sxs-lookup"><span data-stu-id="0a711-103">Azure PowerShell release notes</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="0a711-104">3.5.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="0a711-104">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a711-105">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="0a711-105">Highlights since the last major release</span></span>
* <span data-ttu-id="0a711-106">Frissült az ügyféloldali telemetria.</span><span class="sxs-lookup"><span data-stu-id="0a711-106">Updated client side telemetry.</span></span>
* <span data-ttu-id="0a711-107">Az.IotHub: parancsmagok hozzáadva az eszközkezelés támogatásához.</span><span class="sxs-lookup"><span data-stu-id="0a711-107">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="0a711-108">Az.SqlVirtualMachine: parancsmagok hozzáadva a rendelkezésreállási csoport figyelőjéhez.</span><span class="sxs-lookup"><span data-stu-id="0a711-108">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a711-109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-109">Az.Accounts</span></span>
* <span data-ttu-id="0a711-110">A SubscriptionId, a TenantId és a végrehajtási idő hozzáadva az ügyféloldali telemetria adataihoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-110">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a711-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a711-111">Az.Automation</span></span>
* <span data-ttu-id="0a711-112">Ki lett javítva a „New-AzAutomationSoftwareUpdateConfiguration” referenciadokumentációjának 1. példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="0a711-112">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a711-113">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a711-113">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a711-114">Az SDK a 7.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="0a711-114">Updated SDK to 7.0</span></span>
* <span data-ttu-id="0a711-115">Tovább lett fejlesztve a hibaüzenet, amely akkor jelenik meg, ha a kiszolgáló üres törzset ad vissza válaszként</span><span class="sxs-lookup"><span data-stu-id="0a711-115">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-116">Az.Compute</span></span>
* <span data-ttu-id="0a711-117">A ProximityPlacementGroupId mostantól üres értékkel is rendelkezhet a frissítés során</span><span class="sxs-lookup"><span data-stu-id="0a711-117">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a711-118">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a711-118">Az.FrontDoor</span></span>
* <span data-ttu-id="0a711-119">Új parancsmag hozzáadva a WAF-ban használható felügyelt szabálydefiníciók lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-119">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a711-120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a711-120">Az.IotHub</span></span>
* <span data-ttu-id="0a711-121">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="0a711-121">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="0a711-122">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="0a711-122">New Cmdlets are:</span></span>
    - <span data-ttu-id="0a711-123">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="0a711-123">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0a711-124">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="0a711-124">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0a711-125">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="0a711-125">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0a711-126">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="0a711-126">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a711-127">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a711-127">Az.KeyVault</span></span>
* <span data-ttu-id="0a711-128">Ki lett javítva az Add-AzKeyVaultKey.md duplikált szövege</span><span class="sxs-lookup"><span data-stu-id="0a711-128">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a711-129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a711-129">Az.Monitor</span></span>
* <span data-ttu-id="0a711-130">Ki lett javítva a Get-AzLog parancsmag leírása.</span><span class="sxs-lookup"><span data-stu-id="0a711-130">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="0a711-131">Egy új, ActionGroupId nevű paraméter lett hozzáadva a „New-AzMetricAlertRuleV2” parancshoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-131">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="0a711-132">A felhasználó a következőket adhatja meg: ActionGroupId(string) vagy ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="0a711-132">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-133">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-133">Az.Network</span></span>
* <span data-ttu-id="0a711-134">Hozzá lett adva egy extra paramétermegjegyzés a „New-AzPrivateLinkService” parancsmag „-EnableProxyProtocol” paraméteréhez.</span><span class="sxs-lookup"><span data-stu-id="0a711-134">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="0a711-135">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-135">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="0a711-136">Hozzá lett adva egy csomagrögzítési példa a Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és Start-AzVirtualnetworkGatewayPacketCapture.md minden belső és külső csomagjának rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="0a711-136">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="0a711-137">Az Azure Firewall-szabályzat mostantól támogatott a Vnet-tűzfalakon</span><span class="sxs-lookup"><span data-stu-id="0a711-137">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="0a711-138">Nem lettek hozzáadva új parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="0a711-138">No new cmdlets are added.</span></span> <span data-ttu-id="0a711-139">Enyhítve lettek a tűzfalszabályzat korlátozásai a Vnet-tűzfalak esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-139">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-140">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-140">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a711-141">A fájlokként történő visszaállítás mostantól támogatott az SQL-adatbázisok esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-141">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-142">Az.Resources</span></span>
* <span data-ttu-id="0a711-143">Újra lettek tervezve a sablonalapú üzembehelyezési parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a711-143">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="0a711-144">Új parancsmagok lettek hozzáadva a felügyeleti csoportban való üzembe helyezés kezeléséhez: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a711-144">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="0a711-145">Új parancsmagok lettek hozzáadva a bérlői hatókörben való üzembe helyezés kezeléséhez: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0a711-145">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="0a711-146">Az \*-AzDeployment parancsmagok kifejezetten az előfizetési hatókörben való működéshez lettek újratervezve</span><span class="sxs-lookup"><span data-stu-id="0a711-146">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="0a711-147">Az \*-AzSubscriptionDeployment aliasok lettek létrehozva az \*-AzDeployment parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-147">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="0a711-148">Ki lett javítva az „Update-AzADApplication” nem beállított „AvailableToOtherTenants” paraméter esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-148">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="0a711-149">Az ApplicationObjectWithoutCredentialParameterSet el lett távolítva az AmbiguousParameterSetException elkerülése érdekében.</span><span class="sxs-lookup"><span data-stu-id="0a711-149">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="0a711-150">A súgófájlok újra létre lettek hozva</span><span class="sxs-lookup"><span data-stu-id="0a711-150">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-151">Az.Sql</span></span>
* <span data-ttu-id="0a711-152">Az előfizetések közötti időponthoz kötött visszaállítás mostantól támogatott a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="0a711-152">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="0a711-153">A már meglévő felügyelt SQL-példány hardvergenerációjának módosítása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="0a711-153">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="0a711-154">Ki lettek javítva az „Update-AzSqlServerVulnerabilityAssessmentSetting” súgópéldái: paraméter/tulajdonságkimenet – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="0a711-154">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="0a711-155">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0a711-155">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="0a711-156">Parancsmagokat hozzáadva a rendelkezésreállási csoport figyelőjéhez</span><span class="sxs-lookup"><span data-stu-id="0a711-156">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0a711-157">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0a711-157">Az.StorageSync</span></span>
* <span data-ttu-id="0a711-158">Frissültek az „Invoke-AzStorageSyncCompatibilityCheck” támogatott karakterkészletei.</span><span class="sxs-lookup"><span data-stu-id="0a711-158">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="0a711-159">3.4.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="0a711-159">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a711-160">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="0a711-160">Highlights since the last major release</span></span>
* <span data-ttu-id="0a711-161">Megjelent az Az.CosmosDB 0.1.0-s kezdeti verziója</span><span class="sxs-lookup"><span data-stu-id="0a711-161">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="0a711-162">Az.Network ConnectionMonitor V2 támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="0a711-162">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a711-163">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-163">Az.Accounts</span></span>
* <span data-ttu-id="0a711-164">A környezet automatikus mentésének letiltása, ha az AzureRmContext.json nem érhető el</span><span class="sxs-lookup"><span data-stu-id="0a711-164">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="0a711-165">Az Azure Powershell Common referenciájának frissítése 1.3.5-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="0a711-165">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0a711-166">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a711-166">Az.ApiManagement</span></span>
* <span data-ttu-id="0a711-167">**Get-AzApiManagementApiSchema** Az API-val társított Open-API séma kijavítása   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="0a711-167">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="0a711-168">**New-AzApiManagementProduct**\* és **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="0a711-168">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="0a711-169">https://github.com/Azure/azure-powershell/issues/10472 dokumentációja kijavítva</span><span class="sxs-lookup"><span data-stu-id="0a711-169">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="0a711-170">**Set-AzApiManagementApi** A ServiceUrl parancsmaggal való frissítését bemutató példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-170">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-171">Az.Compute</span></span>
* <span data-ttu-id="0a711-172">A virtuális gép állapotának korlátozása 100 értékre, hogy ne legyen szabályozás, ha a Get-AzVM -Status a virtuális gép neve nélkül lett végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="0a711-172">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="0a711-173">Update-AzDiskEncryptionSet parancsmagok hozzáadása</span><span class="sxs-lookup"><span data-stu-id="0a711-173">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="0a711-174">Az EncryptionType és a DiskEncryptionSetId paraméterek hozzáadása a következő parancsmagokhoz:</span><span class="sxs-lookup"><span data-stu-id="0a711-174">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="0a711-175">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-175">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="0a711-176">A ColocationStatus paraméter hozzáadva a Get-AzProximityPlacementGroup parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-176">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a711-177">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a711-177">Az.DataFactory</span></span>
* <span data-ttu-id="0a711-178">Az ADF .Net SDK frissítve lett a 4.7.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="0a711-178">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0a711-179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0a711-179">Az.DeploymentManager</span></span>
* <span data-ttu-id="0a711-180">LIST műveletek hozzáadása az erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-180">Adds LIST operations for resources</span></span>
* <span data-ttu-id="0a711-181">Műveletek végrehajtásának lehetősége az állapotellenőrzés lépésein</span><span class="sxs-lookup"><span data-stu-id="0a711-181">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a711-182">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a711-182">Az.HDInsight</span></span>
* <span data-ttu-id="0a711-183">A New-AzHDInsightCluster dokumentációs hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="0a711-183">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a711-184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a711-184">Az.KeyVault</span></span>
* <span data-ttu-id="0a711-185">Name alias hozzáadása a VaultName attribútumhoz, hogy a Remove-AzureKeyVault konzisztens legyen a New-AzureKeyVault paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="0a711-185">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-186">Az.Network</span></span>
* <span data-ttu-id="0a711-187">Új példa hozzáadva a Set-AzNetworkWatcherConfigFlowLog.md fájlhoz a Traffic Analytics-letiltási forgatókönyv szemléltetésére.</span><span class="sxs-lookup"><span data-stu-id="0a711-187">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="0a711-188">Felügyeleti IP-konfiguráció támogatás hozzáadva az Azure Firewallhoz – egy dedikált alhálózat és nyilvános IP-cím, amelyet a tűzfal a forgalom felügyeléséhez használni fog</span><span class="sxs-lookup"><span data-stu-id="0a711-188">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="0a711-189">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="0a711-189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0a711-190">Hozzá lett adva a (nem kötelező) -PublicIpAddress-ManagementPublicIpAddress paraméter, amely egy nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="0a711-190">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="0a711-191">Hozzá lett adva a SetManagementIpConfiguration metódus a tűzfalobjektumok esetében – nyilvános IP-cím-objektumokat fogad el bemeneti adatként – az alhálózat nevének AzureFirewallManagementSubnet értéknek kell lennie</span><span class="sxs-lookup"><span data-stu-id="0a711-191">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="0a711-192">A Get-AzNetworkSecurityGroup példái javítva, hogy hálózati biztonsági csoportok példáit tartalmazzák hálózati adapterek helyett.</span><span class="sxs-lookup"><span data-stu-id="0a711-192">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="0a711-193">Javítottunk egy elírást a New-AzVpnSite parancsban, amely megakadályozta, hogy az erőforrásazonosító-kiegészítő kiegészítsen egy paramétert.</span><span class="sxs-lookup"><span data-stu-id="0a711-193">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="0a711-194">Az Application Gateway szabály-újraírási műveletkészletének URL-konfigurálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="0a711-194">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="0a711-195">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="0a711-195">New cmdlets added:</span></span>
        - <span data-ttu-id="0a711-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a711-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="0a711-197">A parancsmagok frissültek a nem kötelező UrlConfiguration paraméterrel</span><span class="sxs-lookup"><span data-stu-id="0a711-197">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="0a711-198">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0a711-198">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="0a711-199">A Network Watcher Connection Monitor 2-es verziójú erőforrások támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-199">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a711-200">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a711-200">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a711-201">A javítandó erőforrások azonosítása előtti megfelelőségértékelés támogatása</span><span class="sxs-lookup"><span data-stu-id="0a711-201">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="0a711-202">-ResourceDiscoverMode paraméter hozzáadása a Start-AzPolicyRemediation parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-202">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="0a711-203">A szabályzatok metaadat-erőforrásainak elérésére szolgáló Get-AzPolicyMetadata parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="0a711-203">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="0a711-204">A Get-AzPolicyState és a Get-AzPolicyStateSummary frissült a 2019-10-01 API-verzióhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-204">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a711-206">Azure Site Recovery-támogatás a replikált lemezek eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="0a711-206">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="0a711-207">Hozzáadott Azure Backup-támogatás a helyreállítási tárak létrehozása közbeni címkehozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-207">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-208">Az.Resources</span></span>
* <span data-ttu-id="0a711-209">A -Scope választható a \*-AzPolicyAssignment parancsmagokban; az alapértelmezett érték a környezeti előfizetés</span><span class="sxs-lookup"><span data-stu-id="0a711-209">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="0a711-210">Az ADServicePrincipal jelszó és kulcs típusú hitelesítő adatokkal való létrehozását szemléltető példák hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-210">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-211">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-211">Az.Sql</span></span>
<span data-ttu-id="0a711-212">A New-AzSqlDatabaseSecondary parancsmag javítva, hogy a PartnerDatabaseName létezését ellenőrizze a DatabaseName létezése helyett.</span><span class="sxs-lookup"><span data-stu-id="0a711-212">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-213">Az.Storage</span></span>
* <span data-ttu-id="0a711-214">A Table/Queue Encryption Keytype készlet beállításának támogatása Storage-fiók létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="0a711-214">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="0a711-215">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a711-215">New-AzStorageAccount</span></span>
* <span data-ttu-id="0a711-216">RequestId megjelenítése, ha a StorageException nem rendelkezik ExtendedErrorInformation paraméterrel</span><span class="sxs-lookup"><span data-stu-id="0a711-216">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="0a711-217">A Start-AzStorageBlobCopy parancsmag 6. példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="0a711-217">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a711-218">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-218">Az.Websites</span></span>
* <span data-ttu-id="0a711-219">A Set-AzWebapp és a Set-AzWebappSlot támogatja az AlwaysOn, a MinTls és a FtpsState tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="0a711-219">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="0a711-220">Javítva a hiba, amely miatt a HttpsOnly és az AppservicePlan Set-AzWebApp paranccsal történő egyidejű módosításakor a HttpsOnly paraméter alaphelyzetbe állt.</span><span class="sxs-lookup"><span data-stu-id="0a711-220">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="0a711-221">3.3.0 – 2020. január</span><span class="sxs-lookup"><span data-stu-id="0a711-221">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a711-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-222">Az.Accounts</span></span>
* <span data-ttu-id="0a711-223">Frissítve lettek az Add-AzEnvironment és Set-AzEnvironment parancsmagok, amelyek mostantól elfogadják az AzureAttestationServiceEndpointResourceId és AzureAttestationServiceEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="0a711-223">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a711-224">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a711-224">Az.Cdn</span></span>
* <span data-ttu-id="0a711-225">A hibaválasz részleteinek láthatóvá tétele a New-AzCdnEndpoint parancsmagban</span><span class="sxs-lookup"><span data-stu-id="0a711-225">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-226">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-226">Az.Compute</span></span>
* <span data-ttu-id="0a711-227">Javítva lett a Set-AzVMCustomScriptExtension parancsmag az olyan virtuális gépek esetében, amelyek felügyelt operációsrendszer-lemeze nem rendelkezik operációsrendszer-profillal.</span><span class="sxs-lookup"><span data-stu-id="0a711-227">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="0a711-228">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0a711-228">Az.ContainerInstance</span></span>
* <span data-ttu-id="0a711-229">Javítva lettek a New-AzContainerGroup parancsmagpélda által használt paraméternevek</span><span class="sxs-lookup"><span data-stu-id="0a711-229">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0a711-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0a711-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0a711-231">Hozzá lett adva a Get-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="0a711-231">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0a711-232">Az Edge Storage-tároló lekérése</span><span class="sxs-lookup"><span data-stu-id="0a711-232">Get the Edge Storage Container</span></span>
* <span data-ttu-id="0a711-233">Hozzá lett adva a New-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="0a711-233">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0a711-234">Új Edge Storage-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="0a711-234">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="0a711-235">Hozzá lett adva a Remove-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="0a711-235">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0a711-236">Az Edge Storage-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0a711-236">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="0a711-237">Hozzá lett adva az Invoke-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="0a711-237">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0a711-238">Meghívási művelet az Edge Storage-tárolóban lévő adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-238">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="0a711-239">Hozzá lett adva a Get-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="0a711-239">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0a711-240">Az Edge Storage-fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="0a711-240">Get the Edge Storage Account</span></span>
* <span data-ttu-id="0a711-241">Hozzá lett adva a New-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="0a711-241">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0a711-242">Új Edge Storage-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="0a711-242">Create new Edge Storage Account</span></span>
* <span data-ttu-id="0a711-243">Hozzá lett adva a Remove-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="0a711-243">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0a711-244">Az Edge Storage-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0a711-244">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="0a711-245">Hozzá lett adva az Invoke-AzDataBoxEdgeShare parancsmag</span><span class="sxs-lookup"><span data-stu-id="0a711-245">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="0a711-246">Meghívási művelet a megosztott adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-246">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="0a711-247">Hozzá lett adva a Set-AzDataBoxEdgeStorageAccountCredential parancsmag</span><span class="sxs-lookup"><span data-stu-id="0a711-247">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="0a711-248">Az Az.DataBoxEdge tárfiók hitelesítő adatainak beállítása</span><span class="sxs-lookup"><span data-stu-id="0a711-248">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a711-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a711-249">Az.DataFactory</span></span>
* <span data-ttu-id="0a711-250">Hozzá lettek adva az AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId és VersionStatus tulajdonságok a Get-AzDataFactoryV2IntegrationRuntime parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-250">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="0a711-251">Az ADF .Net SDK frissítve lett a 4.6.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="0a711-251">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="0a711-252">A PublicIPs paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz statikus nyilvános IP-címekkel rendelkező Azure-SSIS IR létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="0a711-252">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="0a711-253">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="0a711-253">Az.DevTestLabs</span></span>
* <span data-ttu-id="0a711-254">A hibás hivatkozás el lett távolítva a Get-AzDtlAllowedVMSizesPolicy.md parancsmagból</span><span class="sxs-lookup"><span data-stu-id="0a711-254">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a711-255">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a711-255">Az.EventHub</span></span>
* <span data-ttu-id="0a711-256">A 10634-es hiba javítása: Ki lett javítva a nullértékű objektumhivatkozás a remove eventhubnamespace esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-256">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a711-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a711-257">Az.HDInsight</span></span>
* <span data-ttu-id="0a711-258">Ki lett javítva az Invoke-AzHDInsightHiveJob.md hibája.</span><span class="sxs-lookup"><span data-stu-id="0a711-258">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0a711-259">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0a711-259">Az.MachineLearning</span></span>
* <span data-ttu-id="0a711-260">El lettek távolítva az alábbi parancsmagok, mivel a MachineLearningCompute már nem érhető el</span><span class="sxs-lookup"><span data-stu-id="0a711-260">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="0a711-261">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0a711-261">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="0a711-262">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="0a711-262">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="0a711-263">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0a711-263">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="0a711-264">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0a711-264">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="0a711-265">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0a711-265">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="0a711-266">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="0a711-266">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="0a711-267">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="0a711-267">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-268">Az.Network</span></span>
* <span data-ttu-id="0a711-269">Frissítve lett a Microsoft.Azure.Management.Sql függősége: 1.36-preview helyett 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="0a711-269">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-270">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-270">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a711-271">Módosított Azure Site Recovery-támogatás azon felügyelt lemezeken található, inaktív állapotban titkosított virtuális gépeknél, amelyekhez felhasználó által kezelt kulcsok tartoznak a következő esetében: Azure – Azure-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="0a711-271">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="0a711-272">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a védelem engedélyezése során a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="0a711-272">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0a711-273">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a lemez szintjén a védelem engedélyezéséhez a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="0a711-273">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0a711-274">Azure Site Recovery-támogatás a Replikációval védett, lemeztitkosítási csoportleképezéssel ellátott elemek frissítéséhez a következő esetében: HyperV – Azure.</span><span class="sxs-lookup"><span data-stu-id="0a711-274">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-275">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-275">Az.Resources</span></span>
* <span data-ttu-id="0a711-276">Javítva lett egy hiba a Remove-AzTag súgódokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="0a711-276">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-277">Az.Sql</span></span>
* <span data-ttu-id="0a711-278">Javítva lett a sebezhetőségi felmérés csoportszintű alapkonfigurációs parancsmagjainak működése: az Azure-adatbázis főadatbázisában használható, a felügyelt példányok rendszeradatbázisaiban korlátozott.</span><span class="sxs-lookup"><span data-stu-id="0a711-278">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="0a711-279">Ki lett javítva egy hiba az SQL-példányok feladatátvételi csoportjainak létrehozása esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-279">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="0a711-280">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0a711-280">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="0a711-281">Hozzá lett adva a DR, mint új érvényes licenctípus</span><span class="sxs-lookup"><span data-stu-id="0a711-281">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-282">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-282">Az.Storage</span></span>
* <span data-ttu-id="0a711-283">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet a DefaultAction értékének módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="0a711-283">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="0a711-284">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a711-284">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="0a711-285">Támogatott a tárfiók legutóbbi szinkronizálási időpontjának lekérése a get-AzureRMStorageAccount parancsmag -IncludeGeoReplicationStats paraméterrel való futtatásával</span><span class="sxs-lookup"><span data-stu-id="0a711-285">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="0a711-286">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a711-286">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="0a711-287">3.2.0 – 2019. december</span><span class="sxs-lookup"><span data-stu-id="0a711-287">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="0a711-288">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="0a711-288">General</span></span>
* <span data-ttu-id="0a711-289">A .psd1 hivatkozásai frissítve, hogy minden modulhoz a relatív elérési utat használják</span><span class="sxs-lookup"><span data-stu-id="0a711-289">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a711-290">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-290">Az.Accounts</span></span>
* <span data-ttu-id="0a711-291">A megfelelő felhasználói ügynök beállítva az ügyféloldali telemetriához az Az 4.0 előzetes verziójában</span><span class="sxs-lookup"><span data-stu-id="0a711-291">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="0a711-292">Felhasználóbarát hibaüzenet megjelenítése, ha az Az 4.0 előzetes verziójában a környezet null értékű</span><span class="sxs-lookup"><span data-stu-id="0a711-292">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0a711-293">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a711-293">Az.Batch</span></span>
* <span data-ttu-id="0a711-294">Ki lett javítva a [10602-es](https://github.com/Azure/azure-powershell/issues/10602) számú hiba, amely miatt a **New-AzBatchPool** nem megfelelően küldte el a „VirtualMachineConfiguration.ContainerConfiguration” és a „VirtualMachineConfiguration.DataDisks” paramétereket a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="0a711-294">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a711-295">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a711-295">Az.DataFactory</span></span>
* <span data-ttu-id="0a711-296">Az ADF .Net SDK a 4.5.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="0a711-296">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a711-297">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a711-297">Az.FrontDoor</span></span>
* <span data-ttu-id="0a711-298">A WAF felügyeleti szabályok kizárása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="0a711-298">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="0a711-299">Hozzá lett adva a SocketAddr automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="0a711-299">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0a711-300">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0a711-300">Az.HealthcareApis</span></span>
* <span data-ttu-id="0a711-301">Kivételkezelés</span><span class="sxs-lookup"><span data-stu-id="0a711-301">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a711-302">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a711-302">Az.KeyVault</span></span>
* <span data-ttu-id="0a711-303">Ki lett javítva az esetleg nem beállított értékek hozzáférésével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="0a711-303">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="0a711-304">Az elliptikus görbéjű titkosítási tanúsítványok kezelése</span><span class="sxs-lookup"><span data-stu-id="0a711-304">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="0a711-305">A görbe tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="0a711-305">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a711-306">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a711-306">Az.Monitor</span></span>
* <span data-ttu-id="0a711-307">Opcionális argumentum hozzáadva a Diagnosztikai beállítások hozzáadása parancshoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-307">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="0a711-308">Ez egy kapcsoló argumentum, amely megléte esetén azt jelzi, hogy a Log Analyticsbe történő exportálást egy rögzített séma (más néven</span><span class="sxs-lookup"><span data-stu-id="0a711-308">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="0a711-309">dedikált adattípus) szerint kell végrehajtani</span><span class="sxs-lookup"><span data-stu-id="0a711-309">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-310">Az.Network</span></span>
* <span data-ttu-id="0a711-311">Támogatás az Ip-csoportok számára az AzureFirewall alkalmazás, valamint a Nat- és a hálózati szabályok esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-311">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-312">Az.Resources</span></span>
* <span data-ttu-id="0a711-313">Ki lett javítva az a hiba, amely miatt a sablonalapú üzembe helyezés során a sablonparamétert nem lehet olvasni, ha a sablonparaméter és egy beépített paraméter neve között névütközés áll fenn.</span><span class="sxs-lookup"><span data-stu-id="0a711-313">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="0a711-314">Frissültek a szabályzat parancsmagjai a 2019. 09. 01. dátumú új API-verzió használatára, amely bevezeti a szabályzatkészlet-definíciókon belüli csoportos támogatást.</span><span class="sxs-lookup"><span data-stu-id="0a711-314">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-315">Az.Sql</span></span>
* <span data-ttu-id="0a711-316">Frissítve lett a sebezhetőségi felmérés automatikus engedélyezéséhez szükséges tárterület létrehozása a Storagev2-ben</span><span class="sxs-lookup"><span data-stu-id="0a711-316">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-317">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-317">Az.Storage</span></span>
* <span data-ttu-id="0a711-318">A blob-/tárolóidentitás-alapú SAS-token Oauth-hitelesítésen alapuló Storage-környezettel való létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="0a711-318">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="0a711-319">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="0a711-319">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="0a711-320">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0a711-320">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="0a711-321">Támogatott lett a tárfiókhoz tartozó felhasználódelegálási kulcsok visszavonása, így minden identitásalapú SAS-token visszavonható</span><span class="sxs-lookup"><span data-stu-id="0a711-321">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="0a711-322">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="0a711-322">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="0a711-323">Frissítés a Microsoft.Azure.Management.Storage 14.2.0-s verziójára az új API-verzió (2019. 06. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="0a711-323">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="0a711-324">A QuotaGiB (gigabájtban megadott megosztási kvóta) esetében támogatottak az 5120-nál nagyobb értékek a fájlmegosztási parancsmagok felügyeleti síkján, és hozzá lett adva a Quota paraméteralias a QuotaGiB paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="0a711-324">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="0a711-325">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a711-325">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="0a711-326">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a711-326">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="0a711-327">A „QuotaGiB” paraméteralias hozzáadva a „kvóta” paraméterhez</span><span class="sxs-lookup"><span data-stu-id="0a711-327">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="0a711-328">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="0a711-328">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="0a711-329">Ki lett javítva az a hiba, amely miatt a Set-AzStorageContainerAcl parancsmag el tudta távolítani a tárolt hozzáférési szabályzatot</span><span class="sxs-lookup"><span data-stu-id="0a711-329">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="0a711-330">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="0a711-330">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="0a711-331">3.1.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="0a711-331">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a711-332">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="0a711-332">Highlights since the last major release</span></span>
* <span data-ttu-id="0a711-333">Az.DataBoxEdge 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="0a711-333">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="0a711-334">Az.SqlVirtualMachine 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="0a711-334">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-335">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-335">Az.Compute</span></span>
* <span data-ttu-id="0a711-336">A virtuális gépek Reapply funkciója</span><span class="sxs-lookup"><span data-stu-id="0a711-336">VM Reapply feature</span></span>
    - <span data-ttu-id="0a711-337">A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-337">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="0a711-338">A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:</span><span class="sxs-lookup"><span data-stu-id="0a711-338">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="0a711-339">Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0a711-339">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="0a711-340">Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-340">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="0a711-341">A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez</span><span class="sxs-lookup"><span data-stu-id="0a711-341">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0a711-342">A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-342">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="0a711-343">A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező</span><span class="sxs-lookup"><span data-stu-id="0a711-343">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="0a711-344">A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="0a711-344">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="0a711-345">A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban</span><span class="sxs-lookup"><span data-stu-id="0a711-345">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="0a711-346">A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-346">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0a711-347">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0a711-347">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0a711-348">A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="0a711-348">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0a711-349">Megrendelés lekérése</span><span class="sxs-lookup"><span data-stu-id="0a711-349">Get the Order</span></span>
* <span data-ttu-id="0a711-350">A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="0a711-350">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0a711-351">Új megrendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="0a711-351">Create new Order</span></span>
* <span data-ttu-id="0a711-352">A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="0a711-352">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0a711-353">Megrendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0a711-353">Remove the Order</span></span>
* <span data-ttu-id="0a711-354">`New-AzDataBoxEdgeShare` parancsmag módosítása</span><span class="sxs-lookup"><span data-stu-id="0a711-354">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="0a711-355">Mostantól helyi megosztást hoz létre</span><span class="sxs-lookup"><span data-stu-id="0a711-355">Now creates Local Share</span></span>
* <span data-ttu-id="0a711-356">A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="0a711-356">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="0a711-357">Mostantól az IotRole leképezhető a Share-re</span><span class="sxs-lookup"><span data-stu-id="0a711-357">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="0a711-358">A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="0a711-358">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="0a711-359">Frissítések keresésének, letöltésének, telepítésének indítása az eszközön</span><span class="sxs-lookup"><span data-stu-id="0a711-359">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="0a711-360">A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="0a711-360">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0a711-361">Triggerek információinak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="0a711-361">Gets the information about Triggers</span></span>
* <span data-ttu-id="0a711-362">A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="0a711-362">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0a711-363">Új triggerek létrehozása</span><span class="sxs-lookup"><span data-stu-id="0a711-363">Create new Triggers</span></span>
* <span data-ttu-id="0a711-364">A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="0a711-364">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0a711-365">Triggerek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0a711-365">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a711-366">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a711-366">Az.DataFactory</span></span>
* <span data-ttu-id="0a711-367">Az ADF .Net SDK a 4.4.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="0a711-367">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="0a711-368">Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="0a711-368">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a711-369">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a711-369">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a711-370">Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja</span><span class="sxs-lookup"><span data-stu-id="0a711-370">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a711-371">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a711-371">Az.EventHub</span></span>
* <span data-ttu-id="0a711-372">A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása</span><span class="sxs-lookup"><span data-stu-id="0a711-372">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a711-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a711-373">Az.FrontDoor</span></span>
* <span data-ttu-id="0a711-374">Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="0a711-374">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="0a711-375">A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="0a711-375">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="0a711-376">Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához</span><span class="sxs-lookup"><span data-stu-id="0a711-376">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="0a711-377">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="0a711-377">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-378">Az.Network</span></span>
* <span data-ttu-id="0a711-379">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.</span><span class="sxs-lookup"><span data-stu-id="0a711-379">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="0a711-380">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="0a711-380">Az.PrivateDns</span></span>
* <span data-ttu-id="0a711-381">A PrivateDns .net sdk frissült az 1.0.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="0a711-381">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a711-383">Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="0a711-383">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="0a711-384">Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.</span><span class="sxs-lookup"><span data-stu-id="0a711-384">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="0a711-385">SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="0a711-385">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0a711-386">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0a711-386">Az.RedisCache</span></span>
* <span data-ttu-id="0a711-387">A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="0a711-387">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="0a711-388">Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="0a711-388">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="0a711-389">Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-389">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-390">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-390">Az.Resources</span></span>
- <span data-ttu-id="0a711-391">Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.</span><span class="sxs-lookup"><span data-stu-id="0a711-391">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="0a711-392">Frissült a létrehozási szabályzat definíciójának súgóbeli példája</span><span class="sxs-lookup"><span data-stu-id="0a711-392">Updated create policy definition help example</span></span>
- <span data-ttu-id="0a711-393">Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.</span><span class="sxs-lookup"><span data-stu-id="0a711-393">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="0a711-394">Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.</span><span class="sxs-lookup"><span data-stu-id="0a711-394">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="0a711-395">A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="0a711-395">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-396">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-396">Az.Sql</span></span>
* <span data-ttu-id="0a711-397">Az adatbázisbeli ReadReplicaCount mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="0a711-397">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="0a711-398">A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén</span><span class="sxs-lookup"><span data-stu-id="0a711-398">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="0a711-399">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="0a711-399">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="0a711-400">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="0a711-400">General</span></span>
* <span data-ttu-id="0a711-401">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0a711-401">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a711-402">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-402">Az.Accounts</span></span>
* <span data-ttu-id="0a711-403">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="0a711-403">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0a711-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0a711-404">Az.Advisor</span></span>
* <span data-ttu-id="0a711-405">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-405">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0a711-406">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a711-406">Az.Batch</span></span>
* <span data-ttu-id="0a711-407">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="0a711-407">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="0a711-408">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="0a711-408">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="0a711-409">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="0a711-409">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="0a711-410">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="0a711-410">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="0a711-411">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="0a711-411">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="0a711-412">Ezek az **New-AzBatchTask**`-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="0a711-412">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="0a711-413">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="0a711-413">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="0a711-414">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="0a711-414">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="0a711-415">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="0a711-415">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="0a711-416">A `PSApplication`**Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-416">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0a711-417">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="0a711-417">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="0a711-418">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="0a711-418">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="0a711-419">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-419">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0a711-420">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="0a711-420">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="0a711-421">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="0a711-421">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="0a711-422">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-422">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="0a711-423">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-423">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="0a711-424">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="0a711-424">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="0a711-425">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-425">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="0a711-426">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="0a711-426">This operation is no longer supported.</span></span>
* <span data-ttu-id="0a711-427">`PSCloudServiceConfiguration``TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-427">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0a711-428">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-428">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0a711-429">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="0a711-429">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="0a711-430">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="0a711-430">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="0a711-431">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="0a711-431">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="0a711-432">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="0a711-432">New non-verified images are also now returned.</span></span> <span data-ttu-id="0a711-433">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="0a711-433">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="0a711-434">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="0a711-434">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="0a711-435">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="0a711-435">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="0a711-436">Ez a `PSNetworkSecurityGroupRule``SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="0a711-436">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="0a711-437">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="0a711-437">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="0a711-438">Ezt a `PSTaskContainerSettings``WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="0a711-438">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="0a711-439">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="0a711-439">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="0a711-440">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="0a711-440">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="0a711-441">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="0a711-441">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="0a711-442">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="0a711-442">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a711-443">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a711-443">Az.Cdn</span></span>
* <span data-ttu-id="0a711-444">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="0a711-444">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="0a711-445">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="0a711-445">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-446">Az.Compute</span></span>
* <span data-ttu-id="0a711-447">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="0a711-447">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="0a711-448">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0a711-448">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="0a711-449">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="0a711-449">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="0a711-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0a711-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="0a711-451">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-451">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0a711-452">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-452">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="0a711-453">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="0a711-453">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="0a711-454">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-454">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="0a711-455">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="0a711-455">Breaking changes</span></span>
    - <span data-ttu-id="0a711-456">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="0a711-456">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="0a711-457">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="0a711-457">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a711-458">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a711-458">Az.DataFactory</span></span>
* <span data-ttu-id="0a711-459">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="0a711-459">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a711-460">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a711-460">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a711-461">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="0a711-461">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="0a711-462">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="0a711-462">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="0a711-463">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="0a711-463">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="0a711-464">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="0a711-464">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="0a711-465">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-465">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="0a711-466">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="0a711-466">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a711-467">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a711-467">Az.FrontDoor</span></span>
* <span data-ttu-id="0a711-468">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="0a711-468">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a711-469">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a711-469">Az.HDInsight</span></span>
* <span data-ttu-id="0a711-470">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-470">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="0a711-471">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="0a711-471">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="0a711-472">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="0a711-472">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="0a711-473">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="0a711-473">Removed five cmdlets:</span></span>
    - <span data-ttu-id="0a711-474">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0a711-474">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0a711-475">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0a711-475">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0a711-476">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0a711-476">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0a711-477">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0a711-477">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="0a711-478">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0a711-478">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="0a711-479">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="0a711-479">Added three cmdlets:</span></span>
    - <span data-ttu-id="0a711-480">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="0a711-480">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0a711-481">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="0a711-481">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0a711-482">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="0a711-482">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="0a711-483">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="0a711-483">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="0a711-484">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="0a711-484">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="0a711-485">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="0a711-485">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="0a711-486">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="0a711-486">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="0a711-487">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="0a711-487">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="0a711-488">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="0a711-488">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="0a711-489">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="0a711-489">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="0a711-490">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="0a711-490">Added some scenario test cases.</span></span>
* <span data-ttu-id="0a711-491">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="0a711-491">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a711-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a711-492">Az.IotHub</span></span>
* <span data-ttu-id="0a711-493">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="0a711-493">Breaking changes:</span></span>
    - <span data-ttu-id="0a711-494">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="0a711-494">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0a711-495">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-495">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0a711-496">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="0a711-496">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0a711-497">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-497">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0a711-498">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-498">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="0a711-499">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-499">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="0a711-500">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="0a711-500">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="0a711-501">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="0a711-501">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="0a711-502">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="0a711-502">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0a711-503">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-503">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0a711-504">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="0a711-504">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0a711-505">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-505">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-506">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-506">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a711-507">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="0a711-507">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="0a711-508">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="0a711-508">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="0a711-509">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="0a711-509">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="0a711-510">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="0a711-510">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="0a711-511">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="0a711-511">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="0a711-512">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="0a711-512">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="0a711-513">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="0a711-513">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="0a711-514">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="0a711-514">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="0a711-515">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="0a711-515">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-516">Az.Resources</span></span>
* <span data-ttu-id="0a711-517">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="0a711-517">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-518">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-518">Az.Network</span></span>
* <span data-ttu-id="0a711-519">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="0a711-519">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="0a711-520">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="0a711-520">Updated cmdlet:</span></span>
        - <span data-ttu-id="0a711-521">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-521">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a711-522">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-522">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a711-523">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-523">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a711-524">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-524">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a711-525">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-525">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0a711-526">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="0a711-526">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="0a711-527">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="0a711-527">New cmdlet:</span></span>
        - <span data-ttu-id="0a711-528">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="0a711-528">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="0a711-529">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-529">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="0a711-530">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="0a711-530">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="0a711-531">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="0a711-531">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="0a711-532">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="0a711-532">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="0a711-533">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="0a711-533">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="0a711-534">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="0a711-534">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="0a711-535">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-535">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="0a711-536">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="0a711-536">New cmdlets added:</span></span>
        - <span data-ttu-id="0a711-537">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="0a711-537">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="0a711-538">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a711-538">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0a711-539">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a711-539">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0a711-540">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a711-540">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0a711-541">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0a711-541">Set-AzVirtualHub</span></span>
* <span data-ttu-id="0a711-542">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-542">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="0a711-543">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="0a711-543">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0a711-544">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-544">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0a711-545">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-545">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0a711-546">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-546">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="0a711-547">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-547">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="0a711-548">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-548">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="0a711-549">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="0a711-549">New cmdlets added:</span></span>
        - <span data-ttu-id="0a711-550">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-550">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="0a711-551">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="0a711-551">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0a711-552">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-552">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0a711-553">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-553">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0a711-554">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-554">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0a711-555">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-555">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0a711-556">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-556">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="0a711-557">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-557">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="0a711-558">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="0a711-558">New cmdlets added:</span></span>
        - <span data-ttu-id="0a711-559">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="0a711-559">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="0a711-560">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="0a711-560">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="0a711-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="0a711-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="0a711-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="0a711-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="0a711-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="0a711-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="0a711-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a711-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="0a711-565">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="0a711-565">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0a711-566">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-566">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="0a711-567">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-567">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="0a711-568">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="0a711-568">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="0a711-569">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-569">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="0a711-570">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="0a711-570">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0a711-571">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-571">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="0a711-572">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-572">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="0a711-573">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="0a711-573">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="0a711-574">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="0a711-574">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="0a711-575">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-575">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="0a711-576">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="0a711-576">New cmdlets added:</span></span>
        - <span data-ttu-id="0a711-577">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0a711-577">New-AzIpGroup</span></span>
        - <span data-ttu-id="0a711-578">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0a711-578">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="0a711-579">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0a711-579">Get-AzIpGroup</span></span>
        - <span data-ttu-id="0a711-580">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0a711-580">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a711-581">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a711-581">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a711-582">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="0a711-582">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-583">Az.Sql</span></span>
* <span data-ttu-id="0a711-584">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="0a711-584">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="0a711-585">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="0a711-585">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="0a711-586">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="0a711-586">Removed deprecated aliases:</span></span>
* <span data-ttu-id="0a711-587">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="0a711-587">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="0a711-588">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="0a711-588">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="0a711-589">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="0a711-589">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0a711-590">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="0a711-590">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="0a711-591">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="0a711-591">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="0a711-592">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="0a711-592">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-593">Az.Storage</span></span>
* <span data-ttu-id="0a711-594">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="0a711-594">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="0a711-595">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a711-595">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0a711-596">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a711-596">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0a711-597">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="0a711-597">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="0a711-598">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0a711-598">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="0a711-599">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0a711-599">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="0a711-600">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="0a711-600">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="0a711-601">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="0a711-601">General</span></span>
* <span data-ttu-id="0a711-602">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="0a711-602">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a711-603">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-603">Az.Accounts</span></span>
* <span data-ttu-id="0a711-604">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="0a711-604">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0a711-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a711-605">Az.ApiManagement</span></span>
* <span data-ttu-id="0a711-606">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="0a711-606">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="0a711-607">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="0a711-607">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a711-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a711-608">Az.Automation</span></span>
* <span data-ttu-id="0a711-609">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="0a711-609">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="0a711-610">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a711-610">Az.Batch</span></span>
* <span data-ttu-id="0a711-611">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="0a711-611">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-612">Az.Compute</span></span>
* <span data-ttu-id="0a711-613">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-613">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0a711-614">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="0a711-614">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="0a711-615">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="0a711-615">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="0a711-616">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="0a711-616">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a711-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a711-617">Az.DataFactory</span></span>
* <span data-ttu-id="0a711-618">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="0a711-618">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="0a711-619">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="0a711-619">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="0a711-620">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="0a711-620">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a711-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a711-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a711-622">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="0a711-622">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0a711-623">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0a711-623">Az.HealthcareApis</span></span>
* <span data-ttu-id="0a711-624">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="0a711-624">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="0a711-625">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="0a711-625">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="0a711-626">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="0a711-626">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="0a711-627">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="0a711-627">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a711-628">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a711-628">Az.IotHub</span></span>
* <span data-ttu-id="0a711-629">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="0a711-629">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="0a711-630">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a711-630">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="0a711-631">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a711-631">Az.Monitor</span></span>
* <span data-ttu-id="0a711-632">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="0a711-632">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="0a711-633">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="0a711-633">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="0a711-634">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="0a711-634">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="0a711-635">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="0a711-635">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-636">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-636">Az.Network</span></span>
* <span data-ttu-id="0a711-637">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="0a711-637">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="0a711-638">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="0a711-638">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="0a711-639">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="0a711-639">New cmdlets added:</span></span>
        - <span data-ttu-id="0a711-640">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="0a711-640">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="0a711-641">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-641">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0a711-642">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="0a711-642">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="0a711-643">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="0a711-643">Updated cmdlets:</span></span>
        - <span data-ttu-id="0a711-644">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-644">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0a711-645">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-645">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0a711-646">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-646">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0a711-647">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="0a711-647">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="0a711-648">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="0a711-648">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="0a711-649">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="0a711-649">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="0a711-650">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="0a711-650">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0a711-651">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0a711-651">Az.RedisCache</span></span>
* <span data-ttu-id="0a711-652">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="0a711-652">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-653">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-653">Az.Sql</span></span>
* <span data-ttu-id="0a711-654">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="0a711-654">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-655">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-655">Az.Storage</span></span>
* <span data-ttu-id="0a711-656">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="0a711-656">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="0a711-657">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="0a711-657">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0a711-658">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0a711-658">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="0a711-659">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="0a711-659">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0a711-660">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a711-660">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0a711-661">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0a711-661">Az.StorageSync</span></span>
* <span data-ttu-id="0a711-662">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="0a711-662">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a711-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-663">Az.Websites</span></span>
* <span data-ttu-id="0a711-664">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="0a711-664">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="0a711-665">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="0a711-665">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0a711-666">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a711-666">Az.ApiManagement</span></span>
* <span data-ttu-id="0a711-667">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="0a711-667">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="0a711-668">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="0a711-668">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="0a711-669">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="0a711-669">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a711-670">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a711-670">Az.Automation</span></span>
* <span data-ttu-id="0a711-671">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="0a711-671">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="0a711-672">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-672">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="0a711-673">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="0a711-673">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-674">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-674">Az.Compute</span></span>
* <span data-ttu-id="0a711-675">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-675">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="0a711-676">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-676">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0a711-677">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="0a711-677">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="0a711-678">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-678">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="0a711-679">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-679">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="0a711-680">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="0a711-680">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="0a711-681">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="0a711-681">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="0a711-682">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-682">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="0a711-683">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-683">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a711-684">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a711-684">Az.DataFactory</span></span>
* <span data-ttu-id="0a711-685">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="0a711-685">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="0a711-686">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="0a711-686">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a711-687">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a711-687">Az.HDInsight</span></span>
* <span data-ttu-id="0a711-688">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="0a711-688">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a711-689">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a711-689">Az.IotHub</span></span>
* <span data-ttu-id="0a711-690">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="0a711-690">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="0a711-691">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="0a711-691">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="0a711-692">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="0a711-692">New cmdlets are:</span></span>
    - <span data-ttu-id="0a711-693">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0a711-693">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0a711-694">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0a711-694">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0a711-695">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0a711-695">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0a711-696">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0a711-696">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a711-697">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a711-697">Az.Monitor</span></span>
* <span data-ttu-id="0a711-698">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="0a711-698">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="0a711-699">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="0a711-699">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="0a711-700">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="0a711-700">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="0a711-701">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="0a711-701">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="0a711-702">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-702">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="0a711-703">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="0a711-703">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="0a711-704">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="0a711-704">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="0a711-705">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="0a711-705">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="0a711-706">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="0a711-706">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0a711-707">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="0a711-707">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="0a711-708">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="0a711-708">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0a711-709">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="0a711-709">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="0a711-710">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-710">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="0a711-711">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="0a711-711">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="0a711-712">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="0a711-712">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="0a711-713">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="0a711-713">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="0a711-714">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="0a711-714">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="0a711-715">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="0a711-715">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="0a711-716">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="0a711-716">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="0a711-717">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="0a711-717">Overall improved help files</span></span>
* <span data-ttu-id="0a711-718">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="0a711-718">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-719">Az.Network</span></span>
* <span data-ttu-id="0a711-720">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="0a711-720">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="0a711-721">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="0a711-721">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="0a711-722">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="0a711-722">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="0a711-723">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="0a711-723">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="0a711-724">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="0a711-724">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="0a711-725">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="0a711-725">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="0a711-726">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="0a711-726">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="0a711-727">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-727">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="0a711-728">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-728">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="0a711-729">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="0a711-729">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="0a711-730">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="0a711-730">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="0a711-731">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="0a711-731">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="0a711-732">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a711-732">New cmdlets</span></span>
        - <span data-ttu-id="0a711-733">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="0a711-733">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="0a711-734">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-734">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="0a711-735">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="0a711-735">Updated cmdlet:</span></span>
        - <span data-ttu-id="0a711-736">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="0a711-736">New-VpnSite</span></span>
        - <span data-ttu-id="0a711-737">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="0a711-737">Update-VpnSite</span></span>
        - <span data-ttu-id="0a711-738">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-738">New-VpnConnection</span></span>
        - <span data-ttu-id="0a711-739">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-739">Update-VpnConnection</span></span>
* <span data-ttu-id="0a711-740">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="0a711-740">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-741">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-741">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a711-742">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="0a711-742">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="0a711-743">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="0a711-743">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-744">Az.Resources</span></span>
* <span data-ttu-id="0a711-745">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="0a711-745">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a711-746">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a711-746">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a711-747">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="0a711-747">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="0a711-748">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="0a711-748">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="0a711-749">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0a711-749">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0a711-750">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0a711-750">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0a711-751">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0a711-751">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0a711-752">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0a711-752">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="0a711-753">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0a711-753">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0a711-754">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0a711-754">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0a711-755">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0a711-755">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0a711-756">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0a711-756">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0a711-757">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0a711-757">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="0a711-758">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0a711-758">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0a711-759">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0a711-759">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0a711-760">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0a711-760">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0a711-761">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="0a711-761">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="0a711-762">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="0a711-762">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0a711-763">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0a711-763">Az.SignalR</span></span>
* <span data-ttu-id="0a711-764">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a711-764">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-765">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-765">Az.Sql</span></span>
* <span data-ttu-id="0a711-766">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="0a711-766">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="0a711-767">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="0a711-767">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="0a711-768">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="0a711-768">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="0a711-769">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="0a711-769">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="0a711-770">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="0a711-770">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-771">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-771">Az.Storage</span></span>
* <span data-ttu-id="0a711-772">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="0a711-772">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="0a711-773">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-773">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="0a711-774">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0a711-774">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="0a711-775">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0a711-775">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="0a711-776">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-776">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="0a711-777">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0a711-777">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="0a711-778">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="0a711-778">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="0a711-779">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a711-779">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0a711-780">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a711-780">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0a711-781">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a711-781">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0a711-782">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a711-782">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a711-783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-783">Az.Websites</span></span>
* <span data-ttu-id="0a711-784">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="0a711-784">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="0a711-785">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="0a711-785">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="0a711-786">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="0a711-786">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="0a711-787">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="0a711-787">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="0a711-788">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="0a711-788">General</span></span>
* <span data-ttu-id="0a711-789">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="0a711-789">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a711-790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-790">Az.Accounts</span></span>
* <span data-ttu-id="0a711-791">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="0a711-791">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="0a711-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0a711-792">Az.Aks</span></span>
* <span data-ttu-id="0a711-793">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="0a711-793">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="0a711-794">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="0a711-794">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0a711-795">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a711-795">Az.ApiManagement</span></span>
* <span data-ttu-id="0a711-796">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="0a711-796">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="0a711-797">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="0a711-797">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="0a711-798">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="0a711-798">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="0a711-799">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="0a711-799">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="0a711-800">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="0a711-800">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0a711-801">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a711-801">Az.Batch</span></span>
* <span data-ttu-id="0a711-802">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="0a711-802">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a711-803">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a711-803">Az.Cdn</span></span>
* <span data-ttu-id="0a711-804">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="0a711-804">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-805">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-805">Az.Compute</span></span>
* <span data-ttu-id="0a711-806">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-806">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="0a711-807">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-807">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="0a711-808">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-808">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="0a711-809">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="0a711-809">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="0a711-810">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="0a711-810">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="0a711-811">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-811">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="0a711-812">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="0a711-812">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="0a711-813">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="0a711-813">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a711-814">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a711-814">Az.DataFactory</span></span>
* <span data-ttu-id="0a711-815">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="0a711-815">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="0a711-816">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="0a711-816">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="0a711-817">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="0a711-817">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="0a711-818">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="0a711-818">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a711-819">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a711-819">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a711-820">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="0a711-820">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a711-821">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a711-821">Az.EventHub</span></span>
* <span data-ttu-id="0a711-822">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="0a711-822">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="0a711-823">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="0a711-823">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="0a711-824">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-824">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="0a711-825">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="0a711-825">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="0a711-826">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0a711-826">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0a711-827">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="0a711-827">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a711-828">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a711-828">Az.Monitor</span></span>
* <span data-ttu-id="0a711-829">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="0a711-829">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-830">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-830">Az.Network</span></span>
* <span data-ttu-id="0a711-831">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-831">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="0a711-832">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="0a711-832">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="0a711-833">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="0a711-833">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="0a711-834">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="0a711-834">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="0a711-835">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="0a711-835">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="0a711-836">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="0a711-836">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="0a711-837">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="0a711-837">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a711-838">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a711-838">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a711-839">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="0a711-839">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="0a711-840">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-840">Added example</span></span>
    - <span data-ttu-id="0a711-841">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="0a711-841">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="0a711-842">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-842">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="0a711-843">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="0a711-843">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-844">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-844">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a711-845">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="0a711-845">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-846">Az.Resources</span></span>
* <span data-ttu-id="0a711-847">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="0a711-847">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="0a711-848">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-848">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="0a711-849">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="0a711-849">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="0a711-850">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-850">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a711-851">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a711-851">Az.ServiceBus</span></span>
* <span data-ttu-id="0a711-852">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="0a711-852">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="0a711-853">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="0a711-853">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="0a711-854">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="0a711-854">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="0a711-855">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a711-855">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a711-856">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="0a711-856">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="0a711-857">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="0a711-857">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="0a711-858">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="0a711-858">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="0a711-859">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="0a711-859">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="0a711-860">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="0a711-860">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="0a711-861">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="0a711-861">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-862">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-862">Az.Sql</span></span>
* <span data-ttu-id="0a711-863">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="0a711-863">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-864">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-864">Az.Storage</span></span>
* <span data-ttu-id="0a711-865">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="0a711-865">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="0a711-866">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="0a711-866">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="0a711-867">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0a711-867">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="0a711-868">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0a711-868">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="0a711-869">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="0a711-869">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="0a711-870">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0a711-870">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a711-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-871">Az.Websites</span></span>
* <span data-ttu-id="0a711-872">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="0a711-872">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="0a711-873">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="0a711-873">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a711-874">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-874">Az.Accounts</span></span>
* <span data-ttu-id="0a711-875">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="0a711-875">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="0a711-876">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="0a711-876">Az.ApplicationInsights</span></span>
* <span data-ttu-id="0a711-877">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="0a711-877">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="0a711-878">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a711-878">Az.Automation</span></span>
* <span data-ttu-id="0a711-879">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="0a711-879">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a711-880">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a711-880">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a711-881">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="0a711-881">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-882">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-882">Az.Compute</span></span>
* <span data-ttu-id="0a711-883">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="0a711-883">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0a711-884">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0a711-884">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0a711-885">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="0a711-885">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="0a711-886">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="0a711-886">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a711-887">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a711-887">Az.DataFactory</span></span>
* <span data-ttu-id="0a711-888">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="0a711-888">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="0a711-889">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="0a711-889">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a711-890">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a711-890">Az.EventHub</span></span>
* <span data-ttu-id="0a711-891">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="0a711-891">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0a711-892">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="0a711-892">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a711-893">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a711-893">Az.KeyVault</span></span>
* <span data-ttu-id="0a711-894">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="0a711-894">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0a711-895">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0a711-895">Az.LogicApp</span></span>
* <span data-ttu-id="0a711-896">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="0a711-896">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="0a711-897">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="0a711-897">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="0a711-898">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="0a711-898">Az.ManagedServices</span></span>
* <span data-ttu-id="0a711-899">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-899">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-900">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-900">Az.Network</span></span>
* <span data-ttu-id="0a711-901">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-901">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="0a711-902">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a711-902">New cmdlets</span></span>
        - <span data-ttu-id="0a711-903">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a711-903">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0a711-904">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a711-904">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0a711-905">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-905">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a711-906">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-906">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a711-907">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-907">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a711-908">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-908">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a711-909">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="0a711-909">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="0a711-910">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a711-910">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="0a711-911">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="0a711-911">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="0a711-912">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="0a711-912">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="0a711-913">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-913">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="0a711-914">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-914">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="0a711-915">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="0a711-915">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="0a711-916">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-916">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="0a711-917">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a711-917">Updated cmdlets</span></span>
        - <span data-ttu-id="0a711-918">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-918">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0a711-919">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-919">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0a711-920">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-920">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0a711-921">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="0a711-921">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0a711-922">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="0a711-922">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="0a711-923">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="0a711-923">Updated cmdlet:</span></span>
        - <span data-ttu-id="0a711-924">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-924">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0a711-925">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-925">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0a711-926">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-926">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="0a711-927">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="0a711-927">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="0a711-928">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="0a711-928">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="0a711-929">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="0a711-929">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a711-930">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a711-930">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a711-931">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="0a711-931">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="0a711-932">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="0a711-932">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-933">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-933">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a711-934">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-934">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0a711-935">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-935">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="0a711-936">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-936">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="0a711-937">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-937">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0a711-938">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-938">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="0a711-939">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-939">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0a711-940">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-940">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="0a711-941">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-941">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0a711-942">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-942">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="0a711-943">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-943">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-944">Az.Resources</span></span>
- <span data-ttu-id="0a711-945">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0a711-945">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="0a711-946">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="0a711-946">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a711-947">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a711-947">Az.ServiceBus</span></span>
* <span data-ttu-id="0a711-948">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="0a711-948">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0a711-949">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="0a711-949">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-950">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-950">Az.Sql</span></span>
* <span data-ttu-id="0a711-951">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="0a711-951">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="0a711-952">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="0a711-952">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="0a711-953">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="0a711-953">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-954">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-954">Az.Storage</span></span>
* <span data-ttu-id="0a711-955">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="0a711-955">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0a711-956">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0a711-956">Az.StorageSync</span></span>
* <span data-ttu-id="0a711-957">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="0a711-957">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="0a711-958">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="0a711-958">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a711-959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-959">Az.Websites</span></span>
* <span data-ttu-id="0a711-960">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="0a711-960">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="0a711-961">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-961">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="0a711-962">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="0a711-962">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="0a711-963">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="0a711-963">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a711-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-964">Az.Accounts</span></span>
* <span data-ttu-id="0a711-965">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="0a711-965">Add support for profile cmdlets</span></span>
* <span data-ttu-id="0a711-966">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="0a711-966">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="0a711-967">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="0a711-967">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0a711-968">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0a711-968">Az.Advisor</span></span>
* <span data-ttu-id="0a711-969">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="0a711-969">GA release of Az.Advisor</span></span>
* <span data-ttu-id="0a711-970">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="0a711-970">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0a711-971">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a711-971">Az.ApiManagement</span></span>
* <span data-ttu-id="0a711-972">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="0a711-972">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="0a711-973">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0a711-973">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="0a711-974">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-974">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="0a711-975">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-975">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="0a711-976">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="0a711-976">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="0a711-977">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0a711-977">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="0a711-978">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="0a711-978">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a711-979">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a711-979">Az.Automation</span></span>
* <span data-ttu-id="0a711-980">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="0a711-980">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-981">Az.Compute</span></span>
* <span data-ttu-id="0a711-982">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-982">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a711-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a711-983">Az.DataFactory</span></span>
* <span data-ttu-id="0a711-984">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="0a711-984">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0a711-985">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0a711-985">Az.EventGrid</span></span>
* <span data-ttu-id="0a711-986">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="0a711-986">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a711-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a711-987">Az.IotHub</span></span>
* <span data-ttu-id="0a711-988">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="0a711-988">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-989">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-989">Az.Network</span></span>
* <span data-ttu-id="0a711-990">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="0a711-990">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="0a711-991">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="0a711-991">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a711-992">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a711-992">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a711-993">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="0a711-993">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="0a711-994">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="0a711-994">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a711-995">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a711-995">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a711-996">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="0a711-996">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-997">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-997">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a711-998">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="0a711-998">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-999">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-999">Az.Resources</span></span>
    - <span data-ttu-id="0a711-1000">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="0a711-1000">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="0a711-1001">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1001">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="0a711-1002">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1002">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="0a711-1003">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1003">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a711-1004">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a711-1004">Az.ServiceBus</span></span>
* <span data-ttu-id="0a711-1005">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="0a711-1005">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-1006">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-1006">Az.Sql</span></span>
* <span data-ttu-id="0a711-1007">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1007">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="0a711-1008">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="0a711-1008">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="0a711-1009">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0a711-1009">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0a711-1010">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0a711-1010">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0a711-1011">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0a711-1011">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0a711-1012">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0a711-1012">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0a711-1013">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0a711-1013">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0a711-1014">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0a711-1014">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="0a711-1015">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="0a711-1015">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-1016">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-1016">Az.Storage</span></span>
* <span data-ttu-id="0a711-1017">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="0a711-1017">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="0a711-1018">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0a711-1018">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="0a711-1019">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="0a711-1019">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="0a711-1020">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="0a711-1020">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="0a711-1021">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="0a711-1021">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="0a711-1022">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a711-1022">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0a711-1023">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a711-1023">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0a711-1024">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="0a711-1024">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="0a711-1025">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0a711-1025">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="0a711-1026">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0a711-1026">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0a711-1027">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0a711-1027">Az.StorageSync</span></span>
* <span data-ttu-id="0a711-1028">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="0a711-1028">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="0a711-1029">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="0a711-1029">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a711-1030">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-1030">Az.Accounts</span></span>
* <span data-ttu-id="0a711-1031">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1031">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="0a711-1032">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="0a711-1032">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="0a711-1033">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1033">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="0a711-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0a711-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="0a711-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="0a711-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1036">Az.Compute</span></span>
* <span data-ttu-id="0a711-1037">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="0a711-1037">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="0a711-1038">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="0a711-1038">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="0a711-1039">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0a711-1039">Az.Dns</span></span>
* <span data-ttu-id="0a711-1040">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="0a711-1040">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0a711-1041">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0a711-1041">Az.EventGrid</span></span>
* <span data-ttu-id="0a711-1042">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="0a711-1042">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="0a711-1043">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="0a711-1043">New cmdlets:</span></span>
    - <span data-ttu-id="0a711-1044">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0a711-1044">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0a711-1045">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="0a711-1045">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0a711-1046">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0a711-1046">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0a711-1047">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="0a711-1047">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="0a711-1048">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0a711-1048">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0a711-1049">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="0a711-1049">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0a711-1050">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0a711-1050">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0a711-1051">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-1051">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0a711-1052">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0a711-1052">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0a711-1053">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="0a711-1053">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="0a711-1054">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="0a711-1054">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0a711-1055">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0a711-1055">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="0a711-1056">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="0a711-1056">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="0a711-1057">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="0a711-1057">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="0a711-1058">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="0a711-1058">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0a711-1059">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="0a711-1059">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="0a711-1060">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="0a711-1060">Updated cmdlets:</span></span>
    - <span data-ttu-id="0a711-1061">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="0a711-1061">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="0a711-1062">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="0a711-1062">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0a711-1063">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="0a711-1063">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0a711-1064">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="0a711-1064">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="0a711-1065">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="0a711-1065">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="0a711-1066">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="0a711-1066">Event subscription expiration date,</span></span>
            - <span data-ttu-id="0a711-1067">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="0a711-1067">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="0a711-1068">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="0a711-1068">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="0a711-1069">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="0a711-1069">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="0a711-1070">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="0a711-1070">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="0a711-1071">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="0a711-1071">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="0a711-1072">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0a711-1072">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="0a711-1073">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="0a711-1073">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="0a711-1074">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="0a711-1074">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a711-1075">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a711-1075">Az.FrontDoor</span></span>
* <span data-ttu-id="0a711-1076">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="0a711-1076">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="0a711-1077">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="0a711-1077">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="0a711-1078">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="0a711-1078">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="0a711-1079">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="0a711-1079">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-1080">Az.Network</span></span>
* <span data-ttu-id="0a711-1081">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-1081">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="0a711-1082">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a711-1082">New cmdlets</span></span>
        - <span data-ttu-id="0a711-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="0a711-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="0a711-1084">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-1084">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="0a711-1085">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a711-1085">New cmdlets</span></span> 
        - <span data-ttu-id="0a711-1086">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="0a711-1086">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="0a711-1087">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-1087">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="0a711-1088">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a711-1088">New cmdlets</span></span> 
        - <span data-ttu-id="0a711-1089">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a711-1089">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="0a711-1090">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a711-1090">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0a711-1091">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a711-1091">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0a711-1092">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-1092">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="0a711-1093">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-1093">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0a711-1094">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-1094">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="0a711-1095">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a711-1095">New cmdlets</span></span>
        - <span data-ttu-id="0a711-1096">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a711-1096">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0a711-1097">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a711-1097">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0a711-1098">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a711-1098">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0a711-1099">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="0a711-1099">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="0a711-1100">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="0a711-1100">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="0a711-1101">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="0a711-1101">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="0a711-1102">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="0a711-1102">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="0a711-1103">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-1103">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="0a711-1104">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-1104">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="0a711-1105">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="0a711-1105">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="0a711-1106">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="0a711-1106">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="0a711-1107">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="0a711-1107">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="0a711-1108">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1108">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="0a711-1109">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="0a711-1109">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="0a711-1110">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1110">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="0a711-1111">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1111">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="0a711-1112">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="0a711-1112">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="0a711-1113">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1113">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="0a711-1114">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="0a711-1114">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0a711-1115">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="0a711-1115">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="0a711-1116">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="0a711-1116">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="0a711-1117">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="0a711-1117">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="0a711-1118">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="0a711-1118">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="0a711-1119">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-1119">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="0a711-1120">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-1120">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0a711-1121">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-1121">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0a711-1122">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-1122">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a711-1123">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a711-1123">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a711-1124">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1124">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-1125">Az.Resources</span></span>
* <span data-ttu-id="0a711-1126">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="0a711-1126">Support for additional Template Export options</span></span>
    - <span data-ttu-id="0a711-1127">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1127">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0a711-1128">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1128">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0a711-1129">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-1129">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a711-1130">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a711-1130">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a711-1131">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="0a711-1131">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-1132">Az.Sql</span></span>
* <span data-ttu-id="0a711-1133">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="0a711-1133">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="0a711-1134">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="0a711-1134">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="0a711-1135">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1135">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="0a711-1136">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0a711-1136">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0a711-1137">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0a711-1137">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0a711-1138">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0a711-1138">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0a711-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0a711-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="0a711-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0a711-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-1141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-1141">Az.Storage</span></span>
* <span data-ttu-id="0a711-1142">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="0a711-1142">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="0a711-1143">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a711-1143">New-AzStorageAccount</span></span>
* <span data-ttu-id="0a711-1144">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="0a711-1144">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="0a711-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0a711-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a711-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-1146">Az.Websites</span></span>
* <span data-ttu-id="0a711-1147">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="0a711-1147">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="0a711-1148">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1148">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="0a711-1149">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="0a711-1149">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="0a711-1150">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a711-1150">Az.Cdn</span></span>
* <span data-ttu-id="0a711-1151">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="0a711-1151">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-1152">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1152">Az.Compute</span></span>
* <span data-ttu-id="0a711-1153">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="0a711-1153">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="0a711-1154">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="0a711-1154">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a711-1155">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a711-1155">Az.EventHub</span></span>
* <span data-ttu-id="0a711-1156">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="0a711-1156">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="0a711-1157">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="0a711-1157">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-1158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-1158">Az.Network</span></span>
* <span data-ttu-id="0a711-1159">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="0a711-1159">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="0a711-1160">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="0a711-1160">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a711-1161">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a711-1161">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a711-1162">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="0a711-1162">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-1163">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1163">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a711-1164">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="0a711-1164">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a711-1165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a711-1165">Az.ServiceBus</span></span>
* <span data-ttu-id="0a711-1166">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="0a711-1166">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a711-1167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a711-1167">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a711-1168">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="0a711-1168">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="0a711-1169">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="0a711-1169">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-1170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-1170">Az.Sql</span></span>
* <span data-ttu-id="0a711-1171">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="0a711-1171">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="0a711-1172">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="0a711-1172">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0a711-1173">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="0a711-1173">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="0a711-1174">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="0a711-1174">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a711-1175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-1175">Az.Websites</span></span>
* <span data-ttu-id="0a711-1176">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="0a711-1176">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="0a711-1177">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="0a711-1177">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0a711-1178">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a711-1178">Az.ApiManagement</span></span>
* <span data-ttu-id="0a711-1179">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="0a711-1179">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="0a711-1180">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="0a711-1180">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="0a711-1181">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="0a711-1181">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="0a711-1182">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="0a711-1182">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="0a711-1183">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="0a711-1183">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="0a711-1184">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1184">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="0a711-1185">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="0a711-1185">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="0a711-1186">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="0a711-1186">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="0a711-1187">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-1187">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="0a711-1188">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="0a711-1188">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="0a711-1189">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="0a711-1189">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="0a711-1190">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0a711-1190">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="0a711-1191">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1191">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="0a711-1192">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-1192">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="0a711-1193">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1193">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="0a711-1194">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="0a711-1194">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="0a711-1195">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0a711-1195">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="0a711-1196">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1196">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="0a711-1197">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="0a711-1197">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="0a711-1198">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="0a711-1198">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="0a711-1199">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-1199">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="0a711-1200">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="0a711-1200">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="0a711-1201">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="0a711-1201">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="0a711-1202">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-1202">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="0a711-1203">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="0a711-1203">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="0a711-1204">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="0a711-1204">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="0a711-1205">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="0a711-1205">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="0a711-1206">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="0a711-1206">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="0a711-1207">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="0a711-1207">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="0a711-1208">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="0a711-1208">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="0a711-1209">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-1209">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="0a711-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="0a711-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="0a711-1211">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="0a711-1211">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="0a711-1212">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1212">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0a711-1213">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="0a711-1213">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="0a711-1214">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="0a711-1214">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="0a711-1215">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="0a711-1215">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="0a711-1216">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="0a711-1216">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="0a711-1217">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="0a711-1217">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="0a711-1218">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1218">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="0a711-1219">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="0a711-1219">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0a711-1220">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="0a711-1220">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="0a711-1221">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="0a711-1221">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="0a711-1222">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="0a711-1222">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="0a711-1223">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1223">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0a711-1224">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="0a711-1224">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0a711-1225">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="0a711-1225">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="0a711-1226">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="0a711-1226">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="0a711-1227">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1227">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="0a711-1228">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="0a711-1228">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="0a711-1229">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="0a711-1229">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="0a711-1230">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="0a711-1230">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="0a711-1231">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="0a711-1231">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="0a711-1232">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1232">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="0a711-1233">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="0a711-1233">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="0a711-1234">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="0a711-1234">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="0a711-1235">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1235">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0a711-1236">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1236">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0a711-1237">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1237">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0a711-1238">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-1238">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0a711-1239">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1239">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0a711-1240">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1240">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0a711-1241">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1241">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0a711-1242">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-1242">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0a711-1243">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="0a711-1243">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="0a711-1244">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0a711-1244">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="0a711-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="0a711-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="0a711-1246">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0a711-1246">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="0a711-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="0a711-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="0a711-1248">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="0a711-1248">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="0a711-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="0a711-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="0a711-1250">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="0a711-1250">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="0a711-1251">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0a711-1251">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="0a711-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="0a711-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="0a711-1253">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="0a711-1253">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="0a711-1254">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="0a711-1254">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="0a711-1255">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0a711-1255">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a711-1256">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a711-1256">Az.Automation</span></span>
* <span data-ttu-id="0a711-1257">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-1257">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="0a711-1258">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="0a711-1258">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="0a711-1259">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="0a711-1259">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="0a711-1260">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="0a711-1260">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="0a711-1261">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="0a711-1261">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="0a711-1262">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="0a711-1262">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="0a711-1263">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="0a711-1263">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1264">Az.Compute</span></span>
* <span data-ttu-id="0a711-1265">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1265">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="0a711-1266">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="0a711-1266">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a711-1267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a711-1267">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a711-1268">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="0a711-1268">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a711-1269">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a711-1269">Az.Monitor</span></span>
* <span data-ttu-id="0a711-1270">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="0a711-1270">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-1271">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-1271">Az.Network</span></span>
* <span data-ttu-id="0a711-1272">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1272">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="0a711-1273">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="0a711-1273">Updated cmdlet:</span></span>
        - <span data-ttu-id="0a711-1274">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a711-1274">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="0a711-1275">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="0a711-1275">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-1276">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-1276">Az.Resources</span></span>
* <span data-ttu-id="0a711-1277">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-1277">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-1278">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-1278">Az.Sql</span></span>
* <span data-ttu-id="0a711-1279">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="0a711-1279">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="0a711-1280">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="0a711-1280">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a711-1281">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-1281">Az.Accounts</span></span>
* <span data-ttu-id="0a711-1282">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="0a711-1282">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a711-1283">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1283">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a711-1284">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="0a711-1284">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="0a711-1285">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="0a711-1285">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1286">Az.Compute</span></span>
* <span data-ttu-id="0a711-1287">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="0a711-1287">Proximity placement group feature.</span></span>
    - <span data-ttu-id="0a711-1288">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="0a711-1288">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="0a711-1289">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-1289">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="0a711-1290">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-1290">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="0a711-1291">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="0a711-1291">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="0a711-1292">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1292">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="0a711-1293">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="0a711-1293">Breaking changes</span></span>
    - <span data-ttu-id="0a711-1294">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="0a711-1294">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="0a711-1295">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="0a711-1295">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0a711-1296">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0a711-1296">Az.DeploymentManager</span></span>
* <span data-ttu-id="0a711-1297">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="0a711-1297">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="0a711-1298">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0a711-1298">Az.Dns</span></span>
* <span data-ttu-id="0a711-1299">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="0a711-1299">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="0a711-1300">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1300">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="0a711-1301">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="0a711-1301">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a711-1302">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a711-1302">Az.FrontDoor</span></span>
* <span data-ttu-id="0a711-1303">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="0a711-1303">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="0a711-1304">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="0a711-1304">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="0a711-1305">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a711-1305">Az.HDInsight</span></span>
* <span data-ttu-id="0a711-1306">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="0a711-1306">Removed two cmdlets:</span></span>
    - <span data-ttu-id="0a711-1307">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0a711-1307">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="0a711-1308">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0a711-1308">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0a711-1309">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="0a711-1309">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0a711-1310">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="0a711-1310">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="0a711-1311">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="0a711-1311">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="0a711-1312">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="0a711-1312">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a711-1313">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a711-1313">Az.Monitor</span></span>
* <span data-ttu-id="0a711-1314">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="0a711-1314">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="0a711-1315">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="0a711-1315">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="0a711-1316">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="0a711-1316">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="0a711-1317">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="0a711-1317">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="0a711-1318">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="0a711-1318">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="0a711-1319">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="0a711-1319">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="0a711-1320">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="0a711-1320">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="0a711-1321">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0a711-1321">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0a711-1322">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0a711-1322">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0a711-1323">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0a711-1323">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0a711-1324">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0a711-1324">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0a711-1325">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0a711-1325">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0a711-1326">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="0a711-1326">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="0a711-1327">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="0a711-1327">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-1328">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-1328">Az.Network</span></span>
* <span data-ttu-id="0a711-1329">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-1329">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="0a711-1330">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a711-1330">New cmdlets</span></span>
        - <span data-ttu-id="0a711-1331">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0a711-1331">New-AzNatGateway</span></span>
        - <span data-ttu-id="0a711-1332">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0a711-1332">Get-AzNatGateway</span></span>
        - <span data-ttu-id="0a711-1333">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0a711-1333">Set-AzNatGateway</span></span>
        - <span data-ttu-id="0a711-1334">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0a711-1334">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="0a711-1335">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a711-1335">Updated cmdlets</span></span>
        - <span data-ttu-id="0a711-1336">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0a711-1336">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="0a711-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0a711-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="0a711-1338">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="0a711-1338">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="0a711-1339">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="0a711-1339">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="0a711-1340">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="0a711-1340">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a711-1341">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a711-1341">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a711-1342">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="0a711-1342">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="0a711-1343">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-1343">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="0a711-1344">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="0a711-1344">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-1345">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1345">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a711-1346">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="0a711-1346">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="0a711-1347">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="0a711-1347">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="0a711-1348">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="0a711-1348">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="0a711-1349">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="0a711-1349">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="0a711-1350">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="0a711-1350">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="0a711-1351">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="0a711-1351">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="0a711-1352">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0a711-1352">Az.Relay</span></span>
* <span data-ttu-id="0a711-1353">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="0a711-1353">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a711-1354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a711-1354">Az.ServiceBus</span></span>
* <span data-ttu-id="0a711-1355">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="0a711-1355">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-1356">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-1356">Az.Storage</span></span>
* <span data-ttu-id="0a711-1357">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="0a711-1357">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="0a711-1358">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="0a711-1358">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="0a711-1359">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="0a711-1359">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="0a711-1360">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a711-1360">New-AzStorageAccount</span></span>
* <span data-ttu-id="0a711-1361">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="0a711-1361">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="0a711-1362">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a711-1362">New-AzStorageAccount</span></span>
    - <span data-ttu-id="0a711-1363">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a711-1363">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="0a711-1364">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a711-1364">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a711-1365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-1365">Az.Websites</span></span>
* <span data-ttu-id="0a711-1366">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1366">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="0a711-1367">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="0a711-1367">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="0a711-1368">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="0a711-1368">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a711-1369">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="0a711-1369">Highlights since the last major release</span></span>
* <span data-ttu-id="0a711-1370">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="0a711-1370">General availability of `Az` module</span></span>
* <span data-ttu-id="0a711-1371">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0a711-1371">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0a711-1372">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0a711-1372">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0a711-1373">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1373">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0a711-1374">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1374">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0a711-1375">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1375">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0a711-1376">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1376">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a711-1377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-1377">Az.Accounts</span></span>
* <span data-ttu-id="0a711-1378">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1378">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0a711-1379">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a711-1379">Az.Batch</span></span>
* <span data-ttu-id="0a711-1380">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1380">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a711-1381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a711-1381">Az.Cdn</span></span>
* <span data-ttu-id="0a711-1382">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1382">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a711-1383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1383">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a711-1384">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1384">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1385">Az.Compute</span></span>
* <span data-ttu-id="0a711-1386">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="0a711-1386">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="0a711-1387">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1387">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a711-1388">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="0a711-1388">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a711-1389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a711-1389">Az.DataFactory</span></span>
* <span data-ttu-id="0a711-1390">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="0a711-1390">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a711-1391">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a711-1391">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a711-1392">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1392">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0a711-1393">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0a711-1393">Az.EventGrid</span></span>
* <span data-ttu-id="0a711-1394">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="0a711-1394">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a711-1395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a711-1395">Az.EventHub</span></span>
* <span data-ttu-id="0a711-1396">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="0a711-1396">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="0a711-1397">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a711-1397">Az.HDInsight</span></span>
* <span data-ttu-id="0a711-1398">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1398">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a711-1399">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a711-1399">Az.IotHub</span></span>
* <span data-ttu-id="0a711-1400">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1400">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a711-1401">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a711-1401">Az.KeyVault</span></span>
* <span data-ttu-id="0a711-1402">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1402">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a711-1403">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="0a711-1403">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0a711-1404">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0a711-1404">Az.MachineLearning</span></span>
* <span data-ttu-id="0a711-1405">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1405">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="0a711-1406">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0a711-1406">Az.Media</span></span>
* <span data-ttu-id="0a711-1407">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1407">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a711-1408">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a711-1408">Az.Monitor</span></span>
  * <span data-ttu-id="0a711-1409">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a711-1409">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="0a711-1410">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="0a711-1410">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="0a711-1411">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="0a711-1411">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="0a711-1412">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0a711-1412">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0a711-1413">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0a711-1413">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0a711-1414">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0a711-1414">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="0a711-1415">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="0a711-1415">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-1416">Az.Network</span></span>
* <span data-ttu-id="0a711-1417">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1417">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a711-1418">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="0a711-1418">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="0a711-1419">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="0a711-1419">Az.NotificationHubs</span></span>
* <span data-ttu-id="0a711-1420">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1420">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a711-1421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a711-1421">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a711-1422">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1422">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="0a711-1423">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="0a711-1423">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="0a711-1424">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1424">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-1425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1425">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a711-1426">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1426">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a711-1427">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="0a711-1427">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="0a711-1428">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="0a711-1428">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="0a711-1429">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="0a711-1429">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0a711-1430">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0a711-1430">Az.RedisCache</span></span>
* <span data-ttu-id="0a711-1431">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1431">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-1432">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-1432">Az.Resources</span></span>
* <span data-ttu-id="0a711-1433">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="0a711-1433">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-1434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-1434">Az.Sql</span></span>
* <span data-ttu-id="0a711-1435">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="0a711-1435">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="0a711-1436">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1436">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a711-1437">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="0a711-1437">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="0a711-1438">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0a711-1438">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="0a711-1439">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="0a711-1439">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="0a711-1440">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="0a711-1440">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="0a711-1441">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="0a711-1441">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a711-1442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-1442">Az.Websites</span></span>
* <span data-ttu-id="0a711-1443">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="0a711-1443">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="0a711-1444">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1444">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a711-1445">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="0a711-1445">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="0a711-1446">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="0a711-1446">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="0a711-1447">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="0a711-1447">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a711-1448">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="0a711-1448">Highlights since the last major release</span></span>
* <span data-ttu-id="0a711-1449">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="0a711-1449">General availability of `Az` module</span></span>
* <span data-ttu-id="0a711-1450">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0a711-1450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0a711-1451">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0a711-1451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0a711-1452">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0a711-1453">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0a711-1454">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0a711-1455">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a711-1456">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-1456">Az.Accounts</span></span>
* <span data-ttu-id="0a711-1457">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="0a711-1457">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0a711-1458">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1458">Az.AnalysisServices</span></span>
* <span data-ttu-id="0a711-1459">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0a711-1459">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="0a711-1460">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-1460">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a711-1461">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a711-1461">Az.Automation</span></span>
* <span data-ttu-id="0a711-1462">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="0a711-1462">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="0a711-1463">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="0a711-1463">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="0a711-1464">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1464">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-1465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1465">Az.Compute</span></span>
* <span data-ttu-id="0a711-1466">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1466">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0a711-1467">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="0a711-1467">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="0a711-1468">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0a711-1468">Az.ContainerInstance</span></span>
* <span data-ttu-id="0a711-1469">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="0a711-1469">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a711-1470">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a711-1470">Az.DataFactory</span></span>
* <span data-ttu-id="0a711-1471">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="0a711-1471">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="0a711-1472">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="0a711-1472">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-1473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-1473">Az.Resources</span></span>
* <span data-ttu-id="0a711-1474">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="0a711-1474">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="0a711-1475">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1475">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="0a711-1476">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="0a711-1476">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="0a711-1477">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0a711-1477">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="0a711-1478">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-1478">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="0a711-1479">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0a711-1479">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-1480">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-1480">Az.Sql</span></span>
* <span data-ttu-id="0a711-1481">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="0a711-1481">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-1482">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-1482">Az.Storage</span></span>
* <span data-ttu-id="0a711-1483">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="0a711-1483">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="0a711-1484">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a711-1484">New-AzStorageContext</span></span>
* <span data-ttu-id="0a711-1485">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="0a711-1485">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="0a711-1486">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0a711-1486">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0a711-1487">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0a711-1487">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0a711-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0a711-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="0a711-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0a711-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="0a711-1490">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-1490">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="0a711-1491">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0a711-1491">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0a711-1492">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0a711-1492">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0a711-1493">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0a711-1493">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="0a711-1494">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0a711-1494">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="0a711-1495">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="0a711-1495">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a711-1496">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="0a711-1496">Highlights since the last major release</span></span>
* <span data-ttu-id="0a711-1497">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="0a711-1497">General availability of `Az` module</span></span>
* <span data-ttu-id="0a711-1498">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0a711-1498">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0a711-1499">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0a711-1499">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0a711-1500">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1500">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0a711-1501">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1501">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0a711-1502">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1502">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0a711-1503">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1503">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a711-1504">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a711-1504">Az.Automation</span></span>
* <span data-ttu-id="0a711-1505">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="0a711-1505">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="0a711-1506">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="0a711-1506">Dynamic grouping</span></span>
    * <span data-ttu-id="0a711-1507">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="0a711-1507">Pre-Post script</span></span>
    * <span data-ttu-id="0a711-1508">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="0a711-1508">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-1509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1509">Az.Compute</span></span>
* <span data-ttu-id="0a711-1510">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1510">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="0a711-1511">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="0a711-1511">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a711-1512">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a711-1512">Az.KeyVault</span></span>
* <span data-ttu-id="0a711-1513">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1513">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-1514">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-1514">Az.Network</span></span>
* <span data-ttu-id="0a711-1515">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1515">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="0a711-1516">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-1516">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-1517">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1517">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a711-1518">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="0a711-1518">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="0a711-1519">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1519">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-1520">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-1520">Az.Resources</span></span>
* <span data-ttu-id="0a711-1521">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1521">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="0a711-1522">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1522">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-1523">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-1523">Az.Sql</span></span>
* <span data-ttu-id="0a711-1524">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="0a711-1524">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-1525">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-1525">Az.Storage</span></span>
* <span data-ttu-id="0a711-1526">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="0a711-1526">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="0a711-1527">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0a711-1527">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0a711-1528">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0a711-1528">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0a711-1529">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0a711-1529">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0a711-1530">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="0a711-1530">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="0a711-1531">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="0a711-1531">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="0a711-1532">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="0a711-1532">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a711-1533">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-1533">Az.Websites</span></span>
* <span data-ttu-id="0a711-1534">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="0a711-1534">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="0a711-1535">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="0a711-1535">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a711-1536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-1536">Az.Accounts</span></span>
* <span data-ttu-id="0a711-1537">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="0a711-1537">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="0a711-1538">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1538">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a711-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a711-1539">Az.Automation</span></span>
* <span data-ttu-id="0a711-1540">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1540">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="0a711-1541">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="0a711-1541">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="0a711-1542">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="0a711-1542">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a711-1543">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a711-1543">Az.Cdn</span></span>
* <span data-ttu-id="0a711-1544">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="0a711-1544">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-1545">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1545">Az.Compute</span></span>
* <span data-ttu-id="0a711-1546">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1546">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a711-1547">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a711-1547">Az.DataFactory</span></span>
* <span data-ttu-id="0a711-1548">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="0a711-1548">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0a711-1549">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0a711-1549">Az.LogicApp</span></span>
* <span data-ttu-id="0a711-1550">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="0a711-1550">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-1551">Az.Network</span></span>
* <span data-ttu-id="0a711-1552">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1552">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-1553">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1553">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a711-1554">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="0a711-1554">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="0a711-1555">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="0a711-1555">SDK Update</span></span>
* <span data-ttu-id="0a711-1556">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="0a711-1556">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="0a711-1557">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1557">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-1558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-1558">Az.Resources</span></span>
* <span data-ttu-id="0a711-1559">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1559">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="0a711-1560">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="0a711-1560">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="0a711-1561">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="0a711-1561">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="0a711-1562">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="0a711-1562">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="0a711-1563">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="0a711-1563">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="0a711-1564">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="0a711-1564">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-1565">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-1565">Az.Sql</span></span>
* <span data-ttu-id="0a711-1566">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="0a711-1566">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="0a711-1567">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="0a711-1567">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-1568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-1568">Az.Storage</span></span>
* <span data-ttu-id="0a711-1569">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a711-1569">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="0a711-1570">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="0a711-1570">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="0a711-1571">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1571">Az.AnalysisServices</span></span>
* <span data-ttu-id="0a711-1572">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="0a711-1572">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a711-1573">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a711-1573">Az.Automation</span></span>
* <span data-ttu-id="0a711-1574">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1574">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="0a711-1575">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1575">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="0a711-1576">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1576">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a711-1577">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1577">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a711-1578">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-1578">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-1579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1579">Az.Compute</span></span>
* <span data-ttu-id="0a711-1580">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="0a711-1580">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="0a711-1581">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="0a711-1581">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="0a711-1582">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1582">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="0a711-1583">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="0a711-1583">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a711-1584">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a711-1584">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a711-1585">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="0a711-1585">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a711-1586">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a711-1586">Az.EventHub</span></span>
* <span data-ttu-id="0a711-1587">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="0a711-1587">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="0a711-1588">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a711-1588">Az.KeyVault</span></span>
* <span data-ttu-id="0a711-1589">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="0a711-1589">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0a711-1590">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0a711-1590">Az.LogicApp</span></span>
* <span data-ttu-id="0a711-1591">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="0a711-1591">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="0a711-1592">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="0a711-1592">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="0a711-1593">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="0a711-1593">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="0a711-1594">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0a711-1594">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0a711-1595">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0a711-1595">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0a711-1596">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0a711-1596">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0a711-1597">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0a711-1597">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="0a711-1598">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="0a711-1598">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="0a711-1599">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a711-1599">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0a711-1600">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a711-1600">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0a711-1601">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a711-1601">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0a711-1602">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a711-1602">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="0a711-1603">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="0a711-1603">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a711-1604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a711-1604">Az.Monitor</span></span>
* <span data-ttu-id="0a711-1605">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1605">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-1606">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-1606">Az.Network</span></span>
* <span data-ttu-id="0a711-1607">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="0a711-1607">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a711-1608">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a711-1608">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a711-1609">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-1609">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="0a711-1610">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="0a711-1610">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="0a711-1611">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="0a711-1611">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="0a711-1612">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-1612">Az.Resources</span></span>
* <span data-ttu-id="0a711-1613">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0a711-1613">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0a711-1614">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0a711-1614">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="0a711-1615">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="0a711-1615">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="0a711-1616">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="0a711-1616">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-1617">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-1617">Az.Sql</span></span>
* <span data-ttu-id="0a711-1618">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-1618">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="0a711-1619">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="0a711-1619">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a711-1620">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-1620">Az.Websites</span></span>
* <span data-ttu-id="0a711-1621">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="0a711-1621">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="0a711-1622">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="0a711-1622">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a711-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-1623">Az.Accounts</span></span>
* <span data-ttu-id="0a711-1624">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="0a711-1624">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0a711-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1625">Az.AnalysisServices</span></span>
<span data-ttu-id="0a711-1626">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="0a711-1626">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-1627">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1627">Az.Compute</span></span>
* <span data-ttu-id="0a711-1628">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="0a711-1628">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="0a711-1629">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="0a711-1629">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="0a711-1630">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="0a711-1630">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-1631">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1631">Az.RecoveryServices</span></span>
<span data-ttu-id="0a711-1632">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="0a711-1632">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-1633">Az.Resources</span></span>
* <span data-ttu-id="0a711-1634">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-1634">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="0a711-1635">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0a711-1635">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0a711-1636">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="0a711-1636">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="0a711-1637">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0a711-1637">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-1638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-1638">Az.Sql</span></span>
* <span data-ttu-id="0a711-1639">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-1639">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="0a711-1640">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="0a711-1640">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="0a711-1641">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="0a711-1641">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="0a711-1642">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="0a711-1642">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a711-1643">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-1643">Az.Accounts</span></span>
* <span data-ttu-id="0a711-1644">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="0a711-1644">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0a711-1645">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1645">Az.AnalysisServices</span></span>
* <span data-ttu-id="0a711-1646">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="0a711-1646">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-1647">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1647">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a711-1648">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="0a711-1648">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="0a711-1649">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="0a711-1649">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a711-1650">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-1650">Az.Accounts</span></span>
* <span data-ttu-id="0a711-1651">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1651">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0a711-1652">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="0a711-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0a711-1653">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="0a711-1653">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="0a711-1654">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0a711-1654">Az.Aks</span></span>
* <span data-ttu-id="0a711-1655">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="0a711-1655">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a711-1656">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a711-1656">Az.Automation</span></span>
* <span data-ttu-id="0a711-1657">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="0a711-1657">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="0a711-1658">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="0a711-1658">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a711-1659">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a711-1659">Az.Cdn</span></span>
* <span data-ttu-id="0a711-1660">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="0a711-1660">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1661">Az.Compute</span></span>
* <span data-ttu-id="0a711-1662">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="0a711-1662">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="0a711-1663">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-1663">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="0a711-1664">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-1664">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0a711-1665">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0a711-1665">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0a711-1666">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="0a711-1666">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a711-1667">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a711-1667">Az.DataFactory</span></span>
* <span data-ttu-id="0a711-1668">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="0a711-1668">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a711-1669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a711-1669">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a711-1670">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="0a711-1670">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="0a711-1671">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="0a711-1671">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="0a711-1672">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="0a711-1672">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a711-1673">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a711-1673">Az.IotHub</span></span>
* <span data-ttu-id="0a711-1674">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-1674">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a711-1675">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a711-1675">Az.KeyVault</span></span>
* <span data-ttu-id="0a711-1676">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="0a711-1676">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-1677">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-1677">Az.Network</span></span>
* <span data-ttu-id="0a711-1678">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="0a711-1678">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-1679">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-1679">Az.Resources</span></span>
* <span data-ttu-id="0a711-1680">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="0a711-1680">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="0a711-1681">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="0a711-1681">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="0a711-1682">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-1682">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="0a711-1683">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="0a711-1683">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="0a711-1684">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="0a711-1684">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="0a711-1685">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="0a711-1685">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="0a711-1686">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="0a711-1686">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a711-1687">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a711-1687">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a711-1688">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="0a711-1688">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="0a711-1689">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-1689">Fix some error messages.</span></span>
* <span data-ttu-id="0a711-1690">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="0a711-1690">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="0a711-1691">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="0a711-1691">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0a711-1692">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0a711-1692">Az.SignalR</span></span>
* <span data-ttu-id="0a711-1693">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="0a711-1693">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-1694">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-1694">Az.Sql</span></span>
* <span data-ttu-id="0a711-1695">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="0a711-1695">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0a711-1696">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="0a711-1696">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="0a711-1697">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="0a711-1697">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="0a711-1698">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="0a711-1698">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-1699">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-1699">Az.Storage</span></span>
* <span data-ttu-id="0a711-1700">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="0a711-1700">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0a711-1701">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="0a711-1701">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="0a711-1702">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="0a711-1702">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="0a711-1703">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0a711-1703">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="0a711-1704">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0a711-1704">Az.TrafficManager</span></span>
* <span data-ttu-id="0a711-1705">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="0a711-1705">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a711-1706">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-1706">Az.Websites</span></span>
* <span data-ttu-id="0a711-1707">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="0a711-1707">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0a711-1708">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="0a711-1708">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="0a711-1709">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="0a711-1709">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="0a711-1710">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="0a711-1710">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a711-1711">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-1711">Az.Accounts</span></span>
* <span data-ttu-id="0a711-1712">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1712">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-1713">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1713">Az.Compute</span></span>
* <span data-ttu-id="0a711-1714">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="0a711-1714">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="0a711-1715">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="0a711-1715">Updated the description of ID in help files</span></span>
* <span data-ttu-id="0a711-1716">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="0a711-1716">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a711-1717">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a711-1717">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a711-1718">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="0a711-1718">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="0a711-1719">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="0a711-1719">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0a711-1720">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0a711-1720">Az.EventGrid</span></span>
* <span data-ttu-id="0a711-1721">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="0a711-1721">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="0a711-1722">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="0a711-1722">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="0a711-1723">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="0a711-1723">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0a711-1724">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="0a711-1724">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0a711-1725">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="0a711-1725">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0a711-1726">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="0a711-1726">Dead letter endpoint.</span></span>
    - <span data-ttu-id="0a711-1727">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="0a711-1727">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0a711-1728">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="0a711-1728">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0a711-1729">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="0a711-1729">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0a711-1730">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="0a711-1730">Dead letter endpoint.</span></span>
* <span data-ttu-id="0a711-1731">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="0a711-1731">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="0a711-1732">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="0a711-1732">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a711-1733">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a711-1733">Az.IotHub</span></span>
* <span data-ttu-id="0a711-1734">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="0a711-1734">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0a711-1735">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0a711-1735">Az.LogicApp</span></span>
* <span data-ttu-id="0a711-1736">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="0a711-1736">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-1737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-1737">Az.Resources</span></span>
* <span data-ttu-id="0a711-1738">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="0a711-1738">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="0a711-1739">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="0a711-1739">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="0a711-1740">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="0a711-1740">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0a711-1741">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="0a711-1741">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="0a711-1742">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1742">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="0a711-1743">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="0a711-1743">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0a711-1744">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0a711-1744">Az.SignalR</span></span>
* <span data-ttu-id="0a711-1745">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="0a711-1745">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-1746">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-1746">Az.Sql</span></span>
* <span data-ttu-id="0a711-1747">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="0a711-1747">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a711-1748">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-1748">Az.Storage</span></span>
* <span data-ttu-id="0a711-1749">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="0a711-1749">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="0a711-1750">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a711-1750">New-AzStorageContext</span></span>
* <span data-ttu-id="0a711-1751">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="0a711-1751">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="0a711-1752">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0a711-1752">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a711-1753">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-1753">Az.Websites</span></span>
* <span data-ttu-id="0a711-1754">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="0a711-1754">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="0a711-1755">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="0a711-1755">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="0a711-1756">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="0a711-1756">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="0a711-1757">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="0a711-1757">General</span></span>

- <span data-ttu-id="0a711-1758">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="0a711-1758">General Availability of Az Module</span></span>
- <span data-ttu-id="0a711-1759">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1759">Online help for each module</span></span>
- <span data-ttu-id="0a711-1760">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="0a711-1760">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="0a711-1761">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0a711-1761">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="0a711-1762">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-1762">Az.Accounts</span></span>
- <span data-ttu-id="0a711-1763">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="0a711-1763">Changed from Az.Profile</span></span>
- <span data-ttu-id="0a711-1764">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1764">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0a711-1765">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a711-1765">Az.ApiManagement</span></span>
- <span data-ttu-id="0a711-1766">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="0a711-1766">Fixes for #7002</span></span>
- <span data-ttu-id="0a711-1767">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0a711-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="0a711-1768">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a711-1768">Az.Batch</span></span>
- <span data-ttu-id="0a711-1769">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="0a711-1769">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="0a711-1770">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="0a711-1770">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="0a711-1771">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0a711-1771">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="0a711-1772">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0a711-1772">Az.Billing</span></span>
- <span data-ttu-id="0a711-1773">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="0a711-1773">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="0a711-1774">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1774">Az.CognitivServices</span></span>
- <span data-ttu-id="0a711-1775">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="0a711-1775">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="0a711-1776">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="0a711-1776">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0a711-1777">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0a711-1777">Az.ContainerInstance</span></span>
- <span data-ttu-id="0a711-1778">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="0a711-1778">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="0a711-1779">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0a711-1779">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="0a711-1780">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0a711-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0a711-1781">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a711-1781">Az.DataLakeStore</span></span>
- <span data-ttu-id="0a711-1782">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0a711-1782">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="0a711-1783">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a711-1783">Az.Monitor</span></span>
- <span data-ttu-id="0a711-1784">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0a711-1784">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="0a711-1785">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a711-1785">Az.KeyVault</span></span>
- <span data-ttu-id="0a711-1786">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-1786">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="0a711-1787">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0a711-1787">Az.MachineLearning</span></span>
- <span data-ttu-id="0a711-1788">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="0a711-1788">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="0a711-1789">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0a711-1789">Az.Media</span></span>
- <span data-ttu-id="0a711-1790">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="0a711-1790">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0a711-1791">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-1791">Az.Network</span></span>
<span data-ttu-id="0a711-1792">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="0a711-1792">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="0a711-1793">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="0a711-1793">New cmdlets added:</span></span>
        - <span data-ttu-id="0a711-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a711-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0a711-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a711-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0a711-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a711-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0a711-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a711-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0a711-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a711-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0a711-1799">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0a711-1799">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="0a711-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0a711-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="0a711-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a711-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="0a711-1802">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a711-1802">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="0a711-1803">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a711-1803">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="0a711-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0a711-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0a711-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0a711-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0a711-1806">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-1806">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="0a711-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="0a711-1808">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="0a711-1808">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="0a711-1809">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0a711-1809">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="0a711-1810">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0a711-1810">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0a711-1811">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0a711-1811">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0a711-1812">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0a711-1812">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="0a711-1813">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="0a711-1813">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="0a711-1814">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0a711-1814">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="0a711-1815">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a711-1815">Az.OperationalInsights</span></span>
- <span data-ttu-id="0a711-1816">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0a711-1816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="0a711-1817">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0a711-1817">Az.Profile</span></span>
- <span data-ttu-id="0a711-1818">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a711-1818">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-1819">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1819">Az.RecoveryServices</span></span>
- <span data-ttu-id="0a711-1820">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0a711-1820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="0a711-1821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-1821">Az.Resources</span></span>
- <span data-ttu-id="0a711-1822">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0a711-1822">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0a711-1823">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a711-1823">Az.ServiceFabric</span></span>
- <span data-ttu-id="0a711-1824">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="0a711-1824">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="0a711-1825">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0a711-1825">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="0a711-1826">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0a711-1826">Az.SIgnalR</span></span>
- <span data-ttu-id="0a711-1827">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="0a711-1827">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="0a711-1828">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-1828">Az.Sql</span></span>
- <span data-ttu-id="0a711-1829">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1829">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="0a711-1830">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="0a711-1830">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="0a711-1831">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0a711-1831">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="0a711-1832">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-1832">Az.Storage</span></span>
- <span data-ttu-id="0a711-1833">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0a711-1833">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0a711-1834">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-1834">Az.Websites</span></span>
- <span data-ttu-id="0a711-1835">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="0a711-1835">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="0a711-1836">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="0a711-1836">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="0a711-1837">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="0a711-1837">General</span></span>

* <span data-ttu-id="0a711-1838">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-1838">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="0a711-1839">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1839">Az.Compute</span></span>

* <span data-ttu-id="0a711-1840">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="0a711-1840">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0a711-1841">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a711-1841">Az.DataLakeStore</span></span>

* <span data-ttu-id="0a711-1842">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="0a711-1842">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="0a711-1843">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a711-1843">Az.FrontDoor</span></span>

* <span data-ttu-id="0a711-1844">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="0a711-1844">Fixed some broken links</span></span>
    - <span data-ttu-id="0a711-1845">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="0a711-1845">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="0a711-1846">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="0a711-1846">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0a711-1847">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1847">Az.RecoveryServices</span></span>

* <span data-ttu-id="0a711-1848">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="0a711-1848">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="0a711-1849">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="0a711-1849">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="0a711-1850">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-1850">Az.Resources</span></span>

* <span data-ttu-id="0a711-1851">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="0a711-1851">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="0a711-1852">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="0a711-1852">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="0a711-1853">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-1853">Az.Sql</span></span>

* <span data-ttu-id="0a711-1854">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="0a711-1854">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="0a711-1855">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="0a711-1855">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="0a711-1856">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="0a711-1856">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="0a711-1857">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-1857">Az.Storage</span></span>

* <span data-ttu-id="0a711-1858">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-1858">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="0a711-1859">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="0a711-1859">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="0a711-1860">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0a711-1860">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0a711-1861">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="0a711-1861">Support Static Website configuration</span></span>
    - <span data-ttu-id="0a711-1862">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0a711-1862">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="0a711-1863">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0a711-1863">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0a711-1864">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-1864">Az.Websites</span></span>

* <span data-ttu-id="0a711-1865">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0a711-1865">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="0a711-1866">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="0a711-1866">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="0a711-1867">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="0a711-1867">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="0a711-1868">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="0a711-1868">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0a711-1869">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a711-1869">Az.ApiManagement</span></span>
* <span data-ttu-id="0a711-1870">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="0a711-1870">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="0a711-1871">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a711-1871">Az.Automation</span></span>
* <span data-ttu-id="0a711-1872">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="0a711-1872">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="0a711-1873">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="0a711-1873">Added Update Management cmdlets</span></span>
* <span data-ttu-id="0a711-1874">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="0a711-1874">Added Source Control cmdlets</span></span>
* <span data-ttu-id="0a711-1875">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="0a711-1875">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="0a711-1876">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="0a711-1876">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="0a711-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1877">Az.Compute</span></span>
* <span data-ttu-id="0a711-1878">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="0a711-1878">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="0a711-1879">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="0a711-1879">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0a711-1880">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0a711-1880">Az.ContainerInstance</span></span>
* <span data-ttu-id="0a711-1881">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="0a711-1881">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="0a711-1882">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0a711-1882">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0a711-1883">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="0a711-1883">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0a711-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-1884">Az.Network</span></span>
* <span data-ttu-id="0a711-1885">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="0a711-1885">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="0a711-1886">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="0a711-1886">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="0a711-1887">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="0a711-1887">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="0a711-1888">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="0a711-1888">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="0a711-1889">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0a711-1889">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0a711-1890">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="0a711-1890">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="0a711-1891">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="0a711-1891">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="0a711-1892">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0a711-1892">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="0a711-1893">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="0a711-1893">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="0a711-1894">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="0a711-1894">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="0a711-1895">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0a711-1895">Az.Relay</span></span>
* <span data-ttu-id="0a711-1896">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1896">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="0a711-1897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-1897">Az.Resources</span></span>
* <span data-ttu-id="0a711-1898">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="0a711-1898">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="0a711-1899">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="0a711-1899">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="0a711-1900">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="0a711-1900">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0a711-1901">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a711-1901">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a711-1902">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-1902">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="0a711-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-1903">Az.Sql</span></span>
* <span data-ttu-id="0a711-1904">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="0a711-1904">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="0a711-1905">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0a711-1905">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0a711-1906">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0a711-1906">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0a711-1907">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0a711-1907">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0a711-1908">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0a711-1908">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0a711-1909">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0a711-1909">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0a711-1910">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0a711-1910">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0a711-1911">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0a711-1911">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0a711-1912">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0a711-1912">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="0a711-1913">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="0a711-1913">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="0a711-1914">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="0a711-1914">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="0a711-1915">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="0a711-1915">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="0a711-1916">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0a711-1916">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0a711-1917">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0a711-1917">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0a711-1918">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0a711-1918">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="0a711-1919">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0a711-1919">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="0a711-1920">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="0a711-1920">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="0a711-1921">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="0a711-1921">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0a711-1922">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="0a711-1922">General</span></span>
* <span data-ttu-id="0a711-1923">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="0a711-1923">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="0a711-1924">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0a711-1924">Az.Profile</span></span>
* <span data-ttu-id="0a711-1925">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="0a711-1925">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="0a711-1926">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="0a711-1926">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="0a711-1927">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="0a711-1927">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="0a711-1928">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="0a711-1928">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="0a711-1929">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="0a711-1929">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="0a711-1930">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="0a711-1930">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="0a711-1931">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="0a711-1931">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a711-1932">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1932">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a711-1933">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="0a711-1933">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-1934">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1934">Az.Compute</span></span>
* <span data-ttu-id="0a711-1935">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="0a711-1935">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="0a711-1936">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="0a711-1936">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="0a711-1937">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="0a711-1937">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a711-1938">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a711-1938">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a711-1939">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="0a711-1939">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="0a711-1940">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="0a711-1940">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="0a711-1941">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="0a711-1941">Az.Insights</span></span>
* <span data-ttu-id="0a711-1942">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="0a711-1942">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="0a711-1943">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="0a711-1943">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="0a711-1944">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="0a711-1944">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="0a711-1945">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="0a711-1945">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-1946">Az.Network</span></span>
* <span data-ttu-id="0a711-1947">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="0a711-1947">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="0a711-1948">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a711-1948">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="0a711-1949">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="0a711-1949">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="0a711-1950">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0a711-1950">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="0a711-1951">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="0a711-1951">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="0a711-1952">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a711-1952">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="0a711-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0a711-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a711-1954">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a711-1954">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a711-1955">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-1955">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-1956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-1956">Az.Resources</span></span>
* <span data-ttu-id="0a711-1957">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="0a711-1957">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="0a711-1958">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="0a711-1958">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a711-1959">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a711-1959">Az.ServiceBus</span></span>
* <span data-ttu-id="0a711-1960">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="0a711-1960">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a711-1961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a711-1961">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a711-1962">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="0a711-1962">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="0a711-1963">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="0a711-1963">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="0a711-1964">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="0a711-1964">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="0a711-1965">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="0a711-1965">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="0a711-1966">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="0a711-1966">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="0a711-1967">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="0a711-1967">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="0a711-1968">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0a711-1968">Az.Profile</span></span>
* <span data-ttu-id="0a711-1969">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="0a711-1969">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="0a711-1970">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="0a711-1970">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-1971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1971">Az.Compute</span></span>
* <span data-ttu-id="0a711-1972">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="0a711-1972">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="0a711-1973">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="0a711-1973">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a711-1974">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a711-1974">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a711-1975">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="0a711-1975">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="0a711-1976">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="0a711-1976">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="0a711-1977">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="0a711-1977">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0a711-1978">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="0a711-1978">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0a711-1979">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="0a711-1979">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-1980">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-1980">Az.Network</span></span>
* <span data-ttu-id="0a711-1981">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="0a711-1981">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="0a711-1982">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="0a711-1982">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-1983">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-1983">Az.Resources</span></span>
* <span data-ttu-id="0a711-1984">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="0a711-1984">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="0a711-1985">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="0a711-1985">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="0a711-1986">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="0a711-1986">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="0a711-1987">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0a711-1987">Azure.Storage</span></span>
* <span data-ttu-id="0a711-1988">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="0a711-1988">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="0a711-1989">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0a711-1989">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="0a711-1990">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0a711-1990">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0a711-1991">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="0a711-1991">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="0a711-1992">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="0a711-1992">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="0a711-1993">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a711-1993">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a711-1994">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="0a711-1994">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a711-1995">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a711-1995">Az.Compute</span></span>
* <span data-ttu-id="0a711-1996">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="0a711-1996">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="0a711-1997">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="0a711-1997">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="0a711-1998">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="0a711-1998">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="0a711-1999">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0a711-1999">Az.DataFactoryV2</span></span>
* <span data-ttu-id="0a711-2000">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="0a711-2000">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a711-2001">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a711-2001">Az.Network</span></span>
* <span data-ttu-id="0a711-2002">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="0a711-2002">Added NetworkProfile functionality.</span></span> <span data-ttu-id="0a711-2003">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="0a711-2003">new cmdlets added</span></span>
    - <span data-ttu-id="0a711-2004">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0a711-2004">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="0a711-2005">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0a711-2005">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="0a711-2006">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0a711-2006">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="0a711-2007">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0a711-2007">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="0a711-2008">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-2008">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="0a711-2009">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a711-2009">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="0a711-2010">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="0a711-2010">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="0a711-2011">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="0a711-2011">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="0a711-2012">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="0a711-2012">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0a711-2013">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0a711-2013">Az.RedisCache</span></span>
* <span data-ttu-id="0a711-2014">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="0a711-2014">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="0a711-2015">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="0a711-2015">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a711-2016">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a711-2016">Az.Resources</span></span>
* <span data-ttu-id="0a711-2017">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="0a711-2017">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0a711-2018">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="0a711-2018">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a711-2019">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a711-2019">Az.Sql</span></span>
* <span data-ttu-id="0a711-2020">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="0a711-2020">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a711-2021">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a711-2021">Az.Websites</span></span>
* <span data-ttu-id="0a711-2022">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="0a711-2022">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="0a711-2023">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="0a711-2023">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="0a711-2024">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="0a711-2024">0.2.0 - September 2018</span></span>
 <span data-ttu-id="0a711-2025">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="0a711-2025">Initial Release</span></span>
