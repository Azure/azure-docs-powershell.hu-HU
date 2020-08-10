---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 77cbbeb01f5c6fcbf0f61bfab3d3f63b74a53bc4
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566410"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="f5a7e-103">Az Azure PowerShell kibocsátási megjegyzései</span><span class="sxs-lookup"><span data-stu-id="f5a7e-103">Azure PowerShell release notes</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="f5a7e-104">4.5.0 – 2020. augusztus</span><span class="sxs-lookup"><span data-stu-id="f5a7e-104">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-105">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-106">„Connect-AzAccount” parancsmag frissítve a „MaxContextPopulation” paraméter elfogadására [#9865]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-106">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="f5a7e-107">A SubscriptionClient-verzió frissítve a 2019. 06. 01. verzióra és a bérlői tartományok megjelenítése [#9838]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-107">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="f5a7e-108">Az előfizetés támogatott otthoni bérlői és managedBy bérlői információi</span><span class="sxs-lookup"><span data-stu-id="f5a7e-108">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="f5a7e-109">A modul neve és a verzió adatai javítva a telemetriai adatokban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-109">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="f5a7e-110">Korrigált SqlDatabaseDnsSuffix és ServiceManagementUrl, ha a környezeti metaadatok végpontja inkompatibilis értéket ad vissza</span><span class="sxs-lookup"><span data-stu-id="f5a7e-110">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5a7e-111">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5a7e-111">Az.Aks</span></span>
* <span data-ttu-id="f5a7e-112">A „ClientIdAndSecret” eltávolítva és lecserélve a ServicePrincipalIdAndSecret parancsmagra, és „ClientIdAndSecret” beállítva aliasként [#12381].</span><span class="sxs-lookup"><span data-stu-id="f5a7e-112">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="f5a7e-113">A „Get-AzAks”/„New-AzAks”/„Remove-AzAks”/„Set-AzAks” eltávolítva és lecserélve a „Get-AzAksCluster”/„New-AzAksCluster”/„Remove-AzAksCluster”/„Set-AzAksCluster” parancsmagra, és az eredetiek beállítva aliasként [#12373].</span><span class="sxs-lookup"><span data-stu-id="f5a7e-113">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5a7e-114">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5a7e-114">Az.ApiManagement</span></span>
* <span data-ttu-id="f5a7e-115">Új 'Add-AzApiManagementApiToGateway' parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-115">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="f5a7e-116">Új „Get-AzApiManagementGateway” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-116">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f5a7e-117">Új „Get-AzApiManagementGatewayHostnameConfiguration” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-117">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="f5a7e-118">Új „Get-AzApiManagementGatewayKey” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-118">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="f5a7e-119">Új „New-AzApiManagementGateway” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-119">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f5a7e-120">Új „New-AzApiManagementGatewayHostnameConfiguration” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-120">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="f5a7e-121">Új „New-AzApiManagementResourceLocationObject” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-121">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="f5a7e-122">Új „Remove-AzApiManagementApiFromGateway” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-122">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="f5a7e-123">Új „Remove-AzApiManagementGateway” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-123">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f5a7e-124">Új „Remove-AzApiManagementGatewayHostnameConfiguration” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-124">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="f5a7e-125">Új „Update-AzApiManagementGateway” parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-125">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f5a7e-126">Új választható [-GatewayId] paramétert hozzáadva a „Get-AzApiManagementApi” parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-126">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5a7e-127">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-127">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5a7e-128">A „Deny” utasítás kifejezetten a NetworkRules alapértelmezett műveleteként lett használva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-128">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5a7e-129">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-129">Az.FrontDoor</span></span>
* <span data-ttu-id="f5a7e-130">Kijavítottunk egy hibát, ahol kivétel történt, amikor az Enum.Parse null értéket próbált kényszeríteni egy engedélyezett vagy letiltott enumerálási értékre [#12344]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-130">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5a7e-131">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5a7e-131">Az.HDInsight</span></span>
* <span data-ttu-id="f5a7e-132">Támogatott a fürtlétrehozás az átvitel közbeni titkosítási funkcióval.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-132">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="f5a7e-133">Új „EncryptionInTransit” paraméter hozzáadva a „New-AzHDInsightCluster” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-133">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="f5a7e-134">Új „EncryptionInTransit” paraméter hozzáadva a „New-AzHDInsightClusterConfig” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-134">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="f5a7e-135">Támogatotta a fürtlétrehozás a privát kapcsolat funkcióval:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-135">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="f5a7e-136">Új „PublicNetworkAccessType” és az „OutboundPublicNetworkAccessType” paraméterek hozzáadva a „New-AzHDInsightCluster” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-136">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="f5a7e-137">Új „PublicNetworkAccessType” és az „OutboundPublicNetworkAccessType” paraméterek hozzáadva a „New-AzHDInsightClusterConfig” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-137">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="f5a7e-138">Virtuális hálózati adatok visszaadása a „New-AzHDInsightCluster” vagy a „Get-AzHDInsightCluster” meghívásakor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-138">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-139">Az.Network</span></span>
* <span data-ttu-id="f5a7e-140">Az AddressPrefixType paraméter mostantól támogatott a Remove-AzExpressRouteCircuitConnectionConfig esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-140">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="f5a7e-141">Hozzáadott nem kompatibilitástörő változások: PeerAddressType funkció a privát társviszony-létesítéshez a „Remove-AzExpressRouteCircutPeeringConfig” parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-141">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="f5a7e-142">A kód úgy lett módosítva, hogy figyelmen kívül hagyja az AddressPrefixType és a PeerAddressType paramétert.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-142">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="f5a7e-143">A „New-AzLoadBalancerFrontendIpConfig”, „New-AzPublicIpAddress” és „New-AzPublicIpPrefix” figyelmeztető üzenete módosult.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-143">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5a7e-144">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-144">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5a7e-145">A „-ForceDelete” kapcsoló hozzáadva a „Remove-AzOperationalInsightsworkspace” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-145">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="f5a7e-146">Új „Get-AzOperationalInsightsDeletedWorkspace” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-146">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="f5a7e-147">Új „Restore-AzOperationalInsightsWorkspace” parancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-147">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-148">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-149">Az Azure Backup tároló-/elemfelderítési funkciója továbbfejlesztve.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-149">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-150">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-151">A „Condition”, a „ConditionVersion” és a „Description” tulajdonság hozzáadva a „New-AzRoleAssignment” parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-151">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="f5a7e-152">Ebbe beletartozik az adatmodellek összes kapcsolódó változása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-152">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-153">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-154">Ki lett javítva a „New-AzSqlServer” és a „set-AzSqlServer” esetében a kiszolgálónevekben a kis- és nagybetűk meg nem különböztetését eredményező hiba</span><span class="sxs-lookup"><span data-stu-id="f5a7e-154">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="f5a7e-155">A „New-AzSqlDatabaseSecondary” parancsmagban egy meglévő adatbázishiba miatt helytelen adatbázisnevet visszaadó hiba javítva lett</span><span class="sxs-lookup"><span data-stu-id="f5a7e-155">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-156">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-157">A tároló/blob SAS-jogkivonat létrehozása támogatott az új x,t engedéllyel</span><span class="sxs-lookup"><span data-stu-id="f5a7e-157">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="f5a7e-158">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f5a7e-158">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="f5a7e-159">„New-AzStorageContainerSASToken”</span><span class="sxs-lookup"><span data-stu-id="f5a7e-159">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="f5a7e-160">A fiók SAS-jogkivonat létrehozása támogatott az új x,t,f engedéllyel</span><span class="sxs-lookup"><span data-stu-id="f5a7e-160">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="f5a7e-161">„New-AzStorageAccountSASToken”</span><span class="sxs-lookup"><span data-stu-id="f5a7e-161">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="f5a7e-162">Az egyetlen fájlmegosztás használatának lekérése támogatott</span><span class="sxs-lookup"><span data-stu-id="f5a7e-162">Supported get single file share usage</span></span>
    - <span data-ttu-id="f5a7e-163">„Get-AzRmStorageShare”</span><span class="sxs-lookup"><span data-stu-id="f5a7e-163">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="f5a7e-164">4.4.0 – 2020. július</span><span class="sxs-lookup"><span data-stu-id="f5a7e-164">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-165">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-165">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-166">Invoke-AzRestMethod új parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-166">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="f5a7e-167">Kijavítottunk egy olyan problémát, amely hitelesítési hibákat okozhat az olyan többfolyamatos forgatókönyvekben, mint például több Azure PowerShell parancsmag futtatása a Start-Job paranccsal [#9448]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-167">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5a7e-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5a7e-168">Az.Aks</span></span>
* <span data-ttu-id="f5a7e-169">Ki lett javítva az a hiba, amely miatt a Get-AzAks nem kér le minden fürtöt [#12296]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-169">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f5a7e-170">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-170">Az.AnalysisServices</span></span>
* <span data-ttu-id="f5a7e-171">A hitelesítés projekthivatkozása eltávolítva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-171">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5a7e-172">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-172">Az.Automation</span></span>
* <span data-ttu-id="f5a7e-173">Ki lett javítva az a hiba, amely miatt a feloldójeleket tartalmazó sztringek nem alakíthatók át JSON-objektummá.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-173">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-174">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-175">Figyelmeztetés jelenik meg a New-AzVmss a „latest” rendszerképverzió nélküli használatakor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-175">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-176">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-176">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-177">Globális paraméterek hozzáadva a Data Factoryhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-177">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f5a7e-178">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f5a7e-178">Az.EventGrid</span></span>
* <span data-ttu-id="f5a7e-179">Frissítve a 2020-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-179">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="f5a7e-180">Új funkciók hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-180">Added new features:</span></span>
    - <span data-ttu-id="f5a7e-181">Bemenetleképezés</span><span class="sxs-lookup"><span data-stu-id="f5a7e-181">Input mapping</span></span>
    - <span data-ttu-id="f5a7e-182">Eseménykézbesítési séma</span><span class="sxs-lookup"><span data-stu-id="f5a7e-182">Event Delivery Schema</span></span>
    - <span data-ttu-id="f5a7e-183">Privát kapcsolat</span><span class="sxs-lookup"><span data-stu-id="f5a7e-183">Private Link</span></span>
    - <span data-ttu-id="f5a7e-184">V10 felhő-eseményséma</span><span class="sxs-lookup"><span data-stu-id="f5a7e-184">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="f5a7e-185">Service Bus-témakör célértékként</span><span class="sxs-lookup"><span data-stu-id="f5a7e-185">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="f5a7e-186">Azure-függvény célértékként</span><span class="sxs-lookup"><span data-stu-id="f5a7e-186">Azure Function As Destination</span></span>
    - <span data-ttu-id="f5a7e-187">Webhookkötegelés</span><span class="sxs-lookup"><span data-stu-id="f5a7e-187">WebHook Batching</span></span>
    - <span data-ttu-id="f5a7e-188">Biztonságos webhook (AAD-támogatás)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-188">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="f5a7e-189">IP-szűrés</span><span class="sxs-lookup"><span data-stu-id="f5a7e-189">IpFiltering</span></span>
* <span data-ttu-id="f5a7e-190">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-190">Updated cmdlets:</span></span>
    - <span data-ttu-id="f5a7e-191">New-AzEventGridSubscription/Update-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-191">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="f5a7e-192">Új választható paraméterek lettek hozzáadva a webhookkötegelés támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-192">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="f5a7e-193">Új választható paraméterek lettek hozzáadva a biztonságos webhook AAD-vel való használatának támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-193">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="f5a7e-194">Új felsorolási érték lett hozzáadva az EndpointType paraméterhez az Azure-függvény és a Service Bus-témakör új célértékként való támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-194">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="f5a7e-195">Új választható paraméter lett hozzáadva a kézbesítési sémához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-195">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="f5a7e-196">New-AzEventGridTopic/Update-AzEventGridTopic és New-AzEventGridDomain/Update-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-196">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="f5a7e-197">Új választható paraméterek lettek hozzáadva az IP-szűrés támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-197">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="f5a7e-198">New-AzEventGridTopic/New-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-198">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="f5a7e-199">Új választható paraméterek lettek hozzáadva a bemenetleképezés támogatásáért.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-199">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5a7e-200">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-200">Az.FrontDoor</span></span>
* <span data-ttu-id="f5a7e-201">Modul frissítve a 2020-05-01-es API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="f5a7e-201">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="f5a7e-202">Privátkapcsolat-támogatás hozzáadva a Storage-, KeyVault- és Web App Service-erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-202">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5a7e-203">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5a7e-203">Az.HDInsight</span></span>
* <span data-ttu-id="f5a7e-204">ADLSGen1/2-tárolóval rendelkező fürt országos felhőkben való létrehozásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-204">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5a7e-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-205">Az.Monitor</span></span>
* <span data-ttu-id="f5a7e-206">Ki lett javítva a Get-AzDiagnosticSetting hibája, amely miatt a metrikák vagy naplók null értékűek [#12272]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-206">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-207">Az.Network</span></span>
* <span data-ttu-id="f5a7e-208">A paraméterek felcserélése ki lett javítva a VWan–HubVnet kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-208">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="f5a7e-209">Új parancsmagok lettek hozzáadva az Azure hálózati virtuális berendezések helyéhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-209">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="f5a7e-210">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="f5a7e-210">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f5a7e-211">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="f5a7e-211">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f5a7e-212">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="f5a7e-212">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f5a7e-213">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="f5a7e-213">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f5a7e-214">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="f5a7e-214">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="f5a7e-215">Új parancsmagok lettek hozzáadva az Azure hálózati virtuális berendezésekhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-215">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="f5a7e-216">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="f5a7e-216">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f5a7e-217">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="f5a7e-217">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f5a7e-218">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="f5a7e-218">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f5a7e-219">Update-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="f5a7e-219">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f5a7e-220">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="f5a7e-220">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="f5a7e-221">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="f5a7e-221">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="f5a7e-222">Application Gateway előkészítve a Private Link gyakori parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-222">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="f5a7e-223">StorageSync előkészítve a Private Link gyakori parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-223">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="f5a7e-224">SignalR előkészítve a Private Link gyakori parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-224">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-226">A hitelesítés projekthivatkozása eltávolítva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-226">Removed project reference to Authentication</span></span>
* <span data-ttu-id="f5a7e-227">Azure Backup-parancsmagok finomhangolása a pontosabb szövegért.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-227">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="f5a7e-228">Az Azure Backup mostantól támogatott az MAB-ügynökfeladatok beolvasásához a Get-AzRecoveryServicesBackupJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-228">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-229">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-229">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-230">A Save-AzResourceGroupDeploymentTemplate frissítése az SDK használatához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-230">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="f5a7e-231">Unregister-AzResourceProvider parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-231">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-232">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-232">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-233">Szolgáltatásnév és vendégfelhasználók támogatása hozzáadva a Set-AzSqlInstanceActiveDirectoryAdministrator parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-233">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="f5a7e-234">Ki lett javítva egy hiba az adatbesorolási parancsmagokban.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-234">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="f5a7e-235">A felügyelt Azure SQL-példány feladatátvétele mostantól támogatott: Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="f5a7e-235">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-236">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-236">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-237">Ki lett javítva az a probléma, amely miatt a UserAgent nem adható hozzá egyes adatsíkparancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-237">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="f5a7e-238">Storage-fiók létrehozásának/frissítésének támogatása a MinimumTlsVersion és az AllowBlobPublicAccess használatával</span><span class="sxs-lookup"><span data-stu-id="f5a7e-238">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="f5a7e-239">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-239">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="f5a7e-240">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-240">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f5a7e-241">A Storage-fiókok Blob service-beli verziószámozása engedélyezésének/letiltásának támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-241">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="f5a7e-242">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f5a7e-242">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="f5a7e-243">Blobok blobverziókkal való listázásának támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-243">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="f5a7e-244">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f5a7e-244">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="f5a7e-245">Egyetlen blobpillanatkép vagy blobverzió lekérésének/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-245">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="f5a7e-246">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f5a7e-246">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="f5a7e-247">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f5a7e-247">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="f5a7e-248">Az Azure.Storage.Blobs 12-es verziójában létrehozott blobobjektum folyamatának támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-248">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="f5a7e-249">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f5a7e-249">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="f5a7e-250">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f5a7e-250">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="f5a7e-251">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f5a7e-251">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="f5a7e-252">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f5a7e-252">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="f5a7e-253">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-253">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f5a7e-254">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f5a7e-254">Az.StorageSync</span></span>
* <span data-ttu-id="f5a7e-255">A 2020-03-01-es API-verziót célzó StorageSync SDK új verziója hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-255">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="f5a7e-256">Tárolószinkronizálási szolgáltatás frissítési parancsmagja hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-256">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="f5a7e-257">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f5a7e-257">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="f5a7e-258">IncomingTrafficPolicy és PrivateEndpointConnections hozzáadva a StorageSyncService parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-258">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-259">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-259">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-260">Támogatás hozzáadva az olyan Pontok műveleteinek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-260">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="f5a7e-261">4.3.0 – 2020. június</span><span class="sxs-lookup"><span data-stu-id="f5a7e-261">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-262">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-262">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-263">A környezetfelderítés beállítása és a környezet hozzáadása az Add-AzEnvironment használatával alapértelmezés szerint támogatott</span><span class="sxs-lookup"><span data-stu-id="f5a7e-263">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="f5a7e-264">Előre betöltött szerelvények frissítése [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-264">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="f5a7e-265">Az Azure.Core szerelvény frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-265">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="f5a7e-266">Ki lett javítva egy probléma, amely a Connect-AzAccount meghiúsulását okozhatta többszálas végrehajtás esetében [#11201]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-266">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5a7e-267">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5a7e-267">Az.Aks</span></span>
* <span data-ttu-id="f5a7e-268">A régi [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) használata helyébe a [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) és a [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API-k meghívása lépett</span><span class="sxs-lookup"><span data-stu-id="f5a7e-268">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f5a7e-269">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5a7e-269">Az.Batch</span></span>
* <span data-ttu-id="f5a7e-270">Frissítve lett az Az.Batch a Microsoft.Azure.Management.Batch SDK 11.0.0-s verziójának használatára</span><span class="sxs-lookup"><span data-stu-id="f5a7e-270">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="f5a7e-271">Hozzá lett adva a BatchAccount identitás beállításának lehetősége a New-AzBatchAccount parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-271">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5a7e-272">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-272">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5a7e-273">A fiók képességeinek megjelenítése támogatott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-273">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="f5a7e-274">Támogatott a PublicNetworkAccess paraméter módosítása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-274">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-275">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-276">A SimulateEviction paraméter hozzá lett adva a Set-AzVm és a Set-AzVmssVM parancsmagokhoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-276">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="f5a7e-277">A Premium_LRS hozzá lett adva a StorageAccountType paraméter argumentumbefejezőjéhez a New-AzGalleryImageVersion parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-277">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="f5a7e-278">Alállapotok lettek hozzáadva a VMCustomScriptExtension bővítményhez [#11297]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-278">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="f5a7e-279">A Törlés lehetőség hozzá lett adva az EvictionPolicy paraméter argumentumbefejezőjéhez a New-AzVM és a New-AzVMConfig parancsmagokban.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-279">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="f5a7e-280">Az új virtuálisgép-bővítmény neve ki lett javítva az SAP esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-280">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-281">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-281">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-282">Az ADF .Net SDK a 4.9.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-282">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5a7e-283">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-283">Az.EventHub</span></span>
* <span data-ttu-id="f5a7e-284">Managed Identity-paraméterek lettek hozzáadva a New-AzEventHubNamespace és a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-284">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="f5a7e-285">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f5a7e-285">Az.Functions</span></span>
* <span data-ttu-id="f5a7e-286">A PowerShell 7.0- és a Java 11-függvényalkalmazások létrehozása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="f5a7e-286">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5a7e-287">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5a7e-287">Az.HDInsight</span></span>
* <span data-ttu-id="f5a7e-288">Támogatott a gazdagépek listázása és a HDInsight-fürt adott gazdagépeinek újraindítása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-288">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f5a7e-289">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f5a7e-289">Az.HealthcareApis</span></span>
* <span data-ttu-id="f5a7e-290">Az SDK a 1.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-290">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="f5a7e-291">Az exportálási beállítások és a Managed Identity mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="f5a7e-291">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5a7e-292">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-292">Az.Monitor</span></span>
* <span data-ttu-id="f5a7e-293">Ki lett javítva a bemeneti objektumparaméter a Set-AzActivityLogAlert parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-293">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="f5a7e-294">Ki lett javítva az InputObject paraméter a Set-AzActionGroup parancsmag esetében [#10868]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-294">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-295">Az.Network</span></span>
* <span data-ttu-id="f5a7e-296">Az AddressPrefixType paraméter mostantól támogatott a Remove-AzExpressRouteCircuitConnectionConfig esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-296">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="f5a7e-297">Új parancsmagok lettek hozzáadva az Azure FirewallPolicy szabályzathoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-297">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="f5a7e-298">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="f5a7e-298">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="f5a7e-299">A tűzfalszabályzathoz tartozó hálózati szabályok céltartományneveinek támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-299">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="f5a7e-300">A háttércímkészlet műveletei mostantól támogatottak</span><span class="sxs-lookup"><span data-stu-id="f5a7e-300">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="f5a7e-301">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-301">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="f5a7e-302">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f5a7e-302">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="f5a7e-303">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f5a7e-303">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="f5a7e-304">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f5a7e-304">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="f5a7e-305">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f5a7e-305">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="f5a7e-306">A New-AzIpGroup névérvényesítése hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-306">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="f5a7e-307">Új parancsmagok lettek hozzáadva az Azure FirewallPolicy szabályzathoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-307">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="f5a7e-308">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="f5a7e-308">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="f5a7e-309">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni DNS-kiszolgálók beállítása/eltávolítása a VirtualWan-P2SVpnGateway átjárón.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-309">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="f5a7e-310">Frissült a New-AzP2sVpnGateway: A -CustomDnsServer opcionális paraméter hozzá lett adva az ügyfelek számára, hogy megadhassák a P2SVpnGateway átjárón beállítani kívánt DNS-kiszolgálókat (ezeket pont–hely ügyfelek is használhatják).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-310">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="f5a7e-311">Frissült az AzP2sVpnGateway: A -CustomDnsServer opcionális paraméter hozzá lett adva az ügyfelek számára, hogy megadhassák a P2SVpnGateway átjárón beállítani kívánt DNS-kiszolgálókat (ezeket pont–hely ügyfelek is használhatják).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-311">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="f5a7e-312">Frissült az Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f5a7e-312">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="f5a7e-313">A -BgpPeeringAddress opcionális paraméter hozzá lett adva az ügyfelek számára a VPN Gateway átjárón beállítani kívánt egyéni bgps megadásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-313">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="f5a7e-314">Új parancsmag lett hozzáadva a VirtualHub-erőforrás útválasztási állapota visszaállításának támogatásához:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-314">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="f5a7e-315">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="f5a7e-315">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="f5a7e-316">A tűzfalszabályzat legutóbbi Swagger-módosításának megfelelően frissültek az alábbi tételek</span><span class="sxs-lookup"><span data-stu-id="f5a7e-316">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="f5a7e-317">A RuleGroup, a RuleCollectionGroup és a RuleType neve megváltozott</span><span class="sxs-lookup"><span data-stu-id="f5a7e-317">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="f5a7e-318">Mostantól támogatott a tűzfalszabályzat NAT-szabálygyűjteménye esetében több NAT-szabálygyűjtemény használata</span><span class="sxs-lookup"><span data-stu-id="f5a7e-318">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="f5a7e-319">[Kompatibilitástörő változás] Kötelező SourceIpGroup paraméter lett hozzáadva a New-AzFirewallPolicyApplicationRule és a New-AzFirewallPolicyNetworkRule esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-319">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="f5a7e-320">[Kompatibilitástörő változás] A New-AzFirewallPolicyApplicationRule ki lett javítva, a SourceAddress paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-320">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="f5a7e-321">[Kompatibilitástörő változás] A New-AzFirewallPolicyApplicationRule ki lett javítva, a SourceAddress paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-321">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="f5a7e-322">[Kompatibilitástörő változás] Eltávolított kötelező paraméterek: TranslatedAddress, TranslatedPort a New-AzFirewallPolicyNatRuleCollection esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-322">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="f5a7e-323">Új parancsmagok lettek hozzáadva a PrivateLink támogatásához az Application Gatewayen</span><span class="sxs-lookup"><span data-stu-id="f5a7e-323">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="f5a7e-324">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-324">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f5a7e-325">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-325">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f5a7e-326">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-326">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f5a7e-327">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-327">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f5a7e-328">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-328">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f5a7e-329">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-329">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="f5a7e-330">Új parancsmagok lettek hozzáadva a VirtualHub HubRouteTables gyermekerőforrásai esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-330">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="f5a7e-331">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-331">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="f5a7e-332">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5a7e-332">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="f5a7e-333">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5a7e-333">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="f5a7e-334">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5a7e-334">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="f5a7e-335">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5a7e-335">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="f5a7e-336">Frissültek a meglévő parancsmagok az opcionális RoutingConfiguration bemeneti paraméter támogatásához az egyéni útválasztás esetében a VirtualWanban.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-336">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="f5a7e-337">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-337">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="f5a7e-338">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-338">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="f5a7e-339">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-339">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f5a7e-340">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-340">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f5a7e-341">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-341">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="f5a7e-342">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-342">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="f5a7e-343">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f5a7e-343">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="f5a7e-344">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f5a7e-344">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5a7e-345">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-345">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5a7e-346">Ki lett javítva az a PSWorkspace-hiba, amely miatt meghiúsult az IOperationalInsightsWorkspace implementálása [#12135]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-346">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="f5a7e-347">A pergb2018 hozzá lett adva az SKU paraméter érvényes értékéhez a Set-AzOperationalInsightsWorkspace esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-347">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="f5a7e-348">A FunctionParameters alias hozzá lett adva a FunctionParameter paraméterhez a következők esetében:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-348">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="f5a7e-349">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="f5a7e-349">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="f5a7e-350">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="f5a7e-350">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-351">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-352">Az Azure Backup mostantól támogatott az MAB-elemek beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-352">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="f5a7e-353">Az Azure Site Recovery támogatja a StandardSSD_LRS lemeztípust</span><span class="sxs-lookup"><span data-stu-id="f5a7e-353">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-354">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-355">A UsageLocation, GivenName, Surname, AccountEnabled, MailNickname, Mail paraméterek hozzá lettek adva a PSADUser esetében [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-355">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="f5a7e-356">Ki lett javítva az a hiba, hogy a -Mail nem működött a Get-AzADUser esetében [#11981]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-356">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="f5a7e-357">Az -ExcludeChangeType paraméter hozzá lett adva a következőkhöz: Get-AzDeploymentWhatIfResult és Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="f5a7e-357">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="f5a7e-358">A -WhatIfExcludeChangeType paraméter hozzá lett adva a következőkhöz: New-AzDeployment és New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f5a7e-358">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="f5a7e-359">A Test-Az\*Deployment parancsmagok frissültek a megfelelőbb hibaüzenetek megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-359">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="f5a7e-360">Ki lett javítva az üzemelő példány -Name paraméterének súgóüzenete a create és a What-If parancsmagok esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-360">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-361">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-361">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-362">Szolgáltatásnév támogatása hozzáadva a Set SQL Server Azure Active Directory Admin parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-362">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="f5a7e-363">Ki lett javítva a szinkronizálási probléma az adatbesorolási parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-363">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="f5a7e-364">Támogatott az e-mail-cím alapján történő felhasználókeresés a következő esetében: Set-AzSqlServerActiveDirectoryAdministrator [#12192]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-364">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-365">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-366">Támogatott a tárfiók RequireInfrastructureEncryption használatával való létrehozása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-366">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="f5a7e-367">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-367">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="f5a7e-368">Át lett helyezve az Azure.Core betöltési logikája Az.Accounts modulba</span><span class="sxs-lookup"><span data-stu-id="f5a7e-368">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-369">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-370">Hozzáadott védelem a létrehozott webalkalmazás törléséhez, ha a visszaállítás nem sikerült a Restore-AzDeletedWebApp esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-370">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f5a7e-371">A SourceWebApp.Location paraméter hozzá lett adva a New-AzWebApp és a New-AzWebAppSlot esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-371">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="f5a7e-372">Ki lett javítva az a hiba, amely megakadályozta a tárolóbeállítások módosítását a Set-AzWebApp és a Set-AzWebAppSlot esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-372">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="f5a7e-373">Ki lett javítva a SiteConfig lekérésének hibája, ha a -Name nem lett megadva a Get-AzWebApp esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-373">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="f5a7e-374">Támogatás hozzáadva ASP létráhozásához Linux-alkalmazások esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-374">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="f5a7e-375">Kivételek hozzáadva az erőforráscsoportok közötti klónozás esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-375">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="f5a7e-376">4.2.0 – 2020. június</span><span class="sxs-lookup"><span data-stu-id="f5a7e-376">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-377">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-378">Kijavítottunk egy problémát, amely miatt az Az Azure Automation-naplókat vagy PowerShell-feladatokat hagyott ki [#11492]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-378">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f5a7e-379">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-379">Az.AnalysisServices</span></span>
* <span data-ttu-id="f5a7e-380">Frissítettük az adatsík parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="f5a7e-380">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5a7e-381">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5a7e-381">Az.ApiManagement</span></span>
* <span data-ttu-id="f5a7e-382">Frissítettük a szolgáltatásfelügyeleti parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="f5a7e-382">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="f5a7e-383">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f5a7e-383">Az.Billing</span></span>
* <span data-ttu-id="f5a7e-384">Frissítettük a felhasználási parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="f5a7e-384">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5a7e-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5a7e-386">A PrivateEndpoint és a PublicNetworkAccess vezérlők támogatása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-386">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-387">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-387">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-388">Frissítettük a Data Factory V2 parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="f5a7e-388">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="f5a7e-389">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="f5a7e-389">Az.DataShare</span></span>
* <span data-ttu-id="f5a7e-390">Az Az.DataShare modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-390">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="f5a7e-391">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="f5a7e-391">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="f5a7e-392">Az „Az.DesktopVirtualization” modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-392">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5a7e-393">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-393">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5a7e-394">SDK frissítve a 0.21.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="f5a7e-394">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="f5a7e-395">Választható paraméterek hozzáadva a következőkhöz:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-395">Added optional parameters to</span></span> 
    - <span data-ttu-id="f5a7e-396">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="f5a7e-396">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="f5a7e-397">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="f5a7e-397">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5a7e-398">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-398">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5a7e-399">Javítottuk a Start-AzPolicyComplianceScan 3. példáját</span><span class="sxs-lookup"><span data-stu-id="f5a7e-399">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f5a7e-400">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f5a7e-400">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f5a7e-401">Frissítettük a PowerBI-parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="f5a7e-401">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="f5a7e-402">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="f5a7e-402">Az.PrivateDns</span></span>
* <span data-ttu-id="f5a7e-403">Javítottuk a Remove-AzPrivateDnsRecordSet kimeneti sztringjének formázását</span><span class="sxs-lookup"><span data-stu-id="f5a7e-403">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-404">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-404">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-405">Azure Site Recovery-támogatás helyreállítási terv létrehozásához az xml-bemenetből kezdeményezett, zónák közötti replikáció esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-405">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="f5a7e-406">Frissítettük a SiteRecovery és a Backup parancsmagok szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="f5a7e-406">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-407">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-408">Szélsőérték paraméter hozzáadva a Get-AzDeploymentScriptLog és a Save-AzDeploymentScriptLog parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-408">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="f5a7e-409">Kimeneti tulajdonság formázása és megjelenítése a Get-AzDeploymentScript parancsmag kimenetén</span><span class="sxs-lookup"><span data-stu-id="f5a7e-409">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="f5a7e-410">A -DeploymentScriptInputObject paraméter új neve -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="f5a7e-410">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="f5a7e-411">Javítottuk a parancsmagüzenetek hiányzó fájl-/célnevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-411">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="f5a7e-412">Frissítettük a Resource Manager és a címkék parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="f5a7e-412">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-413">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-413">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-414">UsePrivateLinkConnection hozzáadva a következőkhöz: New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember és Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f5a7e-414">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="f5a7e-415">SyncMemberAzureDatabaseResourceId hozzáadva a következőkhöz: New-AzSqlSyncMember és Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f5a7e-415">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="f5a7e-416">Vendégfelhasználó-keresés támogatása hozzáadva a Set SQL Server Azure Active Directory Admin parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-416">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-417">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-417">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-418">Frissítettük az adatsík parancsmagjainak szerelvényverzióját</span><span class="sxs-lookup"><span data-stu-id="f5a7e-418">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="f5a7e-419">4.1.0 – 2020. május</span><span class="sxs-lookup"><span data-stu-id="f5a7e-419">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="f5a7e-420">A legutóbbi kiadás óta bevezetett újdonságok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-420">Highlights since the last release</span></span>
* <span data-ttu-id="f5a7e-421">Támogatott PowerShell-verziók: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="f5a7e-421">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="f5a7e-422">Az Az.Functions általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-422">General availability of Az.Functions</span></span> 
* <span data-ttu-id="f5a7e-423">A következők rendelkeznek nagyobb kiadással: Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources és Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-423">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-424">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-424">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-425">Frissítve lett az Add-AzEnvironment és a Set-AzEnvironment parancsmag, amelyek mostantól elfogadják az AzureSynapseAnalyticsEndpointResourceId és az AzureSynapseAnalyticsEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="f5a7e-425">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="f5a7e-426">Hozzá lettek adva az Azure.Core-hoz kapcsolódó szerelvények az Az.Accounts-hoz, a támogatott platformok a Windows PowerShell 5.1, a PowerShell Core 6.2.4 és a PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="f5a7e-426">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5a7e-427">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5a7e-427">Az.Aks</span></span>
* <span data-ttu-id="f5a7e-428">Az API-verzió frissítve lett a 2019-10-01-es verzióra</span><span class="sxs-lookup"><span data-stu-id="f5a7e-428">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="f5a7e-429">Az AKS Windows-tárolókkal történő létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-429">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="f5a7e-430">Elérhető új parancsmagok: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool,        Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="f5a7e-430">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5a7e-431">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5a7e-431">Az.ApiManagement</span></span>
* <span data-ttu-id="f5a7e-432">New-AzApiManagement és Set-AzApiManagement: az [-AssignIdentity] paraméter új neve [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-432">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="f5a7e-433">New-AzApiManagement és Set-AzApiManagement: Új paraméter lett hozzáadva: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-433">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="f5a7e-434">A Get-AzApiManagementProperty át lett nevezve a következőre: Get-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-434">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f5a7e-435">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-435">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="f5a7e-436">A New-AzApiManagementProperty át lett nevezve a következőre: New-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-436">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f5a7e-437">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-437">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="f5a7e-438">A Set-AzApiManagementProperty át lett nevezve a következőre: Set-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-438">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f5a7e-439">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-439">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="f5a7e-440">A Remove-AzApiManagementProperty át lett nevezve a következőre: Remove-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-440">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f5a7e-441">A PropertyId paraméter át lett nevezve a következőre: NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-441">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="f5a7e-442">Hozzá lett adva az új Get-AzApiManagementAuthorizationServerClientSecret parancsmag, valamint a Get-AzApiManagementAuthorizationServer már nem ad vissza titkos ügyfélkulcsot.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-442">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="f5a7e-443">Hozzá lett adva az új Get-AzApiManagementNamedValueSecretValue parancsmag, és a Get-AzApiManagementNamedValue nem ad vissza titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-443">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="f5a7e-444">Hozzá lett adva az új Get-AzApiManagementOpenIdConnectProviderClientSecret parancsmag, valamint a Get-AzApiManagementOpenIdConnectProvider már nem ad vissza titkos ügyfélkulcsot.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-444">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="f5a7e-445">Hozzá lett adva az új Get-AzApiManagementSubscriptionKey parancsmag, és a Get-AzApiManagementSubscription már nem ad vissza előfizetési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-445">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="f5a7e-446">Hozzá lett adva az új Get-AzApiManagementTenantAccessSecret parancsmag, és a Get-AzApiManagementTenantAccess már nem ad vissza kulcsot.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-446">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="f5a7e-447">Hozzá lett adva az új Get-AzApiManagementTenantGitAccessSecret parancsmag, és a Get-AzApiManagementTenantGitAccess már nem ad vissza kulcsot.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-447">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="f5a7e-448">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-448">Az.ApplicationInsights</span></span>
* <span data-ttu-id="f5a7e-449">Hozzáadott paraméterek: A New-AzApplicationInsights esetében: RetentionInDays, PublicNetworkAccessForIngestion, PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="f5a7e-449">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="f5a7e-450">Létre lett hozva az Update-AzApplicationInsights parancsmag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-450">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="f5a7e-451">Parancsmagok lettek létrehozva a társított tárfiókhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-451">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f5a7e-452">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5a7e-452">Az.Batch</span></span>
* <span data-ttu-id="f5a7e-453">Frissítve lett az Az.Batch a Microsoft.Azure.Batch SDK 13.0.0.-s verziójának és a Microsoft.Azure.Management.Batch SDK 9.0.0-s verziójának használatára.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-453">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="f5a7e-454">Kiválaszthatóvá vált a hozzáadni kívánt tanúsítvány típusa a New-AzBatchCertificate új -CertificateKind paraméterének használatával.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-454">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="f5a7e-455">El lett távolítva az ApplicationPackages tulajdonság a PSApplicationből, amelynek típusa eddig mindig '' volt.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-455">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="f5a7e-456">Most már lekérhetők az alkalmazásokon belüli adott csomagok a Get-AzBatchApplicationPackage használatával.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-456">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="f5a7e-457">Például: Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-457">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="f5a7e-458">Egy készlet New-AzBatchPool használatával történő létrehozásakor a PSImageReference VirtualMachineImageId tulajdonsága már csak a Shared Image Gallery-ben található rendszerképre hivatkozhat.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-458">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="f5a7e-459">Egy készlet New-AzBatchPool használatával történő létrehozásakor a készlet nyilvános IP-cím nélkül is létrehozható a PSNetworkConfiguration új PublicIPAddressConfiguration tulajdonságával.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-459">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="f5a7e-460">A PSNetworkConfiguration PublicIPs tulajdonsága a PSPublicIPAddressConfiguration esetében is elérhető.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-460">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="f5a7e-461">Ez a tulajdonság csak akkor adható meg, ha az IPAddressProvisioningType UserManaged típusú.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-461">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-462">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-463">A HostId paraméter hozzá lett adva az Update-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-463">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="f5a7e-464">Frissültek a New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem és Set-AzVmssOsProfile parancsmagok súgódokumentumai.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-464">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="f5a7e-465">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="f5a7e-465">Breaking changes</span></span>
    - <span data-ttu-id="f5a7e-466">A FilterExpression paraméter el lett távolítva a Get-AzVMImage parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-466">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="f5a7e-467">Az AssignIdentity paraméter el lett távolítva a New-AzVmssConfig, New-AzVMConfig és Update-AzVM parancsmagokból.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-467">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="f5a7e-468">Az AutomaticRepairMaxInstanceRepairsPercent paraméter el lett távolítva a New-AzVmssConfig és az Update-AzVmss parancsmagokból.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-468">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="f5a7e-469">Az AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus és VirtualMachineScaleSetsColocationStatus tulajdonságok el lettek távolítva a ProximityPlacementGroup paraméterből.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-469">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="f5a7e-470">A MaxInstanceRepairsPercent tulajdonság el lett távolítva a következőből: AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-470">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="f5a7e-471">Az AvailabilitySets, VirtualMachines és VirtualMachineScaleSets típusa IList<SubResource> helyett mostantól IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-471">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="f5a7e-472">Frissült a Get-AzVM parancsmag leírása, hogy pontosabban ismertesse a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-472">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-473">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-473">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-474">Adatfolyam futtatókörnyezeti tulajdonságaihoz tartozó CRUD támogatása a felügyelt IR-ben.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-474">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5a7e-475">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-475">Az.FrontDoor</span></span>
* <span data-ttu-id="f5a7e-476">Új parancsmagok lettek hozzáadva a Front Door szabálymotor-objektumának létrehozására, frissítésére, lekérésére és törlésére.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-476">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="f5a7e-477">Hozzá lettek adva segítő parancsmagok a Front Door szabálymotor-objektumának létrehozásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-477">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="f5a7e-478">Hozzá lett adva a szabálymotor-referencia a Front Door útválasztásiszabály-objektumához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-478">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="f5a7e-479">Hozzá lettek adva privát kapcsolati paraméterek a Front Door háttérobjektumához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-479">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="f5a7e-480">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f5a7e-480">Az.Functions</span></span>
* <span data-ttu-id="f5a7e-481">Az Az.Functions modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-481">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5a7e-482">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5a7e-482">Az.HDInsight</span></span>
* <span data-ttu-id="f5a7e-483">Az ügyfél által felügyelt kulcson alapuló lemeztitkosítás mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-483">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f5a7e-484">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f5a7e-484">Az.HealthcareApis</span></span>
* <span data-ttu-id="f5a7e-485">A hozzáférési szabályzatok már nem tartoznak alapértelmezés szerint az aktuális rendszerbiztonsági taghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-485">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5a7e-486">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-486">Az.IotHub</span></span>
* <span data-ttu-id="f5a7e-487">Hozzá lett adva egy parancsmag, amellyel egy SQL-szerű nyelv használatával végzett, információkat lekérő lekérdezés indítható el az IoT Hubban.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-487">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="f5a7e-488">Javítva a hiba, amely miatt az Add-AzIotHubDevice gyermekeszköz nélkül nem tudott Edge-kompatibilis eszközt létrehozni [#11597]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-488">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="f5a7e-489">Hozzá lett adva egy parancsmag egy SAS-token létrehozásához az IoT Hub, eszköz vagy modul számára.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-489">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="f5a7e-490">Hozzá lett adva egy parancsmag a konfiguráció-metrikák lekérdezésének meghívásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-490">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="f5a7e-491">Az IoT Edge nagy léptékű automatikus üzembe helyezésének kezelése.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-491">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="f5a7e-492">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-492">New cmdlets are:</span></span>
    - <span data-ttu-id="f5a7e-493">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="f5a7e-493">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="f5a7e-494">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="f5a7e-494">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="f5a7e-495">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="f5a7e-495">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="f5a7e-496">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="f5a7e-496">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="f5a7e-497">Hozzá lett adva egy parancsmag, amellyel az IoT Edge üzembehelyezési metrikáit lekérő lekérdezést hívható meg.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-497">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="f5a7e-498">Hozzá lett adva egy parancsmag a konfiguráció tartalmának egy adott Edge-eszközre történő alkalmazásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-498">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5a7e-499">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5a7e-499">Az.KeyVault</span></span>
* <span data-ttu-id="f5a7e-500">A következő két alias el lett távolítva: New-AzKeyVaultCertificateAdministratorDetails és New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="f5a7e-500">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="f5a7e-501">Alapértelmezés szerint engedélyezve lett a helyreállítható törlés egy kulcstartó létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-501">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="f5a7e-502">Kulcstartó létrehozásakor a hálózati szabályok beállíthatók a megadott hálózati helyekről való hozzáférés szabályozására</span><span class="sxs-lookup"><span data-stu-id="f5a7e-502">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="f5a7e-503">A saját kulcs használata (BYOK) már támogatott</span><span class="sxs-lookup"><span data-stu-id="f5a7e-503">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="f5a7e-504">Az Add-AzKeyVaultKey támogatja a kulcscserekulcsok létrehozását</span><span class="sxs-lookup"><span data-stu-id="f5a7e-504">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="f5a7e-505">A Get-AzKeyVaultKey támogatja a nyilvános kulcsok PEM formátumban való letöltését</span><span class="sxs-lookup"><span data-stu-id="f5a7e-505">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="f5a7e-506">Frissült az Add-AzKeyVaultKey súgódokumentációjának KeyOps része</span><span class="sxs-lookup"><span data-stu-id="f5a7e-506">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5a7e-507">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-507">Az.Monitor</span></span>
* <span data-ttu-id="f5a7e-508">Javítva a Set-AzDiagnosticSettings hibája, amely miatt a megtartási szabályzat nem vonatkozott minden kategóriára [#11589]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-508">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="f5a7e-509">A WebTest rendelkezésre állási feltételeinek támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-509">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="f5a7e-510">New-AzMetricAlertRuleV2Criteria: mostantól megadhatók a webteszt rendelkezésre állási feltételei</span><span class="sxs-lookup"><span data-stu-id="f5a7e-510">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="f5a7e-511">Add-AzMetricAlertRuleV2: támogatja a webteszt új rendelkezésre állási feltételeit</span><span class="sxs-lookup"><span data-stu-id="f5a7e-511">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="f5a7e-512">El lett távolítva a RetentionPolicy redundáns definíciója a PSLogProfile-ból [#7608]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-512">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="f5a7e-513">El lettek távolítva a PSEventData objektumban meghatározott redundáns tulajdonságok [#11353]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-513">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="f5a7e-514">A Get-Azlog át lett nevezve a következőre: Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="f5a7e-514">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-515">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-515">Az.Network</span></span>
* <span data-ttu-id="f5a7e-516">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely figyelmeztet a Zone alapértelmezett viselkedésének változásáról</span><span class="sxs-lookup"><span data-stu-id="f5a7e-516">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="f5a7e-517">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f5a7e-517">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="f5a7e-518">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f5a7e-518">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="f5a7e-519">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-519">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="f5a7e-520">Hozzá lett adva az új, SecurityPartnerProvider legfelsőbb szintű erőforrás támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-520">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="f5a7e-521">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-521">New cmdlets added:</span></span>
        - <span data-ttu-id="f5a7e-522">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f5a7e-522">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="f5a7e-523">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f5a7e-523">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="f5a7e-524">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f5a7e-524">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="f5a7e-525">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f5a7e-525">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="f5a7e-526">Hozzá lett adva a RequiredZoneNames tulajdonság a PSPrivateLinkResource esetében, és a GroupId a PSPrivateEndpointConnection esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-526">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="f5a7e-527">Kijavítva a SuccessThresholdRoundTripTimeMs paraméter típusa a New-AzNetworkWatcherConnectionMonitorTestConfigurationObject esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-527">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="f5a7e-528">Frissítve lettek a VirtualWan parancsmagok az AllowVnetToVnetTraffic argumentum True értékre való állításához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-528">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="f5a7e-529">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f5a7e-529">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="f5a7e-530">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f5a7e-530">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="f5a7e-531">Új parancsmagok lettek hozzáadva a privát végpontok DNS-zónacsoportjainak támogatásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-531">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="f5a7e-532">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-532">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="f5a7e-533">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="f5a7e-533">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="f5a7e-534">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="f5a7e-534">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="f5a7e-535">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="f5a7e-535">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="f5a7e-536">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="f5a7e-536">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="f5a7e-537">Hozzá lett adva a DNSEnableProxy, a DNSRequireProxyForNetworkRules és a DNSServers paraméter az AzureFirewall-hoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-537">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="f5a7e-538">Hozzá lett adva az EnableDnsProxy, a DnsProxyNotRequiredForNetworkRule és a DnsServer paraméter az AzureFirewall-hoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-538">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="f5a7e-539">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-539">Updated cmdlet:</span></span>
        - <span data-ttu-id="f5a7e-540">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f5a7e-540">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5a7e-541">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-541">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5a7e-542">Frissítve lett a régi kód az újonnan létrehozott SDK alkalmazásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-542">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="f5a7e-543">Az elavult API-k miatt törölt parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-543">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="f5a7e-544">Get-AzOperationalInsightsSavedSearchResult (alias: Get-AzOperationalInsightsSavedSearchResults)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-544">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="f5a7e-545">Get-AzOperationalInsightsSearchResult (alias: Get-AzOperationalInsightsSearchResults)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-545">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="f5a7e-546">Get-AzOperationalInsightsLinkTarget (alias: Get-AzOperationalInsightsLinkTargets)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-546">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="f5a7e-547">Paraméterek lettek hozzáadva a Set-AzOperationalInsightsWorkspace és New-AzOperationalInsightsWorkspace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-547">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="f5a7e-548">Parancsmagok lettek létrehozva a társított tárfiókhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-548">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="f5a7e-549">Parancsmagok lettek létrehozva a fürtökhöz és a társított szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-549">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-551">Hozzá lett adva az Azure Site Recovery-támogatás a közelségi elhelyezési csoportokban lévő virtuális gépek védelme érdekében, az Azure–Azure szolgáltatók esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-551">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="f5a7e-552">Hozzá lett adva az Azure Site Recovery-támogatás a zónák közötti replikáció esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-552">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="f5a7e-553">Az Azure Backup már támogatja a hosszú távú megőrzést az Azure FileShare helyreállítási pontok esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-553">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="f5a7e-554">Hozzá lettek adva az Azure Backup lemezkizárási tulajdonságok a Get-AzRecoveryServicesBackupItem parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-554">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="f5a7e-555">Hozzá lett adva a privát végpont a Vault hitelesítési fájljaihoz a Site Recovery szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-555">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-556">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-557">Hozzá lett adva a megtekintés késéséről figyelmeztető üzenet az új szerepkör-definíció létrehozása során</span><span class="sxs-lookup"><span data-stu-id="f5a7e-557">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="f5a7e-558">Módosítva lettek a szabályzat-parancsmagok a szigorú típusmegadású objektumok megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-558">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="f5a7e-559">El lett távolítva a Get-AzResourceLock parancsmaghoz használt -TenantLevel paraméter [#11335]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-559">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="f5a7e-560">Javítva a Remove-AzResourceGroup -Id ResourceId parancsmag [#9882]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-560">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="f5a7e-561">Hozzá lett adva egy új parancsmag az ARM-sablon What-If típusú eredményeinek lekéréséhez az erőforráscsoport hatókörében: Get-AzDeploymentResourceGroupWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="f5a7e-561">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="f5a7e-562">Hozzá lett adva egy új parancsmag az ARM-sablonok What-If típusú eredményeinek lekéréséhez az előfizetés hatókörében: Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="f5a7e-562">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="f5a7e-563">Alias: Get-AzSubscriptionDeploymentWhatIf</span><span class="sxs-lookup"><span data-stu-id="f5a7e-563">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="f5a7e-564">A -WhatIf és a -Confirm paraméter felül lett írva a New-AzDeployment és a New-AzResourceGroupDeployment parancsmagok esetében az ARM-sablon What-If típusú eredményeinek használata érdekében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-564">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="f5a7e-565">Hozzá lett adva az elavulási üzenet az ApiVersion paraméterhez az üzembehelyezési parancsmagokban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-565">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="f5a7e-566">Hozzá lett adva egy képesség, amely lehetővé teszi, hogy fejlettebb hibaüzenetek jelenjenek meg az üzembehelyezési hibák esetén</span><span class="sxs-lookup"><span data-stu-id="f5a7e-566">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="f5a7e-567">Hozzá lett adva a correlationId-naplózása az üzembehelyezési hibák esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-567">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="f5a7e-568">Hozzá lett adva az error tulajdonság az üzembehelyezési szkript kimenetéhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-568">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="f5a7e-569">A Microsoft.Azure.Management.ResourceManager NuGet frissítve lett a 3.7.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="f5a7e-569">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="f5a7e-570">El lettek távolítva adott tesztesetek, mivel a DeploymentValidateResult Error tulajdonsága csak olvasható állapotúra változott a NuGet 3.7.1-preview verziójától kezdődően</span><span class="sxs-lookup"><span data-stu-id="f5a7e-570">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="f5a7e-571">A GenericResourceExpanded át lett hozva a ResourceManager SDK 3.7.1-preview verziójából</span><span class="sxs-lookup"><span data-stu-id="f5a7e-571">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="f5a7e-572">Hozzá lett adva a címketámogatás az összes, üzembe helyezéshez használt Get parancsmaghoz, valamint a következőkhöz:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-572">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="f5a7e-573">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f5a7e-573">'New-AzDeployment'</span></span>
    - <span data-ttu-id="f5a7e-574">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f5a7e-574">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="f5a7e-575">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f5a7e-575">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f5a7e-576">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f5a7e-576">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5a7e-577">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5a7e-577">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5a7e-578">Javítva a hiba, amely hibás tanúsítvány-ujjlenyomatot kért le a tanúsítvány --SecretIdentifier használatával történő hozzáadásakor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-578">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-579">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-580">Javult a következők teljesítménye:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-580">Enhance performance of:</span></span>
    - <span data-ttu-id="f5a7e-581">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="f5a7e-581">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f5a7e-582">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="f5a7e-582">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f5a7e-583">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="f5a7e-583">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f5a7e-584">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="f5a7e-584">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f5a7e-585">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-585">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="f5a7e-586">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-586">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="f5a7e-587">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-587">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="f5a7e-588">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-588">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="f5a7e-589">El lett távolítva a RetentionDays paraméter ügyféloldali érvényesítése a Set-AzSqlDatabaseBackupShortTermRetentionPolicy parancsmagból</span><span class="sxs-lookup"><span data-stu-id="f5a7e-589">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="f5a7e-590">A Vnet-ben található tárfiók naplózása, javítva a Storage Blob-adatok közreműködői szerepkörének létrehozásakor fellépő hiba.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-590">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-591">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-591">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-592">Hozzá lett adva az -AsJob a fiók Get-AzStorageAccount parancsmagjának lekéréséhez vagy listázásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-592">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="f5a7e-593">A KeyVersion választható lett a Storage-fiók KeyvaultEncryption használatával történő frissítésekor a kulcs automatikus rotálásának támogatásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-593">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="f5a7e-594">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-594">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f5a7e-595">Javítva a hiba, amely során az Azure File Directory eltávolítása egy folyamattal meghiúsult</span><span class="sxs-lookup"><span data-stu-id="f5a7e-595">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="f5a7e-596">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-596">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="f5a7e-597">[#9880] javítva: Módosítva lett a NetWorkRule DefaultAction értékdefiníciója, hogy megfeleljen a Swaggernek.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-597">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="f5a7e-598">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-598">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="f5a7e-599">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-599">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="f5a7e-600">[#11624] javítva: Duplikált szabályok kihagyása NetworkRules hozzáadásakor a kiszolgáló meghibásodásának elkerülése érdekében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-600">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="f5a7e-601">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-601">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="f5a7e-602">A Microsoft.Azure.Cosmos.Table SDK verziója 1.0.7-re frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-602">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="f5a7e-603">Hozzá lett adva egy figyelmeztető üzenet, amely emlékezteti a felhasználót, hogy listázzon újra a ContinuationToken használatával, ha csak részleges elemeket ad vissza a rendszer a Data Lake Gen2 elemek listáján</span><span class="sxs-lookup"><span data-stu-id="f5a7e-603">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="f5a7e-604">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="f5a7e-604">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="f5a7e-605">Storage-fiók létrehozásának és frissítésének támogatása Azure Files Active Directory Domain Service-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="f5a7e-605">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="f5a7e-606">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-606">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="f5a7e-607">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-607">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f5a7e-608">Storage-fiók Kerberos-kulcsai listázásának vagy új Kerberos-kulcsok létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-608">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="f5a7e-609">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f5a7e-609">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="f5a7e-610">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f5a7e-610">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="f5a7e-611">Feladatátvételi Storage-fiók támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-611">Supported failover Storage account</span></span>
    - <span data-ttu-id="f5a7e-612">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="f5a7e-612">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="f5a7e-613">Frissítve a Get-AzStorageBlobCopyState súgója</span><span class="sxs-lookup"><span data-stu-id="f5a7e-613">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="f5a7e-614">Frissítve a Get-AzStorageFileCopyState és a Start-AzStorageBlobCopy súgója</span><span class="sxs-lookup"><span data-stu-id="f5a7e-614">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="f5a7e-615">A Storage-ügyfélkódtár 12-es verziója integrálva lett a Queue és a File parancsmagokba</span><span class="sxs-lookup"><span data-stu-id="f5a7e-615">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="f5a7e-616">A kimenet típusa CloudFile helyett mostantól AzureStorageFile, az eredeti kimenet az új kimenet gyermektulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-616">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="f5a7e-617">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="f5a7e-617">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="f5a7e-618">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="f5a7e-618">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="f5a7e-619">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f5a7e-619">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="f5a7e-620">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f5a7e-620">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="f5a7e-621">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-621">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="f5a7e-622">A kimenet típusa CloudFileDirectory helyett mostantól AzureStorageFileDirectory, az eredeti kimenet az új kimenet gyermektulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-622">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="f5a7e-623">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-623">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="f5a7e-624">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-624">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="f5a7e-625">A kimenet típusa CloudFileShare helyett mostantól AzureStorageFileShare, az eredeti kimenet az új kimenet gyermektulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-625">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="f5a7e-626">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="f5a7e-626">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="f5a7e-627">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="f5a7e-627">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="f5a7e-628">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="f5a7e-628">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="f5a7e-629">A kimenet típusa FileShareProperties helyett mostantól AzureStorageFileShare, az eredeti kimenet az új kimenet gyermek-altulajdonsága lesz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-629">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="f5a7e-630">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="f5a7e-630">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f5a7e-631">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f5a7e-631">Az.TrafficManager</span></span>
* <span data-ttu-id="f5a7e-632">Javítva a hibás profilnév a DisableAzureTrafficManagerEndpoint részletes kimenetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-632">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-633">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-633">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-634">Javítva az elgépelés az Update-AzWebAppAccessRestrictionConfig súgójában.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-634">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="f5a7e-635">3.8.0 – 2020. április</span><span class="sxs-lookup"><span data-stu-id="f5a7e-635">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="f5a7e-636">A legutóbbi kiadás óta bevezetett újdonságok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-636">Highlights since the last release</span></span>
* <span data-ttu-id="f5a7e-637">Az Az.Storage által támogatott PowerShell-verziók: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="f5a7e-637">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-638">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-638">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-639">Frissítve lett az Azure PowerShell-felmérés URL-címe a következő helyen: Resolve-AzError [#11507]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-639">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5a7e-640">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5a7e-640">Az.ApiManagement</span></span>
* <span data-ttu-id="f5a7e-641">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó értesítés az Azure File parancsmagok kimenetére vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-641">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="f5a7e-642">Set-AzApiManagementGroup – Frissítve lett a dokumentáció a GroupId paraméter meghatározása érdekében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-642">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f5a7e-643">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5a7e-643">Az.Cdn</span></span>
* <span data-ttu-id="f5a7e-644">Ki lett javítva a díjszabási termékváltozat megjelenítése a ChinaCDN kapcsán</span><span class="sxs-lookup"><span data-stu-id="f5a7e-644">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5a7e-645">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-645">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5a7e-646">Támogatott identitás, Titkosítás, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-646">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-647">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-648">Hozzá lett adva a Set-AzVmssOrchestrationServiceState parancsmag.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-648">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="f5a7e-649">A Get-AzVmss az InstanceView használatával az OrchestrationService állapotait mutatja.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-649">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5a7e-650">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-650">Az.IotHub</span></span>
* <span data-ttu-id="f5a7e-651">Az IoT-ikereszköz konfigurációjának kezelése, Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-651">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="f5a7e-652">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="f5a7e-652">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="f5a7e-653">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="f5a7e-653">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="f5a7e-654">Hozzá lett adva egy parancsmag a közvetlen metódusok az IoT Hubban lévő eszközökön való meghívásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-654">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="f5a7e-655">Az IoT-ikereszköz modulja konfigurációjának kezelése, Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-655">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="f5a7e-656">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="f5a7e-656">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="f5a7e-657">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="f5a7e-657">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="f5a7e-658">Nagy méretekben történő automatikus IoT-eszközfelügyelet konfigurációjának kezelése.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-658">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="f5a7e-659">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-659">New cmdlets are:</span></span>
    - <span data-ttu-id="f5a7e-660">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-660">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f5a7e-661">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-661">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f5a7e-662">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-662">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f5a7e-663">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-663">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="f5a7e-664">Hozzá lett adva egy parancsmag az Edge-modul metódusok az IoT Hubban való meghívásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-664">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5a7e-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5a7e-665">Az.KeyVault</span></span>
* <span data-ttu-id="f5a7e-666">Hozzá lett adva egy új Update-AzKeyVault parancsmag a helyreállító törlés és végleges törlés elleni védelem tárolón való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-666">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="f5a7e-667">Támogatás a következőhöz: Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-667">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="f5a7e-668">Ki lettek javítva a Remove-AzKeyVaultManagedStorageSasDefinition [#11479] példáinak hibái</span><span class="sxs-lookup"><span data-stu-id="f5a7e-668">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="f5a7e-669">Támogatás a privát végponthoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-669">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="f5a7e-670">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="f5a7e-670">Az.Maintenance</span></span>
* <span data-ttu-id="f5a7e-671">Karbantartási parancsmagok végleges verziójának közzététele az általánosan elérhető kiadás számára</span><span class="sxs-lookup"><span data-stu-id="f5a7e-671">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5a7e-672">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-672">Az.Monitor</span></span>
* <span data-ttu-id="f5a7e-673">Parancsmagok hozzáadva a privát kapcsolat hatóköréhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-673">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="f5a7e-674">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f5a7e-674">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f5a7e-675">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f5a7e-675">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f5a7e-676">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f5a7e-676">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f5a7e-677">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f5a7e-677">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f5a7e-678">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f5a7e-678">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="f5a7e-679">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f5a7e-679">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="f5a7e-680">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f5a7e-680">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-681">Az.Network</span></span>
* <span data-ttu-id="f5a7e-682">Frissítve lettek a parancsmagok a virtuális hálózati átjáróhoz való csatlakozás engedélyezéséhez magánhálózati IP-cím esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-682">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="f5a7e-683">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f5a7e-683">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="f5a7e-684">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f5a7e-684">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="f5a7e-685">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-685">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="f5a7e-686">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-686">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="f5a7e-687">Frissítve lettek a parancsmagok az FQDN-alapú LocalNetworkGateways és VpnSites engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-687">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="f5a7e-688">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f5a7e-688">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="f5a7e-689">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="f5a7e-689">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="f5a7e-690">Az IPv6-címcsalád támogatása a következőben: ExpressRouteCircuitConnectionConfig (Global Reach)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-690">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="f5a7e-691">Hozzá lett adva a Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-691">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="f5a7e-692">lehetővé teszi az összes meglévő tulajdonság beállítását, beleértve a következőt is: IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="f5a7e-692">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="f5a7e-693">Frissítve lett az Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-693">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="f5a7e-694">Hozzá lett adva egy másik opcionális AddressPrefixType paraméter a címelőtag címcsaládjának meghatározásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-694">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="f5a7e-695">Frissítve lettek a parancsmagok a DPD-időtúllépés beállításának engedélyezéséhez a virtuális hálózati átjáró kapcsolatain.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-695">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="f5a7e-696">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-696">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="f5a7e-697">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-697">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5a7e-698">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-698">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5a7e-699">Hozzá lett adva a Start-AzPolicyComplianceScan parancsmag a szabályzatok megfelelőségi vizsgálatának elindításához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-699">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="f5a7e-700">Szabályzatdefiníció, készletdefiníció és hozzárendelési verziók hozzáadva a Get-AzPolicyState kimenetéhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-700">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5a7e-701">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5a7e-701">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5a7e-702">Tovább lett fejlesztve a kódok formázása és a használhatóság a New-AzServiceFabricCluster példái esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-702">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-703">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-704">Hozzá lettek adva a Get-AzSqlInstanceOperation és a Stop-AzSqlInstanceOperation parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-704">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="f5a7e-705">Naplózás támogatása egy VNet-ben található tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-705">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-706">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-707">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó értesítés az Azure File parancsmagok kimenetére vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-707">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="f5a7e-708">Támogatott új SkuName StandardGZRS, StandardRAGZRS a Storage-fiók létrehozása/frissítése során</span><span class="sxs-lookup"><span data-stu-id="f5a7e-708">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="f5a7e-709">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-709">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="f5a7e-710">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-710">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f5a7e-711">Támogatott Data Lake Gen2</span><span class="sxs-lookup"><span data-stu-id="f5a7e-711">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="f5a7e-712">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f5a7e-712">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f5a7e-713">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f5a7e-713">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f5a7e-714">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="f5a7e-714">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="f5a7e-715">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f5a7e-715">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f5a7e-716">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="f5a7e-716">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="f5a7e-717">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f5a7e-717">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f5a7e-718">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="f5a7e-718">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="f5a7e-719">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f5a7e-719">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="f5a7e-720">0.10.0-s előzetes verzió – 2020. április</span><span class="sxs-lookup"><span data-stu-id="f5a7e-720">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="f5a7e-721">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f5a7e-721">General</span></span>
* <span data-ttu-id="f5a7e-722">Az Az modulok előzetes verziója mostantól elérhető az Azure Stack Hubon.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-722">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="f5a7e-723">Ez lehetővé teszi a platformok közötti kompatibilitást a Linux és a macOs rendszerekkel.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-723">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="f5a7e-724">A Azure Stack Hub mostantól támogatja a PowerShell Core-t az Az modulokkal, további információt [itt](https://aka.ms/az4AzureStack) talál</span><span class="sxs-lookup"><span data-stu-id="f5a7e-724">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="f5a7e-725">Az Az modulok támogatják a 2019-03-01-hybrid profilt:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-725">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="f5a7e-726">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f5a7e-726">Az.Billing</span></span>
  - <span data-ttu-id="f5a7e-727">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-727">Az.Compute</span></span>
  - <span data-ttu-id="f5a7e-728">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f5a7e-728">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="f5a7e-729">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-729">Az.EventHub</span></span>
  - <span data-ttu-id="f5a7e-730">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-730">Az.IotHub</span></span>
  - <span data-ttu-id="f5a7e-731">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5a7e-731">Az.KeyVault</span></span>
  - <span data-ttu-id="f5a7e-732">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-732">Az.Monitor</span></span>
  - <span data-ttu-id="f5a7e-733">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-733">Az.Network</span></span>
  - <span data-ttu-id="f5a7e-734">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-734">Az.Resources</span></span>
  - <span data-ttu-id="f5a7e-735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-735">Az.Storage</span></span>
  - <span data-ttu-id="f5a7e-736">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-736">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-737">A következő három új PowerShell-modul lett bevezetve, amelyek használhatók az Azure Stack Hubbal: Az.Databox, Az.IotHub és Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-737">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="f5a7e-738">A parancsok viszonylag változatlanok maradnak, kisebb módosításokkal. Például az Az helyébe az AzureRM lép.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-738">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="f5a7e-739">Az Azure Stack Hubhoz kapcsolódó PowerShell-dokumentáció frissített hivatkozását [itt](https://aka.ms/InstallASHPowerShell) találja</span><span class="sxs-lookup"><span data-stu-id="f5a7e-739">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="f5a7e-740">3.7.0 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="f5a7e-740">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-741">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-741">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-742">Ki lett javítva az a hiba, hogy a Get-AzTenant/Get-AzDefault/Set-AzDefault parancs NullReferenceException hibát ad vissza kijelentkezett állapotban [#10292]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-742">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-743">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-744">A következő paraméterek lettek hozzáadva a New-AzDiskConfig parancsmaghoz:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-744">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="f5a7e-745">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="f5a7e-745">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="f5a7e-746">Engedélyezve lett a New-AzGalleryImageVersion parancsmag célparaméterének titkosítási tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-746">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="f5a7e-747">Ki lett javítva a tempDisk hibája a Set-AzVmss -Reimage és az Invoke-AzVMReimage parancsmag esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-747">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="f5a7e-748">[#11354]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-748">[#11354]</span></span>
* <span data-ttu-id="f5a7e-749">Az alábbi parancsmagok mostantól támogatottak az új SAP-bővítmény esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-749">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="f5a7e-750">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f5a7e-750">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f5a7e-751">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f5a7e-751">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f5a7e-752">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f5a7e-752">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f5a7e-753">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="f5a7e-753">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="f5a7e-754">Ki lettek javítva a súgódokumentáció példáinak hibái</span><span class="sxs-lookup"><span data-stu-id="f5a7e-754">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="f5a7e-755">Táblázatos formátumban jelenítette meg a sztring pontos értékét a PowerState virtuális gép esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-755">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="f5a7e-756">New-AzVmssConfig: ki lett javítva az AutomaticRepairs tulajdonság szerializálása a SinglePlacementGroup letiltott állapota esetén.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-756">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="f5a7e-757">[#11257]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-757">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-758">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-758">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-759">Az ADF .Net SDK a 4.8.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-759">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="f5a7e-760">Opcionális paraméterek lettek hozzáadva az Invoke-AzDataFactoryV2Pipeline parancshoz az újrafuttatás támogatásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-760">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5a7e-761">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5a7e-761">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5a7e-762">Hozzá lett adva a kompatibilitástörő változás leírása az Export-AzDataLakeStoreItem és az Import-AzDataLakeStoreItem parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-762">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="f5a7e-763">A bájtkódolási lehetőség hozzá lett adva a New-AzDataLakeStoreItem, az Add-AzDAtaLakeStoreItemContent és a Get-AzDAtaLakeStoreItemContent parancsok esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-763">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5a7e-764">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5a7e-764">Az.HDInsight</span></span>
* <span data-ttu-id="f5a7e-765">Fürt létrehozásakor a minimálisan támogatott TLS-verzió megadása támogatott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-765">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5a7e-766">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-766">Az.IotHub</span></span>
* <span data-ttu-id="f5a7e-767">Hozzá lett adva az elosztott beállítások eszközönkénti felügyeletének támogatása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-767">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="f5a7e-768">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-768">New Cmdlets are:</span></span>
    - <span data-ttu-id="f5a7e-769">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="f5a7e-769">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="f5a7e-770">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="f5a7e-770">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5a7e-771">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5a7e-771">Az.KeyVault</span></span>
* <span data-ttu-id="f5a7e-772">Kompatibilitástörő változást okozó attribútumok lettek hozzáadva a New-AzKeyVault parancshoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-772">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5a7e-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-773">Az.Monitor</span></span>
* <span data-ttu-id="f5a7e-774">Frissült a New-AzScheduledQueryRuleLogMetricTrigger dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f5a7e-774">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-775">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-775">Az.Network</span></span>
* <span data-ttu-id="f5a7e-776">Frissültek a parancsmagok a több-bérlős VirtualHubVnetConnections engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-776">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="f5a7e-777">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-777">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f5a7e-778">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-778">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f5a7e-779">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-779">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="f5a7e-780">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-780">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="f5a7e-781">Az SQL Management SDK-függőség el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-781">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5a7e-782">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-782">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5a7e-783">Továbbfejlesztett hibaüzenetek</span><span class="sxs-lookup"><span data-stu-id="f5a7e-783">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-784">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-784">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-785">Hozzá lett adva az Azure Site Recovery-támogatás az Azure Diskkel titkosított virtuális gépek védelmének újbóli beállítása és frissített virtuálisgép-tulajdonságai esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-785">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="f5a7e-786">Hozzá lett adva az Azure Site Recovery VmwareToAzure tulajdonságainak vészhelyreállítási monitorozása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-786">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="f5a7e-787">Hozzá lett adva az Azure Backup-támogatás a sikertelen elemekre vonatkozó szabályzatfrissítés újbóli végrehajtása esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-787">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="f5a7e-788">Hozzá lett adva az Azure Backup-támogatás a lemezkizárási beállításokhoz a biztonsági mentés és a visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-788">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="f5a7e-789">Hozzá lett adva az Azure Backup-támogatás több fájl/mappa visszaállításához az AzureFileShare-ben</span><span class="sxs-lookup"><span data-stu-id="f5a7e-789">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="f5a7e-790">Hozzá lett adva az Azure Backup-támogatás a felhasználó által megadott erőforráscsoport támogatásához az IaasVM-szabályzat frissítésekor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-790">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-791">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-792">Ki lett javítva a Get-AzResource-ResourceGroupName-Name-ExpandProperties-ResourceType parancs, hogy ezentúl az erőforrások aktuális API-verzióját használja az alapértelmezett verzió helyett [#11267]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-792">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="f5a7e-793">Hozzá lett adva a CorrelationId-naplózás a hibaforgatókönyvek esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-793">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="f5a7e-794">A Get-AzResourceLock dokumentációjában kisebb módosítás történt.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-794">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="f5a7e-795">Példa hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-795">Added example.</span></span>
* <span data-ttu-id="f5a7e-796">A szimpla idézőjel fel lett oldva a Get-AzADUser paraméterértékében [#11317]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-796">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="f5a7e-797">Új parancsmagok lettek hozzáadva az üzembehelyezési szkriptekhez (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-797">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-798">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-799">Olvasható másodlagos paraméter lett hozzáadva az Invoke-AzSqlDatabaseFailover parancshoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-799">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="f5a7e-800">A Disable-AzSqlServerActiveDirectoryOnlyAuthentication parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-800">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="f5a7e-801">Az érzékenységi besorolás mentése megtörténik az adatbázis oszlopainak osztályozásakor.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-801">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="f5a7e-802">Az.Support</span><span class="sxs-lookup"><span data-stu-id="f5a7e-802">Az.Support</span></span>
* <span data-ttu-id="f5a7e-803">Az Az.Support modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-803">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-804">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-804">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-805">Mostantól támogatott a webalkalmazások forgalom-útválasztási szabályainak az alábbi új parancsmagokkal történő használata</span><span class="sxs-lookup"><span data-stu-id="f5a7e-805">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="f5a7e-806">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f5a7e-806">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f5a7e-807">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f5a7e-807">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f5a7e-808">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f5a7e-808">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f5a7e-809">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f5a7e-809">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="f5a7e-810">3.6.1 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="f5a7e-810">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-811">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-812">Azure PowerShell felmérési oldal megnyitása itt: Send-Feedback [#11020]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-812">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="f5a7e-813">Azure PowerShell-felmérés URL-címének megjelenítése itt: Resolve-Error [#11021]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-813">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="f5a7e-814">Az-verzió hozzáadva az UserAgenthez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-814">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5a7e-815">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5a7e-815">Az.ApiManagement</span></span>
* <span data-ttu-id="f5a7e-816">Mostantól támogatott az egyéni tartomány lekérése és konfigurálása a DeveloperPortal végpontján [#11007]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-816">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="f5a7e-817">Export-AzApiManagementAPi – Mostantól támogatott az Api-definíció Json formátumban való letöltése [#9987]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-817">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="f5a7e-818">Import-AzApiManagementApi – Az OpenAPI 3.0-definíció Json-dokumentumokból való importálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-818">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="f5a7e-819">New-AzApiManagementIdentityProvider és Set-AzApiManagementIdentityProvider – A Signin Tenant konfigurálása az AAD B2C-szolgáltató esetében mostantól támogatott. [#9784]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-819">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5a7e-820">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5a7e-820">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5a7e-821">A System.Buffershez hivatkozásának explicit hozzáadása a következőkben: csproj és psd1</span><span class="sxs-lookup"><span data-stu-id="f5a7e-821">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5a7e-822">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-822">Az.IotHub</span></span>
* <span data-ttu-id="f5a7e-823">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-823">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f5a7e-824">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-824">New Cmdlets are:</span></span>
    - <span data-ttu-id="f5a7e-825">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f5a7e-825">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f5a7e-826">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f5a7e-826">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f5a7e-827">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f5a7e-827">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f5a7e-828">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f5a7e-828">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="f5a7e-829">A cél IoT-eszközökön lévő modulok IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-829">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="f5a7e-830">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-830">New Cmdlets are:</span></span>
    - <span data-ttu-id="f5a7e-831">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-831">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="f5a7e-832">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-832">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="f5a7e-833">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-833">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="f5a7e-834">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-834">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="f5a7e-835">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-835">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f5a7e-836">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz modulja kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-836">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f5a7e-837">Az IoT-eszközök szülő eszközének lekérése/beállítása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-837">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="f5a7e-838">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-838">New Cmdlets are:</span></span>
    - <span data-ttu-id="f5a7e-839">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="f5a7e-839">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="f5a7e-840">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f5a7e-840">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="f5a7e-841">Az eszközök szülő-gyermek kapcsolatainak kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-841">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5a7e-842">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-842">Az.Monitor</span></span>
* <span data-ttu-id="f5a7e-843">A Get-AzMetricDefinition kimeneti értéke javítva [#9714]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-843">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-844">Az.Network</span></span>
* <span data-ttu-id="f5a7e-845">SQL Management SDK frissítve.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-845">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="f5a7e-846">Kijavítottuk a PrivateLinkServiceConnectionState osztály eltérő elnevezéssel kapcsolatos hibáját.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-846">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="f5a7e-847">Az ActionsRequired mező leképezése a követezőre: ActionRequired</span><span class="sxs-lookup"><span data-stu-id="f5a7e-847">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="f5a7e-848">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="f5a7e-848">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-849">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-850">A Get-AzRoleAssignment null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-850">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="f5a7e-851">A -Force és a -PassThru kapcsoló nem kötelezőként lett megjelölve a Remove-AzADGroup esetében [#10849]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-851">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="f5a7e-852">Javítva a hiba, amely miatt a MailNickname nem lett visszaadva Remove-AzADGroup esetében [#11167]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-852">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="f5a7e-853">A Remove-AzADGroup folyamatművelet működési hibája kijavítva [#11171]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-853">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="f5a7e-854">A GetAzureRoleAssignmentCommand null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-854">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="f5a7e-855">Kompatibilitástörő változás hozzáadva a szabályzati parancsmagok soron következő változásaihoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-855">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="f5a7e-856">Frissült a Get-AzResourceGroup az erőforráscsoport-címke kiszolgálóoldali szűrésének elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-856">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="f5a7e-857">A címkeparancsmagok kiterjesztése a -ResourceID elfogadása érdekében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-857">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="f5a7e-858">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5a7e-858">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f5a7e-859">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5a7e-859">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f5a7e-860">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5a7e-860">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="f5a7e-861">Új címkeparancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-861">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="f5a7e-862">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5a7e-862">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="f5a7e-863">A ScopedDeployment áthozva az SDK 3.3.0-ból</span><span class="sxs-lookup"><span data-stu-id="f5a7e-863">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-864">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-864">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-865">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="f5a7e-865">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="f5a7e-866">Támogatás hozzáadva a biztonsági másolatok hosszú távú megőrzési konfigurációjához a felügyelt adatbázisok esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-866">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="f5a7e-867">LTR-szabályzat lekérése/beállítása felügyelt adatbázison</span><span class="sxs-lookup"><span data-stu-id="f5a7e-867">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="f5a7e-868">LTR biztonsági másolat(ok) lekérése felügyelt adatbázis, felügyelt példány vagy hely szerint</span><span class="sxs-lookup"><span data-stu-id="f5a7e-868">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="f5a7e-869">LTR biztonsági másolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-869">Remove an LTR backup</span></span>
    - <span data-ttu-id="f5a7e-870">LTR biztonsági másolat visszaállítása új felügyelt adatbázis létrehozásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-870">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="f5a7e-871">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="f5a7e-871">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="f5a7e-872">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlInstance és Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f5a7e-872">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="f5a7e-873">Az SQL SDK-verzió felléptetése a következőhöz: AZ.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-873">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-874">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-874">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-875">Támogatott AllowProtectedAppendWrite a következőben: ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-875">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="f5a7e-876">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-876">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="f5a7e-877">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet az AzureStorageTable típusának módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-877">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="f5a7e-878">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="f5a7e-878">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="f5a7e-879">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="f5a7e-879">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-880">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-880">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-881">Címke paraméter hozzáadva a következőkhöz: New-AzAppServicePlan és Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f5a7e-881">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="f5a7e-882">A parancsmag végrehajtásának leállítása, ha egy egyéni tartomány webhelyhez történő hozzáadásakor a rendszer kivételt ad vissza</span><span class="sxs-lookup"><span data-stu-id="f5a7e-882">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="f5a7e-883">Támogatás hozzáadva az olyan App Services műveletek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-883">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="f5a7e-884">Hozzáférési korlátozás alkalmazva a különböző erőforráscsoportokban lévő webalkalmazásokra/függvényekre</span><span class="sxs-lookup"><span data-stu-id="f5a7e-884">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="f5a7e-885">Az egyéni WebAppSlots-gazdanevek beállítására vonatkozó hiba kijavítva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-885">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="f5a7e-886">3.5.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="f5a7e-886">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f5a7e-887">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-887">Highlights since the last major release</span></span>
* <span data-ttu-id="f5a7e-888">Frissült az ügyféloldali telemetria.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-888">Updated client side telemetry.</span></span>
* <span data-ttu-id="f5a7e-889">Az.IotHub: parancsmagok hozzáadva az eszközkezelés támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-889">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="f5a7e-890">Az.SqlVirtualMachine: parancsmagok hozzáadva a rendelkezésreállási csoport figyelőjéhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-890">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-891">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-891">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-892">A SubscriptionId, a TenantId és a végrehajtási idő hozzáadva az ügyféloldali telemetria adataihoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-892">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5a7e-893">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-893">Az.Automation</span></span>
* <span data-ttu-id="f5a7e-894">Ki lett javítva a „New-AzAutomationSoftwareUpdateConfiguration” referenciadokumentációjának 1. példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="f5a7e-894">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5a7e-895">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-895">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5a7e-896">Az SDK a 7.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-896">Updated SDK to 7.0</span></span>
* <span data-ttu-id="f5a7e-897">Tovább lett fejlesztve a hibaüzenet, amely akkor jelenik meg, ha a kiszolgáló üres törzset ad vissza válaszként</span><span class="sxs-lookup"><span data-stu-id="f5a7e-897">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-898">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-898">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-899">A ProximityPlacementGroupId mostantól üres értékkel is rendelkezhet a frissítés során</span><span class="sxs-lookup"><span data-stu-id="f5a7e-899">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5a7e-900">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-900">Az.FrontDoor</span></span>
* <span data-ttu-id="f5a7e-901">Új parancsmag hozzáadva a WAF-ban használható felügyelt szabálydefiníciók lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-901">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5a7e-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-902">Az.IotHub</span></span>
* <span data-ttu-id="f5a7e-903">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-903">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f5a7e-904">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-904">New Cmdlets are:</span></span>
    - <span data-ttu-id="f5a7e-905">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f5a7e-905">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f5a7e-906">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f5a7e-906">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f5a7e-907">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f5a7e-907">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f5a7e-908">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f5a7e-908">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5a7e-909">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5a7e-909">Az.KeyVault</span></span>
* <span data-ttu-id="f5a7e-910">Ki lett javítva az Add-AzKeyVaultKey.md duplikált szövege</span><span class="sxs-lookup"><span data-stu-id="f5a7e-910">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5a7e-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-911">Az.Monitor</span></span>
* <span data-ttu-id="f5a7e-912">Ki lett javítva a Get-AzLog parancsmag leírása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-912">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="f5a7e-913">Egy új, ActionGroupId nevű paraméter lett hozzáadva a „New-AzMetricAlertRuleV2” parancshoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-913">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="f5a7e-914">A felhasználó a következőket adhatja meg: ActionGroupId(string) vagy ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-914">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-915">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-915">Az.Network</span></span>
* <span data-ttu-id="f5a7e-916">Hozzá lett adva egy extra paramétermegjegyzés a „New-AzPrivateLinkService” parancsmag „-EnableProxyProtocol” paraméteréhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-916">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="f5a7e-917">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-917">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f5a7e-918">Hozzá lett adva egy csomagrögzítési példa a Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és Start-AzVirtualnetworkGatewayPacketCapture.md minden belső és külső csomagjának rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-918">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f5a7e-919">Az Azure Firewall-szabályzat mostantól támogatott a Vnet-tűzfalakon</span><span class="sxs-lookup"><span data-stu-id="f5a7e-919">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="f5a7e-920">Nem lettek hozzáadva új parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-920">No new cmdlets are added.</span></span> <span data-ttu-id="f5a7e-921">Enyhítve lettek a tűzfalszabályzat korlátozásai a Vnet-tűzfalak esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-921">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-922">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-922">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-923">A fájlokként történő visszaállítás mostantól támogatott az SQL-adatbázisok esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-923">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-924">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-924">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-925">Újra lettek tervezve a sablonalapú üzembehelyezési parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-925">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="f5a7e-926">Új parancsmagok lettek hozzáadva a felügyeleti csoportban való üzembe helyezés kezeléséhez: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f5a7e-926">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="f5a7e-927">Új parancsmagok lettek hozzáadva a bérlői hatókörben való üzembe helyezés kezeléséhez: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f5a7e-927">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="f5a7e-928">Az \*-AzDeployment parancsmagok kifejezetten az előfizetési hatókörben való működéshez lettek újratervezve</span><span class="sxs-lookup"><span data-stu-id="f5a7e-928">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="f5a7e-929">Az \*-AzSubscriptionDeployment aliasok lettek létrehozva az \*-AzDeployment parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-929">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="f5a7e-930">Ki lett javítva az „Update-AzADApplication” nem beállított „AvailableToOtherTenants” paraméter esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-930">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="f5a7e-931">Az ApplicationObjectWithoutCredentialParameterSet el lett távolítva az AmbiguousParameterSetException elkerülése érdekében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-931">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="f5a7e-932">A súgófájlok újra létre lettek hozva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-932">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-933">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-933">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-934">Az előfizetések közötti időponthoz kötött visszaállítás mostantól támogatott a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-934">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="f5a7e-935">A már meglévő felügyelt SQL-példány hardvergenerációjának módosítása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="f5a7e-935">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="f5a7e-936">Ki lettek javítva az „Update-AzSqlServerVulnerabilityAssessmentSetting” súgópéldái: paraméter/tulajdonságkimenet – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="f5a7e-936">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f5a7e-937">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f5a7e-937">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f5a7e-938">Parancsmagokat hozzáadva a rendelkezésreállási csoport figyelőjéhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-938">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f5a7e-939">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f5a7e-939">Az.StorageSync</span></span>
* <span data-ttu-id="f5a7e-940">Frissültek az „Invoke-AzStorageSyncCompatibilityCheck” támogatott karakterkészletei.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-940">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="f5a7e-941">3.4.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="f5a7e-941">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f5a7e-942">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-942">Highlights since the last major release</span></span>
* <span data-ttu-id="f5a7e-943">Megjelent az Az.CosmosDB 0.1.0-s kezdeti verziója</span><span class="sxs-lookup"><span data-stu-id="f5a7e-943">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="f5a7e-944">Az.Network ConnectionMonitor V2 támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-944">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-945">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-946">A környezet automatikus mentésének letiltása, ha az AzureRmContext.json nem érhető el</span><span class="sxs-lookup"><span data-stu-id="f5a7e-946">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="f5a7e-947">Az Azure Powershell Common referenciájának frissítése 1.3.5-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="f5a7e-947">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5a7e-948">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5a7e-948">Az.ApiManagement</span></span>
* <span data-ttu-id="f5a7e-949">**Get-AzApiManagementApiSchema** Az API-val társított Open-API séma kijavítása   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="f5a7e-949">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="f5a7e-950">**New-AzApiManagementProduct**\* és **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="f5a7e-950">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="f5a7e-951">https://github.com/Azure/azure-powershell/issues/10472 dokumentációja kijavítva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-951">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="f5a7e-952">**Set-AzApiManagementApi** A ServiceUrl parancsmaggal való frissítését bemutató példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-952">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-953">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-953">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-954">A virtuális gép állapotának korlátozása 100 értékre, hogy ne legyen szabályozás, ha a Get-AzVM -Status a virtuális gép neve nélkül lett végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-954">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="f5a7e-955">Update-AzDiskEncryptionSet parancsmagok hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-955">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="f5a7e-956">Az EncryptionType és a DiskEncryptionSetId paraméterek hozzáadása a következő parancsmagokhoz:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-956">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="f5a7e-957">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-957">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="f5a7e-958">A ColocationStatus paraméter hozzáadva a Get-AzProximityPlacementGroup parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-958">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-959">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-959">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-960">Az ADF .Net SDK frissítve lett a 4.7.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="f5a7e-960">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f5a7e-961">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f5a7e-961">Az.DeploymentManager</span></span>
* <span data-ttu-id="f5a7e-962">LIST műveletek hozzáadása az erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-962">Adds LIST operations for resources</span></span>
* <span data-ttu-id="f5a7e-963">Műveletek végrehajtásának lehetősége az állapotellenőrzés lépésein</span><span class="sxs-lookup"><span data-stu-id="f5a7e-963">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5a7e-964">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5a7e-964">Az.HDInsight</span></span>
* <span data-ttu-id="f5a7e-965">A New-AzHDInsightCluster dokumentációs hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-965">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5a7e-966">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5a7e-966">Az.KeyVault</span></span>
* <span data-ttu-id="f5a7e-967">Name alias hozzáadása a VaultName attribútumhoz, hogy a Remove-AzureKeyVault konzisztens legyen a New-AzureKeyVault paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-967">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-968">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-968">Az.Network</span></span>
* <span data-ttu-id="f5a7e-969">Új példa hozzáadva a Set-AzNetworkWatcherConfigFlowLog.md fájlhoz a Traffic Analytics-letiltási forgatókönyv szemléltetésére.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-969">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="f5a7e-970">Felügyeleti IP-konfiguráció támogatás hozzáadva az Azure Firewallhoz – egy dedikált alhálózat és nyilvános IP-cím, amelyet a tűzfal a forgalom felügyeléséhez használni fog</span><span class="sxs-lookup"><span data-stu-id="f5a7e-970">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="f5a7e-971">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-971">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f5a7e-972">Hozzá lett adva a (nem kötelező) -PublicIpAddress-ManagementPublicIpAddress paraméter, amely egy nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="f5a7e-972">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="f5a7e-973">Hozzá lett adva a SetManagementIpConfiguration metódus a tűzfalobjektumok esetében – nyilvános IP-cím-objektumokat fogad el bemeneti adatként – az alhálózat nevének AzureFirewallManagementSubnet értéknek kell lennie</span><span class="sxs-lookup"><span data-stu-id="f5a7e-973">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="f5a7e-974">A Get-AzNetworkSecurityGroup példái javítva, hogy hálózati biztonsági csoportok példáit tartalmazzák hálózati adapterek helyett.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-974">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="f5a7e-975">Javítottunk egy elírást a New-AzVpnSite parancsban, amely megakadályozta, hogy az erőforrásazonosító-kiegészítő kiegészítsen egy paramétert.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-975">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="f5a7e-976">Az Application Gateway szabály-újraírási műveletkészletének URL-konfigurálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-976">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="f5a7e-977">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-977">New cmdlets added:</span></span>
        - <span data-ttu-id="f5a7e-978">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-978">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="f5a7e-979">A parancsmagok frissültek a nem kötelező UrlConfiguration paraméterrel</span><span class="sxs-lookup"><span data-stu-id="f5a7e-979">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="f5a7e-980">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-980">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="f5a7e-981">A Network Watcher Connection Monitor 2-es verziójú erőforrások támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-981">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5a7e-982">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-982">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5a7e-983">A javítandó erőforrások azonosítása előtti megfelelőségértékelés támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-983">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="f5a7e-984">-ResourceDiscoverMode paraméter hozzáadása a Start-AzPolicyRemediation parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-984">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="f5a7e-985">A szabályzatok metaadat-erőforrásainak elérésére szolgáló Get-AzPolicyMetadata parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-985">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="f5a7e-986">A Get-AzPolicyState és a Get-AzPolicyStateSummary frissült a 2019-10-01 API-verzióhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-986">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-987">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-987">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-988">Azure Site Recovery-támogatás a replikált lemezek eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-988">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="f5a7e-989">Hozzáadott Azure Backup-támogatás a helyreállítási tárak létrehozása közbeni címkehozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-989">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-990">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-990">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-991">A -Scope választható a \*-AzPolicyAssignment parancsmagokban; az alapértelmezett érték a környezeti előfizetés</span><span class="sxs-lookup"><span data-stu-id="f5a7e-991">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="f5a7e-992">Az ADServicePrincipal jelszó és kulcs típusú hitelesítő adatokkal való létrehozását szemléltető példák hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-992">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-993">Az.Sql</span></span>
<span data-ttu-id="f5a7e-994">A New-AzSqlDatabaseSecondary parancsmag javítva, hogy a PartnerDatabaseName létezését ellenőrizze a DatabaseName létezése helyett.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-994">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-995">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-996">A Table/Queue Encryption Keytype készlet beállításának támogatása Storage-fiók létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-996">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="f5a7e-997">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-997">New-AzStorageAccount</span></span>
* <span data-ttu-id="f5a7e-998">RequestId megjelenítése, ha a StorageException nem rendelkezik ExtendedErrorInformation paraméterrel</span><span class="sxs-lookup"><span data-stu-id="f5a7e-998">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="f5a7e-999">A Start-AzStorageBlobCopy parancsmag 6. példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-999">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-1000">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1000">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-1001">A Set-AzWebapp és a Set-AzWebappSlot támogatja az AlwaysOn, a MinTls és a FtpsState tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1001">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="f5a7e-1002">Javítva a hiba, amely miatt a HttpsOnly és az AppservicePlan Set-AzWebApp paranccsal történő egyidejű módosításakor a HttpsOnly paraméter alaphelyzetbe állt.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1002">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="f5a7e-1003">3.3.0 – 2020. január</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1003">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-1004">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1004">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-1005">Frissítve lettek az Add-AzEnvironment és Set-AzEnvironment parancsmagok, amelyek mostantól elfogadják az AzureAttestationServiceEndpointResourceId és AzureAttestationServiceEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1005">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f5a7e-1006">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1006">Az.Cdn</span></span>
* <span data-ttu-id="f5a7e-1007">A hibaválasz részleteinek láthatóvá tétele a New-AzCdnEndpoint parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1007">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-1008">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1008">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-1009">Javítva lett a Set-AzVMCustomScriptExtension parancsmag az olyan virtuális gépek esetében, amelyek felügyelt operációsrendszer-lemeze nem rendelkezik operációsrendszer-profillal.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1009">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f5a7e-1010">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1010">Az.ContainerInstance</span></span>
* <span data-ttu-id="f5a7e-1011">Javítva lettek a New-AzContainerGroup parancsmagpélda által használt paraméternevek</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1011">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f5a7e-1012">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1012">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f5a7e-1013">Hozzá lett adva a Get-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1013">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f5a7e-1014">Az Edge Storage-tároló lekérése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1014">Get the Edge Storage Container</span></span>
* <span data-ttu-id="f5a7e-1015">Hozzá lett adva a New-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1015">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f5a7e-1016">Új Edge Storage-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1016">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="f5a7e-1017">Hozzá lett adva a Remove-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1017">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f5a7e-1018">Az Edge Storage-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1018">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="f5a7e-1019">Hozzá lett adva az Invoke-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1019">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f5a7e-1020">Meghívási művelet az Edge Storage-tárolóban lévő adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1020">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="f5a7e-1021">Hozzá lett adva a Get-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1021">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f5a7e-1022">Az Edge Storage-fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1022">Get the Edge Storage Account</span></span>
* <span data-ttu-id="f5a7e-1023">Hozzá lett adva a New-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1023">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f5a7e-1024">Új Edge Storage-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1024">Create new Edge Storage Account</span></span>
* <span data-ttu-id="f5a7e-1025">Hozzá lett adva a Remove-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1025">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f5a7e-1026">Az Edge Storage-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1026">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="f5a7e-1027">Hozzá lett adva az Invoke-AzDataBoxEdgeShare parancsmag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1027">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="f5a7e-1028">Meghívási művelet a megosztott adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1028">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="f5a7e-1029">Hozzá lett adva a Set-AzDataBoxEdgeStorageAccountCredential parancsmag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1029">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="f5a7e-1030">Az Az.DataBoxEdge tárfiók hitelesítő adatainak beállítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1030">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-1031">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1031">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-1032">Hozzá lettek adva az AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId és VersionStatus tulajdonságok a Get-AzDataFactoryV2IntegrationRuntime parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1032">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="f5a7e-1033">Az ADF .Net SDK frissítve lett a 4.6.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1033">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="f5a7e-1034">A PublicIPs paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz statikus nyilvános IP-címekkel rendelkező Azure-SSIS IR létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1034">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="f5a7e-1035">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1035">Az.DevTestLabs</span></span>
* <span data-ttu-id="f5a7e-1036">A hibás hivatkozás el lett távolítva a Get-AzDtlAllowedVMSizesPolicy.md parancsmagból</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1036">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5a7e-1037">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1037">Az.EventHub</span></span>
* <span data-ttu-id="f5a7e-1038">A 10634-es hiba javítása: Ki lett javítva a nullértékű objektumhivatkozás a remove eventhubnamespace esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1038">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5a7e-1039">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1039">Az.HDInsight</span></span>
* <span data-ttu-id="f5a7e-1040">Ki lett javítva az Invoke-AzHDInsightHiveJob.md hibája.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1040">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f5a7e-1041">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1041">Az.MachineLearning</span></span>
* <span data-ttu-id="f5a7e-1042">El lettek távolítva az alábbi parancsmagok, mivel a MachineLearningCompute már nem érhető el</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1042">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="f5a7e-1043">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1043">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="f5a7e-1044">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1044">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="f5a7e-1045">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1045">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="f5a7e-1046">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1046">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="f5a7e-1047">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1047">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="f5a7e-1048">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1048">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="f5a7e-1049">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1049">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-1050">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1050">Az.Network</span></span>
* <span data-ttu-id="f5a7e-1051">Frissítve lett a Microsoft.Azure.Management.Sql függősége: 1.36-preview helyett 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1051">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-1052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1052">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-1053">Módosított Azure Site Recovery-támogatás azon felügyelt lemezeken található, inaktív állapotban titkosított virtuális gépeknél, amelyekhez felhasználó által kezelt kulcsok tartoznak a következő esetében: Azure – Azure-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1053">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="f5a7e-1054">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a védelem engedélyezése során a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1054">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f5a7e-1055">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a lemez szintjén a védelem engedélyezéséhez a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1055">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f5a7e-1056">Azure Site Recovery-támogatás a Replikációval védett, lemeztitkosítási csoportleképezéssel ellátott elemek frissítéséhez a következő esetében: HyperV – Azure.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1056">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-1057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1057">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-1058">Javítva lett egy hiba a Remove-AzTag súgódokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1058">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-1059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1059">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-1060">Javítva lett a sebezhetőségi felmérés csoportszintű alapkonfigurációs parancsmagjainak működése: az Azure-adatbázis főadatbázisában használható, a felügyelt példányok rendszeradatbázisaiban korlátozott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1060">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="f5a7e-1061">Ki lett javítva egy hiba az SQL-példányok feladatátvételi csoportjainak létrehozása esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1061">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f5a7e-1062">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1062">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f5a7e-1063">Hozzá lett adva a DR, mint új érvényes licenctípus</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1063">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-1064">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1064">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-1065">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet a DefaultAction értékének módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1065">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="f5a7e-1066">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1066">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="f5a7e-1067">Támogatott a tárfiók legutóbbi szinkronizálási időpontjának lekérése a get-AzureRMStorageAccount parancsmag -IncludeGeoReplicationStats paraméterrel való futtatásával</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1067">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="f5a7e-1068">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1068">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="f5a7e-1069">3.2.0 – 2019. december</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1069">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="f5a7e-1070">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1070">General</span></span>
* <span data-ttu-id="f5a7e-1071">A .psd1 hivatkozásai frissítve, hogy minden modulhoz a relatív elérési utat használják</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1071">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-1072">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1072">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-1073">A megfelelő felhasználói ügynök beállítva az ügyféloldali telemetriához az Az 4.0 előzetes verziójában</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1073">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="f5a7e-1074">Felhasználóbarát hibaüzenet megjelenítése, ha az Az 4.0 előzetes verziójában a környezet null értékű</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1074">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f5a7e-1075">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1075">Az.Batch</span></span>
* <span data-ttu-id="f5a7e-1076">Ki lett javítva a [10602-es](https://github.com/Azure/azure-powershell/issues/10602) számú hiba, amely miatt a **New-AzBatchPool** nem megfelelően küldte el a „VirtualMachineConfiguration.ContainerConfiguration” és a „VirtualMachineConfiguration.DataDisks” paramétereket a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1076">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-1077">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1077">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-1078">Az ADF .Net SDK a 4.5.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1078">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5a7e-1079">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1079">Az.FrontDoor</span></span>
* <span data-ttu-id="f5a7e-1080">A WAF felügyeleti szabályok kizárása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1080">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="f5a7e-1081">Hozzá lett adva a SocketAddr automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1081">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f5a7e-1082">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1082">Az.HealthcareApis</span></span>
* <span data-ttu-id="f5a7e-1083">Kivételkezelés</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1083">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5a7e-1084">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1084">Az.KeyVault</span></span>
* <span data-ttu-id="f5a7e-1085">Ki lett javítva az esetleg nem beállított értékek hozzáférésével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1085">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="f5a7e-1086">Az elliptikus görbéjű titkosítási tanúsítványok kezelése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1086">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="f5a7e-1087">A görbe tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1087">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5a7e-1088">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1088">Az.Monitor</span></span>
* <span data-ttu-id="f5a7e-1089">Opcionális argumentum hozzáadva a Diagnosztikai beállítások hozzáadása parancshoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1089">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="f5a7e-1090">Ez egy kapcsoló argumentum, amely megléte esetén azt jelzi, hogy a Log Analyticsbe történő exportálást egy rögzített séma (más néven</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1090">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="f5a7e-1091">dedikált adattípus) szerint kell végrehajtani</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1091">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-1092">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1092">Az.Network</span></span>
* <span data-ttu-id="f5a7e-1093">Támogatás az Ip-csoportok számára az AzureFirewall alkalmazás, valamint a Nat- és a hálózati szabályok esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1093">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1094">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-1095">Ki lett javítva az a hiba, amely miatt a sablonalapú üzembe helyezés során a sablonparamétert nem lehet olvasni, ha a sablonparaméter és egy beépített paraméter neve között névütközés áll fenn.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1095">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="f5a7e-1096">Frissültek a szabályzat parancsmagjai a 2019. 09. 01. dátumú új API-verzió használatára, amely bevezeti a szabályzatkészlet-definíciókon belüli csoportos támogatást.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1096">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-1097">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1097">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-1098">Frissítve lett a sebezhetőségi felmérés automatikus engedélyezéséhez szükséges tárterület létrehozása a Storagev2-ben</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1098">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-1099">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1099">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-1100">A blob-/tárolóidentitás-alapú SAS-token Oauth-hitelesítésen alapuló Storage-környezettel való létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1100">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="f5a7e-1101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1101">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="f5a7e-1102">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1102">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="f5a7e-1103">Támogatott lett a tárfiókhoz tartozó felhasználódelegálási kulcsok visszavonása, így minden identitásalapú SAS-token visszavonható</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1103">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="f5a7e-1104">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1104">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="f5a7e-1105">Frissítés a Microsoft.Azure.Management.Storage 14.2.0-s verziójára az új API-verzió (2019. 06. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1105">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="f5a7e-1106">A QuotaGiB (gigabájtban megadott megosztási kvóta) esetében támogatottak az 5120-nál nagyobb értékek a fájlmegosztási parancsmagok felügyeleti síkján, és hozzá lett adva a Quota paraméteralias a QuotaGiB paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1106">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="f5a7e-1107">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1107">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="f5a7e-1108">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1108">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="f5a7e-1109">A „QuotaGiB” paraméteralias hozzáadva a „kvóta” paraméterhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1109">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="f5a7e-1110">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1110">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="f5a7e-1111">Ki lett javítva az a hiba, amely miatt a Set-AzStorageContainerAcl parancsmag el tudta távolítani a tárolt hozzáférési szabályzatot</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1111">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="f5a7e-1112">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1112">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="f5a7e-1113">3.1.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1113">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f5a7e-1114">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1114">Highlights since the last major release</span></span>
* <span data-ttu-id="f5a7e-1115">Az.DataBoxEdge 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1115">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="f5a7e-1116">Az.SqlVirtualMachine 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1116">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-1117">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1117">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-1118">A virtuális gépek Reapply funkciója</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1118">VM Reapply feature</span></span>
    - <span data-ttu-id="f5a7e-1119">A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1119">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="f5a7e-1120">A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1120">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="f5a7e-1121">Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1121">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="f5a7e-1122">Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1122">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="f5a7e-1123">A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1123">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f5a7e-1124">A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1124">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="f5a7e-1125">A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1125">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="f5a7e-1126">A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1126">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="f5a7e-1127">A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1127">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="f5a7e-1128">A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1128">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f5a7e-1129">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1129">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f5a7e-1130">A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1130">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f5a7e-1131">Megrendelés lekérése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1131">Get the Order</span></span>
* <span data-ttu-id="f5a7e-1132">A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1132">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f5a7e-1133">Új megrendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1133">Create new Order</span></span>
* <span data-ttu-id="f5a7e-1134">A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1134">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f5a7e-1135">Megrendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1135">Remove the Order</span></span>
* <span data-ttu-id="f5a7e-1136">`New-AzDataBoxEdgeShare` parancsmag módosítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1136">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="f5a7e-1137">Mostantól helyi megosztást hoz létre</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1137">Now creates Local Share</span></span>
* <span data-ttu-id="f5a7e-1138">A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1138">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="f5a7e-1139">Mostantól az IotRole leképezhető a Share-re</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1139">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="f5a7e-1140">A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1140">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="f5a7e-1141">Frissítések keresésének, letöltésének, telepítésének indítása az eszközön</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1141">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="f5a7e-1142">A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1142">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f5a7e-1143">Triggerek információinak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1143">Gets the information about Triggers</span></span>
* <span data-ttu-id="f5a7e-1144">A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1144">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f5a7e-1145">Új triggerek létrehozása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1145">Create new Triggers</span></span>
* <span data-ttu-id="f5a7e-1146">A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1146">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f5a7e-1147">Triggerek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1147">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-1148">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1148">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-1149">Az ADF .Net SDK a 4.4.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1149">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="f5a7e-1150">Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1150">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5a7e-1151">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1151">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5a7e-1152">Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1152">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5a7e-1153">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1153">Az.EventHub</span></span>
* <span data-ttu-id="f5a7e-1154">A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1154">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5a7e-1155">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1155">Az.FrontDoor</span></span>
* <span data-ttu-id="f5a7e-1156">Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1156">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="f5a7e-1157">A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1157">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="f5a7e-1158">Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1158">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="f5a7e-1159">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1159">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-1160">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1160">Az.Network</span></span>
* <span data-ttu-id="f5a7e-1161">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1161">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="f5a7e-1162">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1162">Az.PrivateDns</span></span>
* <span data-ttu-id="f5a7e-1163">A PrivateDns .net sdk frissült az 1.0.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1163">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-1165">Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1165">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="f5a7e-1166">Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1166">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="f5a7e-1167">SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1167">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f5a7e-1168">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1168">Az.RedisCache</span></span>
* <span data-ttu-id="f5a7e-1169">A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1169">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="f5a7e-1170">Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1170">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="f5a7e-1171">Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1171">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1172">Az.Resources</span></span>
- <span data-ttu-id="f5a7e-1173">Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1173">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="f5a7e-1174">Frissült a létrehozási szabályzat definíciójának súgóbeli példája</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1174">Updated create policy definition help example</span></span>
- <span data-ttu-id="f5a7e-1175">Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1175">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="f5a7e-1176">Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1176">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="f5a7e-1177">A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1177">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1178">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-1179">Az adatbázisbeli ReadReplicaCount mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1179">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="f5a7e-1180">A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1180">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="f5a7e-1181">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1181">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="f5a7e-1182">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1182">General</span></span>
* <span data-ttu-id="f5a7e-1183">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1183">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-1184">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1184">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-1185">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1185">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f5a7e-1186">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1186">Az.Advisor</span></span>
* <span data-ttu-id="f5a7e-1187">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1187">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f5a7e-1188">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1188">Az.Batch</span></span>
* <span data-ttu-id="f5a7e-1189">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1189">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="f5a7e-1190">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1190">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="f5a7e-1191">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1191">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="f5a7e-1192">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1192">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="f5a7e-1193">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1193">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="f5a7e-1194">Ezek az **New-AzBatchTask**`-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1194">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="f5a7e-1195">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1195">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="f5a7e-1196">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1196">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="f5a7e-1197">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1197">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="f5a7e-1198">A `PSApplication`**Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1198">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f5a7e-1199">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1199">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="f5a7e-1200">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1200">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="f5a7e-1201">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1201">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f5a7e-1202">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1202">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="f5a7e-1203">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1203">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="f5a7e-1204">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1204">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="f5a7e-1205">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1205">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="f5a7e-1206">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1206">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="f5a7e-1207">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1207">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="f5a7e-1208">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1208">This operation is no longer supported.</span></span>
* <span data-ttu-id="f5a7e-1209">`PSCloudServiceConfiguration``TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1209">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f5a7e-1210">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1210">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f5a7e-1211">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1211">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="f5a7e-1212">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1212">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="f5a7e-1213">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1213">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="f5a7e-1214">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1214">New non-verified images are also now returned.</span></span> <span data-ttu-id="f5a7e-1215">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1215">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="f5a7e-1216">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1216">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="f5a7e-1217">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1217">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="f5a7e-1218">Ez a `PSNetworkSecurityGroupRule``SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1218">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="f5a7e-1219">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1219">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="f5a7e-1220">Ezt a `PSTaskContainerSettings``WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1220">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="f5a7e-1221">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1221">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="f5a7e-1222">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1222">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="f5a7e-1223">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1223">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="f5a7e-1224">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1224">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f5a7e-1225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1225">Az.Cdn</span></span>
* <span data-ttu-id="f5a7e-1226">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1226">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="f5a7e-1227">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1227">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-1228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1228">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-1229">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1229">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="f5a7e-1230">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1230">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="f5a7e-1231">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1231">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="f5a7e-1232">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1232">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f5a7e-1233">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1233">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="f5a7e-1234">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1234">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="f5a7e-1235">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1235">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="f5a7e-1236">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1236">Breaking changes</span></span>
    - <span data-ttu-id="f5a7e-1237">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1237">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="f5a7e-1238">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1238">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-1239">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1239">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-1240">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1240">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5a7e-1241">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1241">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5a7e-1242">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1242">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="f5a7e-1243">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1243">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="f5a7e-1244">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1244">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="f5a7e-1245">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1245">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="f5a7e-1246">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1246">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="f5a7e-1247">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1247">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5a7e-1248">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1248">Az.FrontDoor</span></span>
* <span data-ttu-id="f5a7e-1249">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1249">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5a7e-1250">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1250">Az.HDInsight</span></span>
* <span data-ttu-id="f5a7e-1251">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1251">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="f5a7e-1252">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1252">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="f5a7e-1253">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1253">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="f5a7e-1254">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1254">Removed five cmdlets:</span></span>
    - <span data-ttu-id="f5a7e-1255">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1255">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f5a7e-1256">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1256">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f5a7e-1257">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1257">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f5a7e-1258">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1258">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="f5a7e-1259">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1259">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="f5a7e-1260">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1260">Added three cmdlets:</span></span>
    - <span data-ttu-id="f5a7e-1261">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1261">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f5a7e-1262">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1262">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f5a7e-1263">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1263">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="f5a7e-1264">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1264">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="f5a7e-1265">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1265">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="f5a7e-1266">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1266">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="f5a7e-1267">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1267">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="f5a7e-1268">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1268">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="f5a7e-1269">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1269">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="f5a7e-1270">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1270">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="f5a7e-1271">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1271">Added some scenario test cases.</span></span>
* <span data-ttu-id="f5a7e-1272">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1272">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5a7e-1273">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1273">Az.IotHub</span></span>
* <span data-ttu-id="f5a7e-1274">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1274">Breaking changes:</span></span>
    - <span data-ttu-id="f5a7e-1275">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1275">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f5a7e-1276">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1276">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f5a7e-1277">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1277">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f5a7e-1278">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1278">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f5a7e-1279">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1279">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="f5a7e-1280">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1280">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="f5a7e-1281">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1281">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="f5a7e-1282">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1282">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="f5a7e-1283">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1283">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f5a7e-1284">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1284">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f5a7e-1285">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1285">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f5a7e-1286">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1286">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-1287">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1287">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-1288">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1288">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="f5a7e-1289">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1289">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="f5a7e-1290">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1290">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="f5a7e-1291">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1291">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="f5a7e-1292">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1292">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="f5a7e-1293">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1293">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="f5a7e-1294">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1294">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="f5a7e-1295">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1295">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="f5a7e-1296">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1296">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1297">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-1298">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1298">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-1299">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1299">Az.Network</span></span>
* <span data-ttu-id="f5a7e-1300">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1300">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="f5a7e-1301">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1301">Updated cmdlet:</span></span>
        - <span data-ttu-id="f5a7e-1302">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1302">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5a7e-1303">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1303">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5a7e-1304">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1304">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5a7e-1305">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1305">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5a7e-1306">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1306">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f5a7e-1307">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1307">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="f5a7e-1308">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1308">New cmdlet:</span></span>
        - <span data-ttu-id="f5a7e-1309">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1309">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="f5a7e-1310">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1310">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="f5a7e-1311">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1311">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="f5a7e-1312">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1312">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="f5a7e-1313">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1313">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="f5a7e-1314">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1314">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="f5a7e-1315">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1315">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="f5a7e-1316">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1316">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="f5a7e-1317">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1317">New cmdlets added:</span></span>
        - <span data-ttu-id="f5a7e-1318">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1318">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="f5a7e-1319">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1319">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f5a7e-1320">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1320">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f5a7e-1321">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1321">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f5a7e-1322">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1322">Set-AzVirtualHub</span></span>
* <span data-ttu-id="f5a7e-1323">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1323">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="f5a7e-1324">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1324">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f5a7e-1325">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1325">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f5a7e-1326">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1326">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f5a7e-1327">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1327">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="f5a7e-1328">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1328">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="f5a7e-1329">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1329">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="f5a7e-1330">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1330">New cmdlets added:</span></span>
        - <span data-ttu-id="f5a7e-1331">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1331">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="f5a7e-1332">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1332">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f5a7e-1333">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1333">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f5a7e-1334">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1334">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f5a7e-1335">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1335">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f5a7e-1336">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1336">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f5a7e-1337">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1337">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="f5a7e-1338">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1338">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="f5a7e-1339">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1339">New cmdlets added:</span></span>
        - <span data-ttu-id="f5a7e-1340">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1340">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="f5a7e-1341">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1341">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="f5a7e-1342">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1342">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="f5a7e-1343">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1343">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="f5a7e-1344">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1344">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="f5a7e-1345">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1345">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="f5a7e-1346">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1346">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f5a7e-1347">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1347">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="f5a7e-1348">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1348">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="f5a7e-1349">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1349">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="f5a7e-1350">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1350">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="f5a7e-1351">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1351">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f5a7e-1352">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1352">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="f5a7e-1353">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1353">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="f5a7e-1354">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1354">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="f5a7e-1355">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1355">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="f5a7e-1356">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1356">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="f5a7e-1357">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1357">New cmdlets added:</span></span>
        - <span data-ttu-id="f5a7e-1358">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1358">New-AzIpGroup</span></span>
        - <span data-ttu-id="f5a7e-1359">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1359">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="f5a7e-1360">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1360">Get-AzIpGroup</span></span>
        - <span data-ttu-id="f5a7e-1361">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1361">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5a7e-1362">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1362">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5a7e-1363">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1363">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-1364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1364">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-1365">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1365">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="f5a7e-1366">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1366">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="f5a7e-1367">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1367">Removed deprecated aliases:</span></span>
* <span data-ttu-id="f5a7e-1368">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1368">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="f5a7e-1369">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1369">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="f5a7e-1370">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1370">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f5a7e-1371">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1371">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="f5a7e-1372">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1372">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="f5a7e-1373">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1373">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-1374">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1374">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-1375">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1375">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="f5a7e-1376">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1376">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f5a7e-1377">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1377">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f5a7e-1378">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1378">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="f5a7e-1379">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1379">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="f5a7e-1380">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1380">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="f5a7e-1381">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1381">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="f5a7e-1382">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1382">General</span></span>
* <span data-ttu-id="f5a7e-1383">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1383">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-1384">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1384">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-1385">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1385">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5a7e-1386">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1386">Az.ApiManagement</span></span>
* <span data-ttu-id="f5a7e-1387">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1387">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="f5a7e-1388">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1388">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5a7e-1389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1389">Az.Automation</span></span>
* <span data-ttu-id="f5a7e-1390">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1390">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f5a7e-1391">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1391">Az.Batch</span></span>
* <span data-ttu-id="f5a7e-1392">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1392">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-1393">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1393">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-1394">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1394">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f5a7e-1395">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1395">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="f5a7e-1396">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1396">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="f5a7e-1397">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1397">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-1398">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1398">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-1399">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1399">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="f5a7e-1400">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1400">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="f5a7e-1401">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1401">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5a7e-1402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1402">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5a7e-1403">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1403">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f5a7e-1404">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1404">Az.HealthcareApis</span></span>
* <span data-ttu-id="f5a7e-1405">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1405">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="f5a7e-1406">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1406">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="f5a7e-1407">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1407">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="f5a7e-1408">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1408">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5a7e-1409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1409">Az.IotHub</span></span>
* <span data-ttu-id="f5a7e-1410">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1410">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="f5a7e-1411">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1411">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5a7e-1412">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1412">Az.Monitor</span></span>
* <span data-ttu-id="f5a7e-1413">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1413">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="f5a7e-1414">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1414">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="f5a7e-1415">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1415">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="f5a7e-1416">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1416">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-1417">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1417">Az.Network</span></span>
* <span data-ttu-id="f5a7e-1418">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1418">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="f5a7e-1419">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1419">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="f5a7e-1420">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1420">New cmdlets added:</span></span>
        - <span data-ttu-id="f5a7e-1421">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1421">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="f5a7e-1422">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1422">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f5a7e-1423">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1423">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="f5a7e-1424">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1424">Updated cmdlets:</span></span>
        - <span data-ttu-id="f5a7e-1425">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1425">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f5a7e-1426">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1426">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f5a7e-1427">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1427">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f5a7e-1428">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1428">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="f5a7e-1429">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1429">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="f5a7e-1430">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1430">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="f5a7e-1431">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1431">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f5a7e-1432">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1432">Az.RedisCache</span></span>
* <span data-ttu-id="f5a7e-1433">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1433">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-1434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1434">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-1435">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1435">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-1436">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1436">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-1437">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1437">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="f5a7e-1438">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1438">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f5a7e-1439">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1439">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="f5a7e-1440">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1440">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f5a7e-1441">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1441">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f5a7e-1442">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1442">Az.StorageSync</span></span>
* <span data-ttu-id="f5a7e-1443">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1443">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-1444">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1444">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-1445">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1445">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="f5a7e-1446">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1446">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f5a7e-1447">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1447">Az.ApiManagement</span></span>
* <span data-ttu-id="f5a7e-1448">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1448">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="f5a7e-1449">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1449">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="f5a7e-1450">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1450">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5a7e-1451">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1451">Az.Automation</span></span>
* <span data-ttu-id="f5a7e-1452">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1452">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="f5a7e-1453">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1453">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="f5a7e-1454">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1454">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-1455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1455">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-1456">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1456">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="f5a7e-1457">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1457">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f5a7e-1458">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1458">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="f5a7e-1459">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1459">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="f5a7e-1460">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1460">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="f5a7e-1461">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1461">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="f5a7e-1462">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1462">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="f5a7e-1463">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1463">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="f5a7e-1464">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1464">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-1465">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1465">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-1466">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1466">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="f5a7e-1467">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1467">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5a7e-1468">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1468">Az.HDInsight</span></span>
* <span data-ttu-id="f5a7e-1469">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1469">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5a7e-1470">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1470">Az.IotHub</span></span>
* <span data-ttu-id="f5a7e-1471">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1471">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="f5a7e-1472">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1472">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="f5a7e-1473">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1473">New cmdlets are:</span></span>
    - <span data-ttu-id="f5a7e-1474">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1474">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f5a7e-1475">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1475">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f5a7e-1476">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1476">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f5a7e-1477">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1477">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5a7e-1478">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1478">Az.Monitor</span></span>
* <span data-ttu-id="f5a7e-1479">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1479">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="f5a7e-1480">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1480">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="f5a7e-1481">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1481">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="f5a7e-1482">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1482">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="f5a7e-1483">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1483">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="f5a7e-1484">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1484">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="f5a7e-1485">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1485">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="f5a7e-1486">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1486">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="f5a7e-1487">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1487">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f5a7e-1488">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1488">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="f5a7e-1489">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1489">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f5a7e-1490">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1490">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="f5a7e-1491">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1491">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="f5a7e-1492">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1492">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="f5a7e-1493">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1493">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="f5a7e-1494">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1494">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="f5a7e-1495">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1495">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="f5a7e-1496">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1496">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="f5a7e-1497">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1497">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="f5a7e-1498">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1498">Overall improved help files</span></span>
* <span data-ttu-id="f5a7e-1499">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1499">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-1500">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1500">Az.Network</span></span>
* <span data-ttu-id="f5a7e-1501">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1501">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="f5a7e-1502">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1502">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="f5a7e-1503">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1503">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="f5a7e-1504">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1504">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="f5a7e-1505">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1505">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="f5a7e-1506">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1506">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="f5a7e-1507">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1507">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="f5a7e-1508">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1508">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="f5a7e-1509">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1509">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="f5a7e-1510">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1510">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="f5a7e-1511">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1511">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="f5a7e-1512">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1512">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="f5a7e-1513">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1513">New cmdlets</span></span>
        - <span data-ttu-id="f5a7e-1514">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1514">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="f5a7e-1515">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1515">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="f5a7e-1516">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1516">Updated cmdlet:</span></span>
        - <span data-ttu-id="f5a7e-1517">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1517">New-VpnSite</span></span>
        - <span data-ttu-id="f5a7e-1518">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1518">Update-VpnSite</span></span>
        - <span data-ttu-id="f5a7e-1519">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1519">New-VpnConnection</span></span>
        - <span data-ttu-id="f5a7e-1520">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1520">Update-VpnConnection</span></span>
* <span data-ttu-id="f5a7e-1521">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1521">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-1522">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1522">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-1523">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1523">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="f5a7e-1524">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1524">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1525">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-1526">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1526">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5a7e-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1527">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5a7e-1528">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1528">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="f5a7e-1529">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1529">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="f5a7e-1530">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1530">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f5a7e-1531">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1531">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f5a7e-1532">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1532">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f5a7e-1533">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1533">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="f5a7e-1534">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1534">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f5a7e-1535">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1535">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f5a7e-1536">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1536">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f5a7e-1537">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1537">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f5a7e-1538">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1538">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="f5a7e-1539">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1539">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f5a7e-1540">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1540">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f5a7e-1541">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1541">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f5a7e-1542">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1542">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="f5a7e-1543">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1543">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f5a7e-1544">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1544">Az.SignalR</span></span>
* <span data-ttu-id="f5a7e-1545">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1545">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-1546">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1546">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-1547">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1547">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="f5a7e-1548">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1548">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="f5a7e-1549">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1549">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="f5a7e-1550">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1550">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="f5a7e-1551">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1551">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-1552">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1552">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-1553">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1553">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="f5a7e-1554">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1554">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="f5a7e-1555">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1555">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="f5a7e-1556">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1556">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="f5a7e-1557">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1557">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="f5a7e-1558">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1558">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="f5a7e-1559">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1559">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="f5a7e-1560">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1560">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f5a7e-1561">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1561">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f5a7e-1562">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1562">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f5a7e-1563">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1563">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-1564">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1564">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-1565">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1565">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="f5a7e-1566">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1566">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="f5a7e-1567">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1567">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="f5a7e-1568">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1568">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="f5a7e-1569">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1569">General</span></span>
* <span data-ttu-id="f5a7e-1570">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1570">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-1571">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1571">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-1572">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1572">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5a7e-1573">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1573">Az.Aks</span></span>
* <span data-ttu-id="f5a7e-1574">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1574">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="f5a7e-1575">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1575">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5a7e-1576">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1576">Az.ApiManagement</span></span>
* <span data-ttu-id="f5a7e-1577">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1577">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="f5a7e-1578">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1578">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="f5a7e-1579">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1579">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="f5a7e-1580">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1580">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="f5a7e-1581">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1581">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f5a7e-1582">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1582">Az.Batch</span></span>
* <span data-ttu-id="f5a7e-1583">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1583">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f5a7e-1584">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1584">Az.Cdn</span></span>
* <span data-ttu-id="f5a7e-1585">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1585">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-1586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1586">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-1587">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1587">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="f5a7e-1588">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1588">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="f5a7e-1589">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1589">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="f5a7e-1590">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1590">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="f5a7e-1591">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1591">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="f5a7e-1592">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1592">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="f5a7e-1593">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1593">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="f5a7e-1594">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1594">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-1595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1595">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-1596">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1596">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="f5a7e-1597">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1597">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="f5a7e-1598">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1598">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="f5a7e-1599">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1599">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5a7e-1600">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1600">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5a7e-1601">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1601">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5a7e-1602">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1602">Az.EventHub</span></span>
* <span data-ttu-id="f5a7e-1603">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1603">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="f5a7e-1604">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1604">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="f5a7e-1605">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1605">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="f5a7e-1606">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1606">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="f5a7e-1607">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1607">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f5a7e-1608">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1608">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5a7e-1609">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1609">Az.Monitor</span></span>
* <span data-ttu-id="f5a7e-1610">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1610">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-1611">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1611">Az.Network</span></span>
* <span data-ttu-id="f5a7e-1612">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1612">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="f5a7e-1613">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1613">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="f5a7e-1614">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1614">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="f5a7e-1615">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1615">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="f5a7e-1616">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1616">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="f5a7e-1617">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1617">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="f5a7e-1618">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1618">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5a7e-1619">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1619">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5a7e-1620">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1620">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="f5a7e-1621">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1621">Added example</span></span>
    - <span data-ttu-id="f5a7e-1622">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1622">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="f5a7e-1623">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1623">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="f5a7e-1624">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1624">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-1625">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1625">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-1626">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1626">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-1627">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1627">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-1628">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1628">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="f5a7e-1629">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1629">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="f5a7e-1630">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1630">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="f5a7e-1631">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1631">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f5a7e-1632">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1632">Az.ServiceBus</span></span>
* <span data-ttu-id="f5a7e-1633">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1633">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="f5a7e-1634">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1634">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="f5a7e-1635">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1635">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5a7e-1636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1636">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5a7e-1637">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1637">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="f5a7e-1638">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1638">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="f5a7e-1639">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1639">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="f5a7e-1640">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1640">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="f5a7e-1641">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1641">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="f5a7e-1642">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1642">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-1643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1643">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-1644">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1644">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-1645">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1645">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-1646">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1646">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="f5a7e-1647">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1647">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="f5a7e-1648">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1648">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="f5a7e-1649">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1649">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="f5a7e-1650">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1650">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="f5a7e-1651">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1651">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-1652">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1652">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-1653">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1653">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="f5a7e-1654">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1654">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-1655">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1655">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-1656">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1656">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="f5a7e-1657">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1657">Az.ApplicationInsights</span></span>
* <span data-ttu-id="f5a7e-1658">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1658">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5a7e-1659">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1659">Az.Automation</span></span>
* <span data-ttu-id="f5a7e-1660">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1660">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5a7e-1661">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1661">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5a7e-1662">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1662">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-1663">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1663">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-1664">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1664">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f5a7e-1665">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1665">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f5a7e-1666">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1666">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="f5a7e-1667">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1667">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-1668">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1668">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-1669">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1669">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="f5a7e-1670">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1670">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5a7e-1671">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1671">Az.EventHub</span></span>
* <span data-ttu-id="f5a7e-1672">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1672">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f5a7e-1673">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1673">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5a7e-1674">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1674">Az.KeyVault</span></span>
* <span data-ttu-id="f5a7e-1675">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1675">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f5a7e-1676">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1676">Az.LogicApp</span></span>
* <span data-ttu-id="f5a7e-1677">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1677">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="f5a7e-1678">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1678">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="f5a7e-1679">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1679">Az.ManagedServices</span></span>
* <span data-ttu-id="f5a7e-1680">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1680">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1681">Az.Network</span></span>
* <span data-ttu-id="f5a7e-1682">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1682">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="f5a7e-1683">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1683">New cmdlets</span></span>
        - <span data-ttu-id="f5a7e-1684">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1684">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f5a7e-1685">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1685">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f5a7e-1686">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1686">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5a7e-1687">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1687">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5a7e-1688">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1688">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5a7e-1689">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1689">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f5a7e-1690">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1690">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="f5a7e-1691">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1691">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="f5a7e-1692">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1692">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="f5a7e-1693">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1693">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="f5a7e-1694">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1694">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="f5a7e-1695">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1695">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="f5a7e-1696">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1696">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="f5a7e-1697">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1697">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="f5a7e-1698">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1698">Updated cmdlets</span></span>
        - <span data-ttu-id="f5a7e-1699">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1699">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f5a7e-1700">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1700">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f5a7e-1701">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1701">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f5a7e-1702">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1702">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f5a7e-1703">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1703">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="f5a7e-1704">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1704">Updated cmdlet:</span></span>
        - <span data-ttu-id="f5a7e-1705">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1705">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f5a7e-1706">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1706">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f5a7e-1707">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1707">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="f5a7e-1708">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1708">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="f5a7e-1709">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1709">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="f5a7e-1710">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1710">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5a7e-1711">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1711">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5a7e-1712">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1712">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="f5a7e-1713">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1713">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-1714">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1714">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-1715">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1715">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f5a7e-1716">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1716">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="f5a7e-1717">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1717">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="f5a7e-1718">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1718">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f5a7e-1719">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1719">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="f5a7e-1720">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1720">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f5a7e-1721">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1721">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="f5a7e-1722">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1722">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f5a7e-1723">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1723">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="f5a7e-1724">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1724">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1725">Az.Resources</span></span>
- <span data-ttu-id="f5a7e-1726">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1726">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="f5a7e-1727">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1727">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f5a7e-1728">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1728">Az.ServiceBus</span></span>
* <span data-ttu-id="f5a7e-1729">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1729">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f5a7e-1730">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1730">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-1731">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1731">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-1732">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1732">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="f5a7e-1733">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1733">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="f5a7e-1734">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1734">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1735">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-1736">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1736">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f5a7e-1737">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1737">Az.StorageSync</span></span>
* <span data-ttu-id="f5a7e-1738">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1738">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="f5a7e-1739">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1739">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-1740">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1740">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-1741">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1741">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="f5a7e-1742">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1742">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="f5a7e-1743">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1743">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="f5a7e-1744">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1744">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-1745">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1745">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-1746">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1746">Add support for profile cmdlets</span></span>
* <span data-ttu-id="f5a7e-1747">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1747">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="f5a7e-1748">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1748">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f5a7e-1749">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1749">Az.Advisor</span></span>
* <span data-ttu-id="f5a7e-1750">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1750">GA release of Az.Advisor</span></span>
* <span data-ttu-id="f5a7e-1751">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1751">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f5a7e-1752">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1752">Az.ApiManagement</span></span>
* <span data-ttu-id="f5a7e-1753">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1753">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="f5a7e-1754">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1754">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="f5a7e-1755">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1755">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="f5a7e-1756">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1756">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="f5a7e-1757">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1757">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="f5a7e-1758">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1758">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="f5a7e-1759">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1759">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5a7e-1760">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1760">Az.Automation</span></span>
* <span data-ttu-id="f5a7e-1761">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1761">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-1762">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1762">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-1763">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1763">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-1764">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1764">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-1765">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1765">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f5a7e-1766">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1766">Az.EventGrid</span></span>
* <span data-ttu-id="f5a7e-1767">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1767">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5a7e-1768">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1768">Az.IotHub</span></span>
* <span data-ttu-id="f5a7e-1769">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1769">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-1770">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1770">Az.Network</span></span>
* <span data-ttu-id="f5a7e-1771">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1771">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="f5a7e-1772">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1772">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5a7e-1773">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1773">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5a7e-1774">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1774">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="f5a7e-1775">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1775">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5a7e-1776">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1776">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5a7e-1777">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1777">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-1778">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1778">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-1779">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1779">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-1780">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1780">Az.Resources</span></span>
    - <span data-ttu-id="f5a7e-1781">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1781">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="f5a7e-1782">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1782">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="f5a7e-1783">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1783">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="f5a7e-1784">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1784">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f5a7e-1785">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1785">Az.ServiceBus</span></span>
* <span data-ttu-id="f5a7e-1786">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1786">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-1787">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1787">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-1788">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1788">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="f5a7e-1789">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1789">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="f5a7e-1790">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1790">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f5a7e-1791">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1791">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f5a7e-1792">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1792">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f5a7e-1793">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1793">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f5a7e-1794">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1794">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f5a7e-1795">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1795">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="f5a7e-1796">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1796">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-1797">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1797">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-1798">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1798">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="f5a7e-1799">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1799">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="f5a7e-1800">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1800">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="f5a7e-1801">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1801">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="f5a7e-1802">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1802">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="f5a7e-1803">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1803">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f5a7e-1804">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1804">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f5a7e-1805">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1805">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="f5a7e-1806">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1806">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="f5a7e-1807">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1807">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f5a7e-1808">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1808">Az.StorageSync</span></span>
* <span data-ttu-id="f5a7e-1809">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1809">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="f5a7e-1810">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1810">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-1811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1811">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-1812">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1812">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="f5a7e-1813">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1813">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="f5a7e-1814">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1814">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="f5a7e-1815">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1815">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="f5a7e-1816">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1816">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1817">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-1818">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1818">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="f5a7e-1819">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1819">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="f5a7e-1820">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1820">Az.Dns</span></span>
* <span data-ttu-id="f5a7e-1821">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1821">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f5a7e-1822">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1822">Az.EventGrid</span></span>
* <span data-ttu-id="f5a7e-1823">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1823">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="f5a7e-1824">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1824">New cmdlets:</span></span>
    - <span data-ttu-id="f5a7e-1825">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1825">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f5a7e-1826">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1826">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f5a7e-1827">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1827">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f5a7e-1828">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1828">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="f5a7e-1829">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1829">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f5a7e-1830">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1830">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f5a7e-1831">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1831">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f5a7e-1832">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1832">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f5a7e-1833">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1833">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f5a7e-1834">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1834">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="f5a7e-1835">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1835">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f5a7e-1836">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1836">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="f5a7e-1837">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1837">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="f5a7e-1838">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1838">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="f5a7e-1839">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1839">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f5a7e-1840">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1840">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="f5a7e-1841">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1841">Updated cmdlets:</span></span>
    - <span data-ttu-id="f5a7e-1842">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1842">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="f5a7e-1843">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1843">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f5a7e-1844">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1844">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f5a7e-1845">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1845">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="f5a7e-1846">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1846">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="f5a7e-1847">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1847">Event subscription expiration date,</span></span>
            - <span data-ttu-id="f5a7e-1848">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1848">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="f5a7e-1849">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1849">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="f5a7e-1850">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1850">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="f5a7e-1851">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1851">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="f5a7e-1852">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1852">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="f5a7e-1853">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1853">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="f5a7e-1854">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1854">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="f5a7e-1855">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1855">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5a7e-1856">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1856">Az.FrontDoor</span></span>
* <span data-ttu-id="f5a7e-1857">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1857">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="f5a7e-1858">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1858">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="f5a7e-1859">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1859">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="f5a7e-1860">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1860">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-1861">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1861">Az.Network</span></span>
* <span data-ttu-id="f5a7e-1862">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1862">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="f5a7e-1863">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1863">New cmdlets</span></span>
        - <span data-ttu-id="f5a7e-1864">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1864">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="f5a7e-1865">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1865">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="f5a7e-1866">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1866">New cmdlets</span></span>
        - <span data-ttu-id="f5a7e-1867">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1867">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="f5a7e-1868">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1868">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="f5a7e-1869">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1869">New cmdlets</span></span>
        - <span data-ttu-id="f5a7e-1870">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1870">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f5a7e-1871">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1871">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f5a7e-1872">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1872">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f5a7e-1873">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1873">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="f5a7e-1874">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1874">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f5a7e-1875">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1875">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="f5a7e-1876">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1876">New cmdlets</span></span>
        - <span data-ttu-id="f5a7e-1877">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1877">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f5a7e-1878">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1878">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f5a7e-1879">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1879">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f5a7e-1880">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1880">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="f5a7e-1881">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1881">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="f5a7e-1882">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1882">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="f5a7e-1883">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1883">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="f5a7e-1884">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1884">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="f5a7e-1885">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1885">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="f5a7e-1886">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1886">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="f5a7e-1887">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1887">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="f5a7e-1888">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1888">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="f5a7e-1889">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1889">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="f5a7e-1890">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1890">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="f5a7e-1891">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1891">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="f5a7e-1892">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1892">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="f5a7e-1893">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1893">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="f5a7e-1894">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1894">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="f5a7e-1895">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1895">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f5a7e-1896">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1896">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="f5a7e-1897">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1897">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="f5a7e-1898">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1898">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="f5a7e-1899">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1899">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="f5a7e-1900">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1900">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="f5a7e-1901">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1901">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f5a7e-1902">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1902">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f5a7e-1903">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1903">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5a7e-1904">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1904">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5a7e-1905">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1905">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-1906">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1906">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-1907">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1907">Support for additional Template Export options</span></span>
    - <span data-ttu-id="f5a7e-1908">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1908">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f5a7e-1909">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1909">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f5a7e-1910">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1910">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5a7e-1911">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1911">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5a7e-1912">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1912">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1913">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-1914">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1914">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="f5a7e-1915">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1915">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="f5a7e-1916">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1916">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="f5a7e-1917">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1917">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f5a7e-1918">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1918">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f5a7e-1919">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1919">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f5a7e-1920">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1920">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="f5a7e-1921">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1921">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-1922">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1922">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-1923">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1923">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="f5a7e-1924">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1924">New-AzStorageAccount</span></span>
* <span data-ttu-id="f5a7e-1925">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1925">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="f5a7e-1926">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1926">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-1927">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1927">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-1928">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1928">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="f5a7e-1929">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1929">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="f5a7e-1930">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1930">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="f5a7e-1931">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1931">Az.Cdn</span></span>
* <span data-ttu-id="f5a7e-1932">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1932">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-1933">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1933">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-1934">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1934">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="f5a7e-1935">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1935">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5a7e-1936">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1936">Az.EventHub</span></span>
* <span data-ttu-id="f5a7e-1937">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1937">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="f5a7e-1938">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1938">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-1939">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1939">Az.Network</span></span>
* <span data-ttu-id="f5a7e-1940">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1940">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="f5a7e-1941">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1941">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5a7e-1942">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1942">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5a7e-1943">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1943">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-1944">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1944">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-1945">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1945">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f5a7e-1946">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1946">Az.ServiceBus</span></span>
* <span data-ttu-id="f5a7e-1947">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1947">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5a7e-1948">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1948">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5a7e-1949">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1949">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="f5a7e-1950">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1950">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-1951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1951">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-1952">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1952">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="f5a7e-1953">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1953">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f5a7e-1954">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1954">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="f5a7e-1955">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1955">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1956">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-1957">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1957">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="f5a7e-1958">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1958">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f5a7e-1959">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1959">Az.ApiManagement</span></span>
* <span data-ttu-id="f5a7e-1960">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1960">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="f5a7e-1961">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1961">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="f5a7e-1962">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1962">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="f5a7e-1963">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1963">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="f5a7e-1964">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1964">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="f5a7e-1965">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1965">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="f5a7e-1966">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1966">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="f5a7e-1967">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1967">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="f5a7e-1968">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1968">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="f5a7e-1969">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1969">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="f5a7e-1970">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1970">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="f5a7e-1971">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1971">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="f5a7e-1972">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1972">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="f5a7e-1973">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1973">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="f5a7e-1974">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1974">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="f5a7e-1975">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1975">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="f5a7e-1976">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1976">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="f5a7e-1977">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1977">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="f5a7e-1978">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1978">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="f5a7e-1979">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1979">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="f5a7e-1980">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1980">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="f5a7e-1981">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1981">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="f5a7e-1982">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1982">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="f5a7e-1983">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1983">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="f5a7e-1984">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1984">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="f5a7e-1985">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1985">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="f5a7e-1986">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1986">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="f5a7e-1987">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1987">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="f5a7e-1988">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1988">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="f5a7e-1989">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1989">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="f5a7e-1990">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1990">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="f5a7e-1991">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1991">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="f5a7e-1992">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1992">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="f5a7e-1993">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1993">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f5a7e-1994">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1994">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="f5a7e-1995">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1995">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="f5a7e-1996">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1996">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="f5a7e-1997">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1997">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="f5a7e-1998">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1998">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="f5a7e-1999">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-1999">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f5a7e-2000">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2000">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f5a7e-2001">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2001">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f5a7e-2002">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2002">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="f5a7e-2003">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2003">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f5a7e-2004">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2004">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f5a7e-2005">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2005">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f5a7e-2006">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2006">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f5a7e-2007">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2007">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f5a7e-2008">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2008">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="f5a7e-2009">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2009">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="f5a7e-2010">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2010">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="f5a7e-2011">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2011">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="f5a7e-2012">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2012">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="f5a7e-2013">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2013">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="f5a7e-2014">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2014">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="f5a7e-2015">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2015">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="f5a7e-2016">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2016">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f5a7e-2017">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2017">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f5a7e-2018">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2018">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f5a7e-2019">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2019">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f5a7e-2020">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2020">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f5a7e-2021">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2021">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f5a7e-2022">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2022">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f5a7e-2023">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2023">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f5a7e-2024">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2024">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="f5a7e-2025">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2025">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="f5a7e-2026">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2026">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="f5a7e-2027">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2027">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="f5a7e-2028">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2028">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="f5a7e-2029">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2029">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="f5a7e-2030">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2030">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="f5a7e-2031">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2031">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="f5a7e-2032">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2032">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="f5a7e-2033">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2033">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="f5a7e-2034">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2034">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="f5a7e-2035">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2035">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="f5a7e-2036">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2036">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5a7e-2037">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2037">Az.Automation</span></span>
* <span data-ttu-id="f5a7e-2038">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2038">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="f5a7e-2039">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2039">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="f5a7e-2040">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2040">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="f5a7e-2041">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2041">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="f5a7e-2042">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2042">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="f5a7e-2043">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2043">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="f5a7e-2044">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2044">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-2045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2045">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-2046">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2046">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="f5a7e-2047">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2047">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5a7e-2048">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2048">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5a7e-2049">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2049">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5a7e-2050">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2050">Az.Monitor</span></span>
* <span data-ttu-id="f5a7e-2051">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2051">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-2052">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2052">Az.Network</span></span>
* <span data-ttu-id="f5a7e-2053">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2053">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="f5a7e-2054">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2054">Updated cmdlet:</span></span>
        - <span data-ttu-id="f5a7e-2055">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2055">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="f5a7e-2056">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2056">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-2057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2057">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-2058">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2058">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-2059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2059">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-2060">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2060">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="f5a7e-2061">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2061">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-2062">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2062">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-2063">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2063">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5a7e-2064">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2064">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5a7e-2065">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2065">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="f5a7e-2066">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2066">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2067">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-2068">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2068">Proximity placement group feature.</span></span>
    - <span data-ttu-id="f5a7e-2069">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2069">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="f5a7e-2070">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2070">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="f5a7e-2071">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2071">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="f5a7e-2072">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2072">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="f5a7e-2073">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2073">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="f5a7e-2074">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2074">Breaking changes</span></span>
    - <span data-ttu-id="f5a7e-2075">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2075">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="f5a7e-2076">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2076">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f5a7e-2077">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2077">Az.DeploymentManager</span></span>
* <span data-ttu-id="f5a7e-2078">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2078">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="f5a7e-2079">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2079">Az.Dns</span></span>
* <span data-ttu-id="f5a7e-2080">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2080">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="f5a7e-2081">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2081">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="f5a7e-2082">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2082">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f5a7e-2083">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2083">Az.FrontDoor</span></span>
* <span data-ttu-id="f5a7e-2084">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2084">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="f5a7e-2085">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2085">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="f5a7e-2086">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2086">Az.HDInsight</span></span>
* <span data-ttu-id="f5a7e-2087">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2087">Removed two cmdlets:</span></span>
    - <span data-ttu-id="f5a7e-2088">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2088">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="f5a7e-2089">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2089">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f5a7e-2090">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2090">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f5a7e-2091">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2091">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="f5a7e-2092">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2092">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="f5a7e-2093">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2093">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5a7e-2094">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2094">Az.Monitor</span></span>
* <span data-ttu-id="f5a7e-2095">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2095">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="f5a7e-2096">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2096">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="f5a7e-2097">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2097">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="f5a7e-2098">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2098">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="f5a7e-2099">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2099">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="f5a7e-2100">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2100">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="f5a7e-2101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2101">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="f5a7e-2102">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2102">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f5a7e-2103">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2103">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f5a7e-2104">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2104">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f5a7e-2105">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2105">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f5a7e-2106">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2106">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f5a7e-2107">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2107">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="f5a7e-2108">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2108">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-2109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2109">Az.Network</span></span>
* <span data-ttu-id="f5a7e-2110">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2110">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="f5a7e-2111">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2111">New cmdlets</span></span>
        - <span data-ttu-id="f5a7e-2112">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2112">New-AzNatGateway</span></span>
        - <span data-ttu-id="f5a7e-2113">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2113">Get-AzNatGateway</span></span>
        - <span data-ttu-id="f5a7e-2114">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2114">Set-AzNatGateway</span></span>
        - <span data-ttu-id="f5a7e-2115">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2115">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="f5a7e-2116">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2116">Updated cmdlets</span></span>
        - <span data-ttu-id="f5a7e-2117">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2117">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="f5a7e-2118">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2118">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="f5a7e-2119">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2119">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="f5a7e-2120">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2120">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="f5a7e-2121">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2121">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5a7e-2122">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2122">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5a7e-2123">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2123">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="f5a7e-2124">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2124">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="f5a7e-2125">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2125">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-2126">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2126">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-2127">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2127">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="f5a7e-2128">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2128">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="f5a7e-2129">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2129">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="f5a7e-2130">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2130">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="f5a7e-2131">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2131">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="f5a7e-2132">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2132">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="f5a7e-2133">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2133">Az.Relay</span></span>
* <span data-ttu-id="f5a7e-2134">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2134">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f5a7e-2135">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2135">Az.ServiceBus</span></span>
* <span data-ttu-id="f5a7e-2136">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2136">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-2137">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2137">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-2138">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2138">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="f5a7e-2139">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2139">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="f5a7e-2140">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2140">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="f5a7e-2141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2141">New-AzStorageAccount</span></span>
* <span data-ttu-id="f5a7e-2142">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2142">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="f5a7e-2143">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2143">New-AzStorageAccount</span></span>
    - <span data-ttu-id="f5a7e-2144">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2144">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="f5a7e-2145">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2145">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-2146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2146">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-2147">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2147">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="f5a7e-2148">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2148">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="f5a7e-2149">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2149">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f5a7e-2150">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2150">Highlights since the last major release</span></span>
* <span data-ttu-id="f5a7e-2151">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2151">General availability of `Az` module</span></span>
* <span data-ttu-id="f5a7e-2152">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f5a7e-2153">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f5a7e-2154">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f5a7e-2155">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f5a7e-2156">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f5a7e-2157">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-2158">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2158">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-2159">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2159">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f5a7e-2160">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2160">Az.Batch</span></span>
* <span data-ttu-id="f5a7e-2161">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f5a7e-2162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2162">Az.Cdn</span></span>
* <span data-ttu-id="f5a7e-2163">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2163">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5a7e-2164">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2164">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5a7e-2165">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2165">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-2166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2166">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-2167">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2167">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="f5a7e-2168">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2168">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f5a7e-2169">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2169">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-2170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2170">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-2171">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2171">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5a7e-2172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2172">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5a7e-2173">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2173">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f5a7e-2174">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2174">Az.EventGrid</span></span>
* <span data-ttu-id="f5a7e-2175">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2175">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5a7e-2176">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2176">Az.EventHub</span></span>
* <span data-ttu-id="f5a7e-2177">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2177">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f5a7e-2178">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2178">Az.HDInsight</span></span>
* <span data-ttu-id="f5a7e-2179">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5a7e-2180">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2180">Az.IotHub</span></span>
* <span data-ttu-id="f5a7e-2181">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2181">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5a7e-2182">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2182">Az.KeyVault</span></span>
* <span data-ttu-id="f5a7e-2183">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2183">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f5a7e-2184">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2184">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f5a7e-2185">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2185">Az.MachineLearning</span></span>
* <span data-ttu-id="f5a7e-2186">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2186">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="f5a7e-2187">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2187">Az.Media</span></span>
* <span data-ttu-id="f5a7e-2188">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2188">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5a7e-2189">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2189">Az.Monitor</span></span>
  * <span data-ttu-id="f5a7e-2190">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2190">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="f5a7e-2191">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2191">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="f5a7e-2192">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2192">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="f5a7e-2193">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2193">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f5a7e-2194">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2194">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f5a7e-2195">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2195">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="f5a7e-2196">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2196">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-2197">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2197">Az.Network</span></span>
* <span data-ttu-id="f5a7e-2198">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f5a7e-2199">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2199">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="f5a7e-2200">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2200">Az.NotificationHubs</span></span>
* <span data-ttu-id="f5a7e-2201">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5a7e-2202">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2202">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5a7e-2203">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f5a7e-2204">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2204">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f5a7e-2205">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-2206">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2206">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-2207">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2207">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f5a7e-2208">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2208">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="f5a7e-2209">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2209">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="f5a7e-2210">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2210">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f5a7e-2211">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2211">Az.RedisCache</span></span>
* <span data-ttu-id="f5a7e-2212">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2212">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-2213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2213">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-2214">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2214">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-2215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2215">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-2216">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2216">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="f5a7e-2217">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2217">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f5a7e-2218">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2218">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="f5a7e-2219">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2219">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="f5a7e-2220">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2220">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="f5a7e-2221">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2221">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="f5a7e-2222">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2222">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-2223">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2223">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-2224">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2224">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="f5a7e-2225">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2225">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f5a7e-2226">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2226">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="f5a7e-2227">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2227">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="f5a7e-2228">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2228">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f5a7e-2229">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2229">Highlights since the last major release</span></span>
* <span data-ttu-id="f5a7e-2230">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2230">General availability of `Az` module</span></span>
* <span data-ttu-id="f5a7e-2231">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f5a7e-2232">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f5a7e-2233">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f5a7e-2234">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f5a7e-2235">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f5a7e-2236">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-2237">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2237">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-2238">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2238">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f5a7e-2239">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2239">Az.AnalysisServices</span></span>
* <span data-ttu-id="f5a7e-2240">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2240">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="f5a7e-2241">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2241">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5a7e-2242">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2242">Az.Automation</span></span>
* <span data-ttu-id="f5a7e-2243">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2243">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="f5a7e-2244">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2244">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="f5a7e-2245">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2245">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-2246">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2246">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-2247">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2247">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f5a7e-2248">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2248">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f5a7e-2249">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2249">Az.ContainerInstance</span></span>
* <span data-ttu-id="f5a7e-2250">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2250">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-2251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2251">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-2252">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2252">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="f5a7e-2253">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2253">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-2254">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2254">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-2255">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2255">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="f5a7e-2256">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2256">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f5a7e-2257">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2257">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="f5a7e-2258">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2258">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="f5a7e-2259">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2259">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="f5a7e-2260">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2260">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-2261">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2261">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-2262">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2262">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-2263">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2263">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-2264">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2264">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="f5a7e-2265">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2265">New-AzStorageContext</span></span>
* <span data-ttu-id="f5a7e-2266">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2266">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="f5a7e-2267">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2267">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f5a7e-2268">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2268">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f5a7e-2269">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2269">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="f5a7e-2270">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2270">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="f5a7e-2271">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2271">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="f5a7e-2272">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2272">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f5a7e-2273">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2273">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f5a7e-2274">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2274">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="f5a7e-2275">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2275">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="f5a7e-2276">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2276">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f5a7e-2277">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2277">Highlights since the last major release</span></span>
* <span data-ttu-id="f5a7e-2278">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2278">General availability of `Az` module</span></span>
* <span data-ttu-id="f5a7e-2279">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2279">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f5a7e-2280">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2280">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f5a7e-2281">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2281">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f5a7e-2282">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2282">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f5a7e-2283">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2283">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f5a7e-2284">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2284">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5a7e-2285">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2285">Az.Automation</span></span>
* <span data-ttu-id="f5a7e-2286">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2286">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="f5a7e-2287">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2287">Dynamic grouping</span></span>
    * <span data-ttu-id="f5a7e-2288">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2288">Pre-Post script</span></span>
    * <span data-ttu-id="f5a7e-2289">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2289">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-2290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2290">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-2291">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2291">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="f5a7e-2292">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2292">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5a7e-2293">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2293">Az.KeyVault</span></span>
* <span data-ttu-id="f5a7e-2294">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2294">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-2295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2295">Az.Network</span></span>
* <span data-ttu-id="f5a7e-2296">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2296">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="f5a7e-2297">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2297">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-2298">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2298">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-2299">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2299">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="f5a7e-2300">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2300">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-2301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2301">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-2302">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2302">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="f5a7e-2303">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2303">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-2304">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2304">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-2305">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2305">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-2306">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2306">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-2307">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2307">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="f5a7e-2308">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2308">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f5a7e-2309">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2309">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f5a7e-2310">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2310">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f5a7e-2311">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2311">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="f5a7e-2312">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2312">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="f5a7e-2313">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2313">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-2314">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2314">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-2315">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2315">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="f5a7e-2316">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2316">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-2317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2317">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-2318">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2318">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="f5a7e-2319">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2319">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5a7e-2320">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2320">Az.Automation</span></span>
* <span data-ttu-id="f5a7e-2321">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2321">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="f5a7e-2322">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2322">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="f5a7e-2323">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2323">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f5a7e-2324">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2324">Az.Cdn</span></span>
* <span data-ttu-id="f5a7e-2325">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2325">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-2326">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2326">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-2327">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2327">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-2328">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2328">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-2329">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2329">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f5a7e-2330">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2330">Az.LogicApp</span></span>
* <span data-ttu-id="f5a7e-2331">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2331">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-2332">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2332">Az.Network</span></span>
* <span data-ttu-id="f5a7e-2333">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2333">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-2334">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2334">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-2335">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2335">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="f5a7e-2336">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2336">SDK Update</span></span>
* <span data-ttu-id="f5a7e-2337">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2337">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="f5a7e-2338">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2338">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-2339">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2339">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-2340">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2340">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="f5a7e-2341">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2341">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="f5a7e-2342">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2342">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="f5a7e-2343">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2343">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="f5a7e-2344">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2344">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="f5a7e-2345">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2345">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-2346">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2346">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-2347">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2347">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="f5a7e-2348">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2348">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-2349">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2349">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-2350">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2350">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="f5a7e-2351">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2351">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="f5a7e-2352">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2352">Az.AnalysisServices</span></span>
* <span data-ttu-id="f5a7e-2353">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2353">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5a7e-2354">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2354">Az.Automation</span></span>
* <span data-ttu-id="f5a7e-2355">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2355">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="f5a7e-2356">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2356">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="f5a7e-2357">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2357">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5a7e-2358">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2358">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5a7e-2359">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2359">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-2360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2360">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-2361">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2361">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="f5a7e-2362">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2362">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="f5a7e-2363">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2363">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="f5a7e-2364">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2364">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5a7e-2365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2365">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5a7e-2366">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2366">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f5a7e-2367">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2367">Az.EventHub</span></span>
* <span data-ttu-id="f5a7e-2368">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2368">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5a7e-2369">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2369">Az.KeyVault</span></span>
* <span data-ttu-id="f5a7e-2370">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2370">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f5a7e-2371">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2371">Az.LogicApp</span></span>
* <span data-ttu-id="f5a7e-2372">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2372">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="f5a7e-2373">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2373">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="f5a7e-2374">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2374">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="f5a7e-2375">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2375">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f5a7e-2376">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2376">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f5a7e-2377">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2377">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f5a7e-2378">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2378">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="f5a7e-2379">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2379">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="f5a7e-2380">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2380">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f5a7e-2381">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2381">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f5a7e-2382">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2382">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f5a7e-2383">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2383">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="f5a7e-2384">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2384">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f5a7e-2385">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2385">Az.Monitor</span></span>
* <span data-ttu-id="f5a7e-2386">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2386">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-2387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2387">Az.Network</span></span>
* <span data-ttu-id="f5a7e-2388">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2388">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f5a7e-2389">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2389">Az.OperationalInsights</span></span>
* <span data-ttu-id="f5a7e-2390">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2390">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="f5a7e-2391">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2391">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="f5a7e-2392">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2392">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-2393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2393">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-2394">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2394">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f5a7e-2395">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2395">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="f5a7e-2396">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2396">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="f5a7e-2397">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2397">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-2398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2398">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-2399">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2399">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="f5a7e-2400">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2400">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-2401">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2401">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-2402">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2402">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="f5a7e-2403">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2403">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-2404">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2404">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-2405">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2405">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f5a7e-2406">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2406">Az.AnalysisServices</span></span>
<span data-ttu-id="f5a7e-2407">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2407">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-2408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2408">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-2409">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2409">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="f5a7e-2410">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2410">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="f5a7e-2411">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2411">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-2412">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2412">Az.RecoveryServices</span></span>
<span data-ttu-id="f5a7e-2413">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2413">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-2414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2414">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-2415">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2415">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="f5a7e-2416">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2416">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f5a7e-2417">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2417">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="f5a7e-2418">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2418">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-2419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2419">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-2420">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2420">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="f5a7e-2421">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2421">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="f5a7e-2422">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2422">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="f5a7e-2423">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2423">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-2424">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2424">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-2425">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2425">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f5a7e-2426">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2426">Az.AnalysisServices</span></span>
* <span data-ttu-id="f5a7e-2427">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2427">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-2428">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2428">Az.RecoveryServices</span></span>
* <span data-ttu-id="f5a7e-2429">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2429">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="f5a7e-2430">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2430">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-2431">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2431">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-2432">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2432">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f5a7e-2433">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f5a7e-2434">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2434">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="f5a7e-2435">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2435">Az.Aks</span></span>
* <span data-ttu-id="f5a7e-2436">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2436">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f5a7e-2437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2437">Az.Automation</span></span>
* <span data-ttu-id="f5a7e-2438">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2438">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="f5a7e-2439">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2439">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f5a7e-2440">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2440">Az.Cdn</span></span>
* <span data-ttu-id="f5a7e-2441">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2441">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-2442">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2442">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-2443">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2443">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="f5a7e-2444">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2444">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="f5a7e-2445">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2445">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f5a7e-2446">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2446">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f5a7e-2447">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2447">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f5a7e-2448">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2448">Az.DataFactory</span></span>
* <span data-ttu-id="f5a7e-2449">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2449">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5a7e-2450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2450">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5a7e-2451">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2451">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="f5a7e-2452">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2452">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="f5a7e-2453">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2453">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5a7e-2454">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2454">Az.IotHub</span></span>
* <span data-ttu-id="f5a7e-2455">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2455">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f5a7e-2456">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2456">Az.KeyVault</span></span>
* <span data-ttu-id="f5a7e-2457">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2457">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-2458">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2458">Az.Network</span></span>
* <span data-ttu-id="f5a7e-2459">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2459">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-2460">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2460">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-2461">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2461">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="f5a7e-2462">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2462">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="f5a7e-2463">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2463">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="f5a7e-2464">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2464">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="f5a7e-2465">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2465">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="f5a7e-2466">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2466">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="f5a7e-2467">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2467">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5a7e-2468">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2468">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5a7e-2469">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2469">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="f5a7e-2470">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2470">Fix some error messages.</span></span>
* <span data-ttu-id="f5a7e-2471">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2471">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="f5a7e-2472">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2472">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f5a7e-2473">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2473">Az.SignalR</span></span>
* <span data-ttu-id="f5a7e-2474">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2474">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-2475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2475">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-2476">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2476">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f5a7e-2477">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2477">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="f5a7e-2478">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2478">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="f5a7e-2479">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2479">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-2480">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2480">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-2481">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2481">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f5a7e-2482">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2482">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="f5a7e-2483">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2483">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="f5a7e-2484">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2484">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f5a7e-2485">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2485">Az.TrafficManager</span></span>
* <span data-ttu-id="f5a7e-2486">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2486">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-2487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2487">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-2488">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2488">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f5a7e-2489">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2489">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="f5a7e-2490">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2490">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="f5a7e-2491">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2491">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f5a7e-2492">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2492">Az.Accounts</span></span>
* <span data-ttu-id="f5a7e-2493">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2493">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-2494">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2494">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-2495">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2495">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="f5a7e-2496">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2496">Updated the description of ID in help files</span></span>
* <span data-ttu-id="f5a7e-2497">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2497">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5a7e-2498">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2498">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5a7e-2499">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2499">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="f5a7e-2500">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2500">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f5a7e-2501">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2501">Az.EventGrid</span></span>
* <span data-ttu-id="f5a7e-2502">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2502">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="f5a7e-2503">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2503">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="f5a7e-2504">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2504">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f5a7e-2505">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2505">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f5a7e-2506">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2506">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f5a7e-2507">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2507">Dead letter endpoint.</span></span>
    - <span data-ttu-id="f5a7e-2508">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2508">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f5a7e-2509">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2509">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f5a7e-2510">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2510">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f5a7e-2511">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2511">Dead letter endpoint.</span></span>
* <span data-ttu-id="f5a7e-2512">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2512">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="f5a7e-2513">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2513">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f5a7e-2514">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2514">Az.IotHub</span></span>
* <span data-ttu-id="f5a7e-2515">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2515">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f5a7e-2516">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2516">Az.LogicApp</span></span>
* <span data-ttu-id="f5a7e-2517">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2517">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-2518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2518">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-2519">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2519">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="f5a7e-2520">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2520">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="f5a7e-2521">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2521">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f5a7e-2522">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2522">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="f5a7e-2523">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2523">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="f5a7e-2524">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2524">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f5a7e-2525">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2525">Az.SignalR</span></span>
* <span data-ttu-id="f5a7e-2526">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2526">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-2527">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2527">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-2528">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2528">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f5a7e-2529">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2529">Az.Storage</span></span>
* <span data-ttu-id="f5a7e-2530">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2530">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="f5a7e-2531">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2531">New-AzStorageContext</span></span>
* <span data-ttu-id="f5a7e-2532">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2532">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="f5a7e-2533">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2533">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-2534">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2534">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-2535">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2535">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f5a7e-2536">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2536">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="f5a7e-2537">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2537">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f5a7e-2538">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2538">General</span></span>

- <span data-ttu-id="f5a7e-2539">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2539">General Availability of Az Module</span></span>
- <span data-ttu-id="f5a7e-2540">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2540">Online help for each module</span></span>
- <span data-ttu-id="f5a7e-2541">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2541">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f5a7e-2542">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2542">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f5a7e-2543">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2543">Az.Accounts</span></span>
- <span data-ttu-id="f5a7e-2544">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2544">Changed from Az.Profile</span></span>
- <span data-ttu-id="f5a7e-2545">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2545">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f5a7e-2546">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2546">Az.ApiManagement</span></span>
- <span data-ttu-id="f5a7e-2547">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2547">Fixes for #7002</span></span>
- <span data-ttu-id="f5a7e-2548">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2548">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f5a7e-2549">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2549">Az.Batch</span></span>
- <span data-ttu-id="f5a7e-2550">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2550">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f5a7e-2551">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2551">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f5a7e-2552">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f5a7e-2553">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2553">Az.Billing</span></span>
- <span data-ttu-id="f5a7e-2554">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2554">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f5a7e-2555">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2555">Az.CognitivServices</span></span>
- <span data-ttu-id="f5a7e-2556">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2556">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f5a7e-2557">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2557">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f5a7e-2558">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2558">Az.ContainerInstance</span></span>
- <span data-ttu-id="f5a7e-2559">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2559">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f5a7e-2560">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2560">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f5a7e-2561">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2561">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f5a7e-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2562">Az.DataLakeStore</span></span>
- <span data-ttu-id="f5a7e-2563">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2563">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f5a7e-2564">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2564">Az.Monitor</span></span>
- <span data-ttu-id="f5a7e-2565">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2565">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f5a7e-2566">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2566">Az.KeyVault</span></span>
- <span data-ttu-id="f5a7e-2567">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2567">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f5a7e-2568">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2568">Az.MachineLearning</span></span>
- <span data-ttu-id="f5a7e-2569">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2569">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f5a7e-2570">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2570">Az.Media</span></span>
- <span data-ttu-id="f5a7e-2571">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2571">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f5a7e-2572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2572">Az.Network</span></span>
<span data-ttu-id="f5a7e-2573">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2573">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f5a7e-2574">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2574">New cmdlets added:</span></span>
        - <span data-ttu-id="f5a7e-2575">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2575">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f5a7e-2576">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2576">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f5a7e-2577">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2577">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f5a7e-2578">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2578">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f5a7e-2579">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2579">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f5a7e-2580">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2580">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f5a7e-2581">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2581">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f5a7e-2582">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2582">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f5a7e-2583">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2583">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f5a7e-2584">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2584">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f5a7e-2585">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2585">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f5a7e-2586">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2586">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f5a7e-2587">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2587">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f5a7e-2588">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2588">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f5a7e-2589">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2589">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f5a7e-2590">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2590">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f5a7e-2591">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2591">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f5a7e-2592">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2592">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f5a7e-2593">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2593">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f5a7e-2594">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2594">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f5a7e-2595">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2595">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f5a7e-2596">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2596">Az.OperationalInsights</span></span>
- <span data-ttu-id="f5a7e-2597">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2597">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f5a7e-2598">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2598">Az.Profile</span></span>
- <span data-ttu-id="f5a7e-2599">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2599">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-2600">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2600">Az.RecoveryServices</span></span>
- <span data-ttu-id="f5a7e-2601">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f5a7e-2602">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2602">Az.Resources</span></span>
- <span data-ttu-id="f5a7e-2603">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f5a7e-2604">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2604">Az.ServiceFabric</span></span>
- <span data-ttu-id="f5a7e-2605">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2605">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f5a7e-2606">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2606">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f5a7e-2607">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2607">Az.SIgnalR</span></span>
- <span data-ttu-id="f5a7e-2608">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2608">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f5a7e-2609">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2609">Az.Sql</span></span>
- <span data-ttu-id="f5a7e-2610">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2610">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f5a7e-2611">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2611">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f5a7e-2612">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2612">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f5a7e-2613">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2613">Az.Storage</span></span>
- <span data-ttu-id="f5a7e-2614">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2614">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f5a7e-2615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2615">Az.Websites</span></span>
- <span data-ttu-id="f5a7e-2616">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2616">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f5a7e-2617">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2617">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f5a7e-2618">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2618">General</span></span>

* <span data-ttu-id="f5a7e-2619">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2619">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f5a7e-2620">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2620">Az.Compute</span></span>

* <span data-ttu-id="f5a7e-2621">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2621">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f5a7e-2622">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2622">Az.DataLakeStore</span></span>

* <span data-ttu-id="f5a7e-2623">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2623">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f5a7e-2624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2624">Az.FrontDoor</span></span>

* <span data-ttu-id="f5a7e-2625">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2625">Fixed some broken links</span></span>
    - <span data-ttu-id="f5a7e-2626">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2626">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f5a7e-2627">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2627">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f5a7e-2628">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2628">Az.RecoveryServices</span></span>

* <span data-ttu-id="f5a7e-2629">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2629">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f5a7e-2630">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2630">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f5a7e-2631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2631">Az.Resources</span></span>

* <span data-ttu-id="f5a7e-2632">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2632">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f5a7e-2633">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2633">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f5a7e-2634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2634">Az.Sql</span></span>

* <span data-ttu-id="f5a7e-2635">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2635">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f5a7e-2636">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2636">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f5a7e-2637">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2637">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f5a7e-2638">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2638">Az.Storage</span></span>

* <span data-ttu-id="f5a7e-2639">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2639">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f5a7e-2640">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2640">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f5a7e-2641">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2641">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f5a7e-2642">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2642">Support Static Website configuration</span></span>
    - <span data-ttu-id="f5a7e-2643">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2643">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f5a7e-2644">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2644">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f5a7e-2645">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2645">Az.Websites</span></span>

* <span data-ttu-id="f5a7e-2646">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2646">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="f5a7e-2647">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2647">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f5a7e-2648">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2648">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f5a7e-2649">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2649">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f5a7e-2650">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2650">Az.ApiManagement</span></span>
* <span data-ttu-id="f5a7e-2651">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2651">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f5a7e-2652">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2652">Az.Automation</span></span>
* <span data-ttu-id="f5a7e-2653">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2653">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f5a7e-2654">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2654">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f5a7e-2655">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2655">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f5a7e-2656">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2656">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f5a7e-2657">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2657">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f5a7e-2658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2658">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-2659">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2659">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f5a7e-2660">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2660">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f5a7e-2661">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2661">Az.ContainerInstance</span></span>
* <span data-ttu-id="f5a7e-2662">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2662">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f5a7e-2663">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2663">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f5a7e-2664">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2664">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f5a7e-2665">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2665">Az.Network</span></span>
* <span data-ttu-id="f5a7e-2666">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2666">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f5a7e-2667">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2667">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f5a7e-2668">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2668">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="f5a7e-2669">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2669">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f5a7e-2670">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2670">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f5a7e-2671">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2671">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f5a7e-2672">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2672">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f5a7e-2673">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2673">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f5a7e-2674">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2674">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f5a7e-2675">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2675">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f5a7e-2676">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2676">Az.Relay</span></span>
* <span data-ttu-id="f5a7e-2677">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2677">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f5a7e-2678">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2678">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-2679">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2679">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f5a7e-2680">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2680">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f5a7e-2681">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2681">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f5a7e-2682">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2682">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5a7e-2683">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2683">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f5a7e-2684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2684">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-2685">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2685">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f5a7e-2686">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2686">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f5a7e-2687">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2687">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f5a7e-2688">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2688">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f5a7e-2689">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2689">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f5a7e-2690">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2690">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f5a7e-2691">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2691">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f5a7e-2692">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2692">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f5a7e-2693">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2693">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f5a7e-2694">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2694">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f5a7e-2695">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2695">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f5a7e-2696">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2696">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f5a7e-2697">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2697">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f5a7e-2698">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2698">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f5a7e-2699">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2699">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f5a7e-2700">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2700">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f5a7e-2701">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2701">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f5a7e-2702">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2702">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f5a7e-2703">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2703">General</span></span>
* <span data-ttu-id="f5a7e-2704">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2704">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f5a7e-2705">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2705">Az.Profile</span></span>
* <span data-ttu-id="f5a7e-2706">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2706">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f5a7e-2707">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2707">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f5a7e-2708">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2708">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f5a7e-2709">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2709">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f5a7e-2710">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2710">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f5a7e-2711">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2711">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f5a7e-2712">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2712">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5a7e-2713">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2713">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5a7e-2714">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2714">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2715">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-2716">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2716">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f5a7e-2717">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2717">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f5a7e-2718">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2718">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5a7e-2719">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2719">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5a7e-2720">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2720">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f5a7e-2721">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2721">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f5a7e-2722">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2722">Az.Insights</span></span>
* <span data-ttu-id="f5a7e-2723">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2723">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f5a7e-2724">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2724">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f5a7e-2725">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2725">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f5a7e-2726">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2726">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-2727">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2727">Az.Network</span></span>
* <span data-ttu-id="f5a7e-2728">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2728">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f5a7e-2729">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2729">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f5a7e-2730">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2730">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f5a7e-2731">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2731">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f5a7e-2732">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2732">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f5a7e-2733">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2733">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f5a7e-2734">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2734">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5a7e-2735">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2735">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5a7e-2736">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2736">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-2737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2737">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-2738">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2738">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f5a7e-2739">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2739">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f5a7e-2740">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2740">Az.ServiceBus</span></span>
* <span data-ttu-id="f5a7e-2741">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2741">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5a7e-2742">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2742">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5a7e-2743">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2743">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f5a7e-2744">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2744">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f5a7e-2745">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2745">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f5a7e-2746">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2746">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f5a7e-2747">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2747">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f5a7e-2748">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2748">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f5a7e-2749">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2749">Az.Profile</span></span>
* <span data-ttu-id="f5a7e-2750">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2750">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f5a7e-2751">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2751">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-2752">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2752">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-2753">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2753">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f5a7e-2754">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5a7e-2755">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2755">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5a7e-2756">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2756">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f5a7e-2757">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2757">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f5a7e-2758">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2758">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f5a7e-2759">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2759">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f5a7e-2760">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2760">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-2761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2761">Az.Network</span></span>
* <span data-ttu-id="f5a7e-2762">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2762">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f5a7e-2763">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2763">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-2764">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2764">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-2765">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2765">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f5a7e-2766">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2766">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f5a7e-2767">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2767">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f5a7e-2768">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2768">Azure.Storage</span></span>
* <span data-ttu-id="f5a7e-2769">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2769">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f5a7e-2770">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2770">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f5a7e-2771">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2771">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f5a7e-2772">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2772">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f5a7e-2773">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2773">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5a7e-2774">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2774">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5a7e-2775">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2775">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5a7e-2776">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2776">Az.Compute</span></span>
* <span data-ttu-id="f5a7e-2777">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2777">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f5a7e-2778">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2778">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f5a7e-2779">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2779">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f5a7e-2780">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2780">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f5a7e-2781">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2781">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5a7e-2782">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2782">Az.Network</span></span>
* <span data-ttu-id="f5a7e-2783">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2783">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f5a7e-2784">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2784">new cmdlets added</span></span>
    - <span data-ttu-id="f5a7e-2785">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2785">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f5a7e-2786">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2786">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f5a7e-2787">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2787">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f5a7e-2788">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2788">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f5a7e-2789">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2789">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f5a7e-2790">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2790">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f5a7e-2791">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2791">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f5a7e-2792">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2792">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f5a7e-2793">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2793">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f5a7e-2794">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2794">Az.RedisCache</span></span>
* <span data-ttu-id="f5a7e-2795">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2795">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f5a7e-2796">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2796">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5a7e-2797">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2797">Az.Resources</span></span>
* <span data-ttu-id="f5a7e-2798">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2798">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f5a7e-2799">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2799">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5a7e-2800">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2800">Az.Sql</span></span>
* <span data-ttu-id="f5a7e-2801">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2801">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5a7e-2802">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2802">Az.Websites</span></span>
* <span data-ttu-id="f5a7e-2803">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2803">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f5a7e-2804">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2804">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f5a7e-2805">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2805">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f5a7e-2806">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="f5a7e-2806">Initial Release</span></span>
